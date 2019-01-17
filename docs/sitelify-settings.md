---
id: sitelify-settings
title: Sitelify Settings
sidebar_label: Sitelify Settings
---

This section describes the settings that can be configured in the Sitelify config file `Altola.Sitelify.config`.

Setting | Default value | Description
--- | --- | ---
`Sitelify.PreviewEditorDelay` | `1000` | <p>The number of milliseconds to wait after a site is deployed before the Netlify site preview editor is displayed in Sitelify Manager.</p><p>After a site is deployed to Netlify for the first time, it takes a few seconds before the site can be accessed using SSL. Increase this value if, after deploying a site to Netlify, the preview editor is not displaying the Netlify site.</p><p></p>

<!-- SITELIFY - PREVIEW EDITOR DELAY (time in ms, default 1000)
           After a site is deployed to Netlify for the first time, it takes a few seconds 
           before the site can be accessed using SSL. Increase this value if, after deploying
           a site to Netlify, the preview editor is not displaying the Netlify site.
      -->
      <setting name="Sitelify.PreviewEditorDelay" value="1000" />