# Refuge Restrooms for Android
[![license: AGPL](https://img.shields.io/badge/license-AGPL-lightgrey.svg)](https://raw.githubusercontent.com/RefugeRestrooms/refugerestrooms-ios/master/LICENSE)
![platform: android](https://img.shields.io/badge/platform-android-lightgrey.svg)
[![Travis CI Build Status](https://travis-ci.com/RefugeRestrooms/refugerestrooms-android.svg?branch=master)](https://travis-ci.com/RefugeRestrooms/refugerestrooms-android)

[![Play Store Badge](https://cloud.githubusercontent.com/assets/16610908/18124896/7be337b6-6f74-11e6-9814-79b9c2d53961.png)](https://play.google.com/store/apps/details?id=org.refugerestrooms)

Android app for [Refuge Restrooms](http://www.refugerestrooms.org/)

## Getting started
You can use Android Studio (http://developer.android.com/tools/studio/index.html) to build this project, and it should behave like any other android studio project.

Clone the repo here and then in Android Studio go to File -> New -> Import Project and navigate to your clone. You may be prompted by Android Studio to install a few sdk dependencies.

## Contributing
By all means contribute :) Areas which definitely need work are listed as TODOs below. Feel free to add more.

Please try to stick to the android style guidelines http://source.android.com/source/code-style.html. Fields should start with 'm'
In addition, please put curly brackets round your blocks.

If you push code, please make sure it builds correctly. Feel free to use pull requests so that other contributors can check your code. Also create an issue when working on a new feature so we don't duplicate work!

## Functionality
- Works best with GPS Location enabled
- Uses [Google Maps Gestures](https://support.google.com/gmm/answer/3139292?hl=en)
- Selecting location marker shows bathroom info and changes navigation to that location
- Navigation icon in the top right gives text directions
- Blue marker = accessible, red marker = not accessible
- Recent Bathrooms tab displays 150 most recent restrooms. Works without cell service!
- Open location in Google Maps available in each restroom's info window
- If no bathroom within 30(ish?) miles, no results are given by refuge restrooms api, so a toast displays to the user that no bathrooms are nearby
- Max locations shown initially: gps = 20, search = 75
- When GPS isn't enabled
  - Popup box will recommend turning it on initial app start
  - Navigation icon gives a toast to enable location
  - Selecting marker doesn't give location
  - Currently location defaults to Minneapolis (Fix this!)
  - Only really useful to use search
  - Searching with no GPS will move camera to first location found, and shows a toast saying locations were foun

## TODO
- [ ] Better add bathroom section, currently just a webview
  - [ ] Recreate as form in Android and api call to submit (to make more responsive)
  - [ ] Allow current location option like in webapp
- [x] Detailed info window
  - [ ] Allow edit suggestions on restroom like in web app
  - [ ] Allow users to rate and report bathrooms
  - [ ] Allow users to leave comments on bathrooms like in webapp
- [x] Add translations / locales in strings.xml file
  - [ ] Add more languages
- [x] Search bar
  - [ ] Search by address option -- need to translate address to lat/lng
  - [ ] Auto-complete search (google places api)
  - [ ] Have filter options for only returning accessible, unisex restrooms

## Screenshots
![](/app/src/main/res/drawable-hdpi/Screenshots/screen1.png?raw=true)
![](/app/src/main/res/drawable-hdpi/Screenshots/screen2.png?raw=true)
![](/app/src/main/res/drawable-hdpi/Screenshots/screen3.png?raw=true)
![](/app/src/main/res/drawable-hdpi/Screenshots/screen4.png?raw=true)
![](/app/src/main/res/drawable-hdpi/Screenshots/screen5.png?raw=true)
![](/app/src/main/res/drawable-hdpi/Screenshots/screen6.png?raw=true)
