cordova-inapp-sample
====================
Pre-requisites
1. npm install cordova -g
2. npm install plugman -g

Create a project for in-app purchases
1. cordova create cordova-inapp-sample
2. cd cordova-inapp-sample
3. cordova platforms add ios
4. cd platforms/ios
5. plugman install --platform ios --project ./ --plugin https://github.com/j3k0/PhoneGap-InAppPurchase-iOS.git

open the project in Xcode

Go to the Build Phases tab and add "-fno-objc-arc" to inapppurchase.m and SKProduct+LocalizedProce.m under compiled sources.

* Look at cordova_plugins.js in the platforms/ios/www root to see the JavaScript bridge and where storekit is assigned. 
* Look at config.xml at the top of the tree (not in www) to see the reference to the InAppPurchase plugin

At this point, you now have the PhoneGap-InAppPurchase-iOS plugin installed and can code for it.

NOTE: running cordova build ios will overwrite so if you want to use that command, make sure you copy files from www up to the merges/ios folder. 