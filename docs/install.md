---
id: install
title:  Step 3. Installing Sitelify
sidebar_label: Step 3. Installing Sitelify
---

Sitelify is a module that is installed on your Sitecore Content Management server. This section guides you through the process of installing and configuring the Sitelify module.

## Install package

Sitelify is installed on your Sitecore server using an installation package.

1. Log into your Sitecore content management (CM) instance as an administrator.
1. Navigate to `Control Panel > Install a package`
1. Upload and install the Sitelify installation package.
1. After the package is installed you will see a new icon in the Sitecore launchpad.

    ![Sitelify app](assets/sitelify-app-sitecore-launchpad.png)

## Configure module

When the module is installed, a new config file is added to your Sitecore server. 
This file contains settings that must be configured before the Sitelify can be used.

The settings below are defined in the following config file:

`[Sitecore CM root folder]\App_Config\Include\Altola.Sitelify\Altola.Sitelify.config`

Setting | Value
--- | ---
`Sitelify.LicenseKey` | Sitelify license key provided to you from Altola.
`Sitelify.NetlifyAccessToken` | Netlify access token you created in the section [Get personal access token](/docs/get-access-token).

## Next steps

Now that the Sitelify module is installed on your Sitecore server, you can configure Sitelify to deploy your JSS application to Netlify.