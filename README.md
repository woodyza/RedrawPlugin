# Cordova Refresh plugin

This little plugin allows forcing the cordova webview to invalidate, triggering a full redraw of the component. This is to allow working around rendering issues in some versions of Android when the webview isn't responding to dynamic CSS or HTML content updates in JavaScript.

Use responsibly, overdoing the refresh calls will have a negative impact on battery life.

## Installation

### With cordova-cli

If you are using [cordova-cli](https://github.com/apache/cordova-cli), install
with:

    cordova plugin add https://github.com/woodyza/RedrawPlugin.git

### With plugman

With a plain [plugman](https://github.com/apache/cordova-plugman), you should be
able to install with something like:

    plugman --platform <ios|android> --project <directory> --plugin https://github.com/woodyza/RedrawPlugin.git

## Use from Javascript

    cordova.plugins.Redraw.invalidateWebView();
