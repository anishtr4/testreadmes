Spotifile (Salesforce + React Native)
===

This is an example [Sanity](https://www.sanity.io) backed [React Native](https://facebook.github.io/react-native/) app for the movies database dataset.

## Setup

This project was bootstrapped with [Forcereact](https://www.npmjs.com/package/forcereact).

Below you'll find information about performing common tasks.

## Table of Contents

* [Development Envroment Setup](#development-environment-setup)
* [Available Scripts](#available-scripts)
  * [npm start](#npm-start) 
  * [npm run ios](#npm-run-ios)   
* [Configure Endpoint RedirectURI And Consumer Key](#configure-Endpoint-RedirectURI-and-consumer-key)
  * [Salesforce Endpoint](#salesforce-endpoint)
  * [Consumer Key](#consumer-key)
  * [oauthRedirectURI](#oauthRedirectURI)
* [Adding Flow](#adding-flow)
* [Customizing App Icon](#customizing-app-icon)


## Development Environment Setup
Install Node.js and npm.
  1. To check if these tools are already installed, at the command prompt type npm -v and press Return.
  2. If you get a “command not found” error message, download and install the Node.js package for your operating system at https://nodejs.org/en/.

Install yarn.
```
     [sudo] npm install -g yarn
```
Install forcereact.

```
     [sudo] npm install -g typescript
```

## Available Scripts

If Yarn was installed when the project was initialized, then dependencies will have been installed via Yarn, and you should probably use it to run these commands as well. Unlike dependency installation, command running syntax is identical for Yarn and NPM at the time of this writing.

### `npm start`

Runs your app in development mode.

It will reload if you save edits to your files, and you will see build errors and logs in the terminal.

Sometimes you may need to reset or clear the React Native packager's cache. To do so, you can pass the `--reset-cache` flag to the start script:

```
npm start -- --reset-cache
# or
yarn start -- --reset-cache
```

#### `npm run ios`

Like `npm start`, but also attempts to open your app in the iOS Simulator if you're on a Mac and have it installed. Alternatively you can open workspace file in xcode and run the project from there.


## Customizing App Icon

You can edit AppIcon in "images.xcassets". Open Spotifile.xcworkspace in project navigator open Spotifle "Supporting Files" and open "images.xcassets" there you can find AppIcon and update the required icons according to the given size/aspect ration 


## Configure Endpoint RedirectURI And Consumer Key

You can configure some of Create React Native App's behavior using environment variables.

### Salesforce Endpoint

In project navigator open Spotifle "Supporting Files" and open info.plist. Update "SFDCOAuthLoginHost" field/key value to specific endpoint/url. Make sure to remove HTTP/HTTPS from the URL.

### Consumer Key

In project navigator open Spotifle "Supporting Files" and open bootconfig.plist. Update "remoteAccessConsumerKey" field/key value to appropriate Consumer Key.

### oauthRedirectURI

In project navigator open Spotifle "Supporting Files" and open bootconfig.plist. Update "oauthRedirectURI" field/key value to appropriate one.


```
exp://192.168.0.2:19000
```

The "manifest" at that URL tells the Expo app how to retrieve and load your app's JavaScript bundle, so even if you load it in the app via a URL like `exp://localhost:19000`, the Expo client app will still try to retrieve your app at the IP address that the start script provides.

In some cases, this is less than ideal. This might be the case if you need to run your project inside of a virtual machine and you have to access the packager via a different IP address than the one which prints by default. In order to override the IP address or hostname that is detected by Create React Native App, you can specify your own hostname via the `REACT_NATIVE_PACKAGER_HOSTNAME` environment variable:

Mac and Linux:

```
REACT_NATIVE_PACKAGER_HOSTNAME='my-custom-ip-address-or-hostname' npm start
```

Windows:
```
set REACT_NATIVE_PACKAGER_HOSTNAME='my-custom-ip-address-or-hostname'
npm start
```

The above example would cause the development server to listen on `exp://my-custom-ip-address-or-hostname:19000`.

## Adding Flow

Flow is a static type checker that helps you write code with fewer bugs. Check out this [introduction to using static types in JavaScript](https://medium.com/@preethikasireddy/why-use-static-types-in-javascript-part-1-8382da1e0adb) if you are new to this concept.

React Native works with [Flow](http://flowtype.org/) out of the box, as long as your Flow version matches the one used in the version of React Native.

To add a local dependency to the correct Flow version to a Create React Native App project, follow these steps:

1. Find the Flow `[version]` at the bottom of the included [.flowconfig](.flowconfig)
2. Run `npm install --save-dev flow-bin@x.y.z` (or `yarn add --dev flow-bin@x.y.z`), where `x.y.z` is the .flowconfig version number.
3. Add `"flow": "flow"` to the `scripts` section of your `package.json`.
4. Add `// @flow` to any files you want to type check (for example, to `App.js`).

Now you can run `npm run flow` (or `yarn flow`) to check the files for type errors.
You can optionally use a [plugin for your IDE or editor](https://flow.org/en/docs/editors/) for a better integrated experience.

To learn more about Flow, check out [its documentation](https://flow.org/).
