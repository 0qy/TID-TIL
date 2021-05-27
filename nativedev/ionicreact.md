# Ionic - React

Native like flow with react and ionic, writing apps in javascript and react.

`npm install -g @ionic/cli`

`ionic start appName blank --type=react --capacitor` appName for the name of the application, blank is for the types of templates. Blank is usually the one that one might wanna use but there are other ones for learning or playing around with different capabilities. `type=react` is telling ionic you are using react, but can also use angular here. `--capacitor` is telling it whether to install capacitor to begin with. This can also be installed later.

`ionic serve`

Ionic cli to create app in one command

Dev environment sets up local server and debugable through the browser.

Debug can also happen live on device with Live Reload `ionic capacitor run <platform> -l --address=<local ip address>` platform for android or ios, -l is for live reload.

For Android Edit AndroidManifest.xml Modify `<adpplication android:usesCleartextTraffic="true">` This is to tell andoird to support clear text which is http communication

## Ionic React Components

IonPage, IonHeader, IonToolBar, IonTitle to create native feeling to a ionic react app. note: search on ionic website with angular annotation i.e. Ion-page, Ion-Header, Ion-TooBar

## Native Capabilities

Community Plugins and Cordova Pugins, and Capacitor, and PWA elements

## Ionic React Hooks

Community Driven library covering most of native capabilities.

## Ionic React vs React Native

Ionic React claims to have bigger componnet list, most versatile. It is also slower and have no native components. React Native uses native UI layer and it will be faster and mighit be more familiar to users.

