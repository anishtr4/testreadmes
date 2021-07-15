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
* [Pod Installation](#pod-installation)
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


## Configure Endpoint RedirectURI And Consumer Key

You can configure some of Create React Native App's behavior using environment variables.

### Salesforce Endpoint

In project navigator open Spotifle "Supporting Files" and open info.plist. Update "SFDCOAuthLoginHost" field/key value to specific endpoint/url. Make sure to remove HTTP/HTTPS from the URL.

### Consumer Key

In project navigator open Spotifle "Supporting Files" and open bootconfig.plist. Update "remoteAccessConsumerKey" field/key value to appropriate Consumer Key.

### oauthRedirectURI

In project navigator open Spotifle "Supporting Files" and open bootconfig.plist. Update "oauthRedirectURI" field/key value to appropriate one.


## Pod Installation
Make sure to do apod install in the ios directory.
  
    ```
    pod install
    ```

## Customizing App Icon

You can edit AppIcon in "images.xcassets". Open Spotifile.xcworkspace in project navigator open Spotifle "Supporting Files" and open "images.xcassets" there you can find AppIcon and update the required icons according to the given size/aspect ration 


