---
layout: post
title:  "Publishing a ReactNative Expo App to Google Play Store"
date:   2021-07-11 07:14:30 -0500
categories: Technology
---

This document is work-in-progress.

# Prerequisites
- bash
- NodeJS
- JDK
- Turtle CI - `npm install -g turtle-cli`

# Signing the app

## Generate a Keystore

```
keytool -genkeypair -v -keyalg RSA -keysize 4096 -validity 10000 -keystore KEYSTORE_OUTPUT_FILE.keystore -alias KEY_ALIAS
```
Keep the keystore file, password and alias in a safe encrypted place.

# App Icon and Permissions

Update the App icon

Update app.json, add permissions and package attributes.

```
"android": {
    "adaptiveIcon": {
        "foregroundImage": "./assets/images/adaptive-icon.png",
        "backgroundColor": "#ffffff"
    },
    "permissions": [], 
    "package": "com.yourapp"
},
```

## Create a Google Service Account and download its JSON private key

Steps can be found here https://github.com/expo/fyi/blob/master/creating-google-service-account.md


