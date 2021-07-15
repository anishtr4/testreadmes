Spotifile (Salesforce + React Native)
===

This is an example [Sanity](https://www.sanity.io) backed [React Native](https://facebook.github.io/react-native/) app for the movies database dataset.

## Setup

This project was bootstrapped with [Forcereact](https://www.npmjs.com/package/forcereact).

Below you'll find information about performing common tasks.

## Table of Contents

* [Development Envroment Setup](#development-environment-setup)  
* [Getting Started](#getting-started)  
* [Configure Endpoint RedirectURI And Consumer Key](#configure-Endpoint-RedirectURI-and-consumer-key)
  * [Salesforce Endpoint](#salesforce-endpoint)
  * [Consumer Key](#consumer-key)
  * [oauthRedirectURI](#oauthRedirectURI)
* [Pod Installation](#pod-installation)
* [Available Scripts](#available-scripts)
  * [npm start](#npm-start) 
  * [npm run ios](#npm-run-ios) 
* [Customizing App Icon](#customizing-app-icon)
* [Core App Struture](#core-app-struture) 


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
## Getting Started
1. Go to project's root directory, `cd spotifile`
2. Run `yarn`/ `npm install`to install dependencies
3. Go to ios folder run `pod install`
4. Go back to project root directory run `npm start`
5. Open `Spotifile.xcworkspace` and run it in any simulator

## Configure Endpoint RedirectURI And Consumer Key

You can configure some of App's behavior using environment variables.

### Salesforce Endpoint

In project navigator open Spotifle "Supporting Files" and open info.plist. Update `SFDCOAuthLoginHost` field/key value to specific endpoint/url. Make sure to remove HTTP/HTTPS from the URL.

### Consumer Key

In project navigator open Spotifle "Supporting Files" and open bootconfig.plist. Update `remoteAccessConsumerKey` field/key value to appropriate Consumer Key.

### oauthRedirectURI

In project navigator open Spotifle "Supporting Files" and open bootconfig.plist. Update `oauthRedirectURI` field/key value to appropriate one.


## Pod Installation
Make sure to do pod install in the ios directory(spotifile/ios).
    ```
    pod install
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

Like `npm start`, but also attempts to open your app in the iOS Simulator if you're on a Mac and have it installed. Alternatively you can open workspace file in xcode and run the project from there make sure to run `npm start` before running it from xcode.


## Customizing App Icon

You can edit AppIcon in "images.xcassets". Open Spotifile.xcworkspace in project navigator open Spotifle "Supporting Files" and open "images.xcassets" there you can find AppIcon and update the required icons according to the given size/aspect ration 

## Core App Struture 

The application is utilizing react-native-paper [React Native Paper](https://callstack.github.io/react-native-paper/) as a core framework (gradually trying to remove React Native Paper dependecy)

As a part of state management we are using [Redux](https://redux.js.org/), [Redux-saga](https://redux-saga.js.org/), [Redux-persist](https://www.npmjs.com/package/redux-persist)

    ### A typical top-level directory layout 


    App
    ├── action                   # Redux actions
    ├── api                      # All the http request/api methods
    ├── assets                   # Art files/icons/images required for the application
    ├── components               # Application components (Following Atomic  Design) Note: Templates is not being used as of now
    │   ├── Atom                    # Atoms are the smallest possible components
    │   ├── Molecules               # Composition of one or more components of atoms
    │   ├── Organisms               # Organisms are the combination of molecules that work together or even with atoms that compose more elaborate interfaces
    │   └── Templates               # Ttemplates create relationships between the organisms and others components through positions, placements and patterns 
    ├── config                   # Contains configurations (app version, api queries) Note: Some of the api queries is not being used any more.
    ├── lib                      # Contains helper functions(create reducer etc).
    ├── navigation               # Contains application navigation flow an navigation options
    ├── permission               # permission request create initlaly for android (as android is not part of the scope now not maintaining it furthur)
    ├── reducers                 # Redux reducers created using helper function available in the lib folder
    ├── sagas                    # Redux-saga files ( is a redux middleware library)
    ├── screens                  # Application screens(home,about us,search ..etc)
    ├── store                    # Redux store configuration (state container which holds the application's state)
    ├── theme                    # Application core styles, colors, font size,Typo graphy 
    └── utils                    # collection of utility function used through out the app
    

