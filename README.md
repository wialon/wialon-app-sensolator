# Sensolator, version 1.3.8: (November 24, 2026)
This is WEB application based on Apps from Gurtam (http://apps.wialon.com).

**This is a legacy app: it is no longer developed or maintained. The code is published as is, without support.**

## Description
Sensolator is a control panel to monitor any number of sensors in a visual interface. Primarily it is designed for stationary units monitoring, including power generators and have different instruments displaying various device conditions. Response to the device faults includes on-line alarm, SMS and email notifications.

## License
[The MIT License](LICENSE-MIT)

## Requirements
 * Browser: a current version of Google Chrome, Firefox, Safari or Edge
 * Language: en, bg, br, de, es, et, fa, fi, fr, hu, pl, ru, sk, tr, vi
 * Components: SDK
 * URL params: Active SID, Base URL, Host URL, Language, Current user

## Quick start
Apps activation through the management system: https://help.wialon.com/en/wialon-hosting/user-guide/management-system/apps  
Working with applications in the GPS tracking system: https://help.wialon.com/en/wialon-hosting/user-guide/monitoring-system/apps

## Installation
The repository contains the app in the form it is hosted in. Put the files on a web server and open `index.html` with the URL params listed above, for example
`index.html?sid=<Active SID>&baseUrl=https://hst-api.wialon.com&user=<Current user>&lang=en`.

 * On start the page requests `/sensolator/app/app.json` and the optional `/sensolator/whitelabel.json` (white label settings) by absolute paths, so host the app under the `/sensolator/` path to have them picked up.
 * `js/main.js` is the code of the app. `js/jq_plugins.js` holds the indicator and chart plugins of the app together with third-party jQuery plugins. `js/vendors.js`, `js/bootstrap.js`, `js/leaflet.js` and `js/modernizr.js` are third-party libraries, concatenated in the form they are distributed in (some of them minified).
 * Leaflet, the WebGIS layer for it and the datepicker locales are loaded from `//apps.wialon.com/plugins/`.
