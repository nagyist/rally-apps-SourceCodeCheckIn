Rally Source Code Check In
============

![Title](https://raw.github.com/RallyApps/SourceCodeCheckIn/master/screenshots/title-screenshot.png)

## Overview

The Source Code Check-In app displays a list of recent check-ins from Rally source code connectors.

## How to Use

To make use of this app, you need to connect Rally to a source code check in system. Supported connectors include AccuRev, Git (in beta), Perforce, Subversion, and Team Foundation Server. You can find instructions on how to link Rally with your check in system [here](http://www.rallydev.com/help/source-code-integrations).

### Running the App

If you want to start using the app immediately, create an Custom HTML app on your Rally dashboard. Then copy App.html from the deploy folder into the HTML text area. That's it, it should be ready to use. See [this](http://www.rallydev.com/help/use_apps#create) help link if you don't know how to create a dashboard page for Custom HTML apps.

Or you can just click [here](https://raw.github.com/RallyApps/SourceCodeCheckIn/master/deploy/App.html) to find the file and copy it into the custom HTML app.

### Using the App

After connecting Rally to your source code check in system, the app is ready to use. To show more revision history, you need to manually change the page size in SourceCodeCheckIn.js. The default size is 20. You need to rerun rake after you make this revision. 

## Customize this App

You're free to customize this app to your liking (see the License section for details). If you need to add any new Javascript or CSS files, make sure to update config.json so it will be included the next time you build the app.

This app uses the Rally SDK 1.32. The documentation can be found [here](http://developer.rallydev.com/help/app-sdk). 

Available Rakefile tasks are:

    rake build                      # Build a deployable app which includes all JavaScript and CSS resources inline
    rake clean                      # Clean all generated output
    rake debug                      # Build a debug version of the app, useful for local development
    rake deploy                     # Deploy an app to a Rally server
    rake deploy:debug               # Deploy a debug app to a Rally server
    rake deploy:info                # Display deploy information
    rake jslint                     # Run jslint on all JavaScript files used by this app, can be enabled by setting ENABLE_JSLINT=true.

## License

SourceCodeCheckIn is released under the MIT license.  See the file [LICENSE](https://raw.github.com/RallyApps/SourceCodeCheckIn/master/LICENSE) for the full text.