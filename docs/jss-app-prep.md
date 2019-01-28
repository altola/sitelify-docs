---
id: jss-app-prep
title: Step 1. Preparing JSS app for Sitelify
sidebar_label: Step 1. JSS app prep
---

In order for your JSS app to fetch content from Netlify and not from the Sitecore origin after deployment and remove the need of code changes to make it happen, make sure you set the value of `layoutServiceHost` value to empty string in `scjssconfig.json`:

```javascript
{
  "sitecore": {
    ...
    "layoutServiceHost": ""
  }
}
```

## Optional step
### follow if running multiple JSS apps on the same Sitecore instance

The change above will force the app to fetch content from the same Content Management host.
If you have more than one JSS app configured on that instance or have other sites configured, make the following additional change within your JSS app.

Add one more query string parameter `sc_site` with the value of your JSS app site in configuration to `fetchOptions.querystringParams` that are passed into `dataApi.fetchRouteData`. For example, if using the official JSS app scaffolding, this can be found within `RouteHandler.js`:
```
  const fetchOptions = {
    querystringParams: { sc_lang: language, sc_apikey: config.sitecoreApiKey, sc_site: 'my-jss-app-site-name-in-configuration' },
  };

```

See this [line in official React sample](https://github.com/Sitecore/jss/blob/5d323ffcd6c8024e6e7a18476330dd2a7fa099cd/samples/react/src/RouteHandler.js#L203).

The value of site name can be found in configuration. For the [sample JSS react app](https://github.com/Sitecore/jss/blob/5d323ffcd6c8024e6e7a18476330dd2a7fa099cd/samples/react/sitecore/config/JssReactWeb.config#L34) it's `"JssReactWeb"`, yours will likely be diferent :)

## Redeploy your app

After this change, make sure to deploy your app to the same Sitecore Content Management instance that will be used for Sitelify module installation.

The `jss deploy files` command will be sufficient, as only the app bundle needs to be updated.

## Next steps

Now that the JSS app is prepped for Sitelify and redeployed, let's proceed to the next step in configuring the module.