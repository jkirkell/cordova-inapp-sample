cordova-inapp-sample
====================

<h3>Pre-requisites</h3>
<ol> 
<li>npm install cordova -g</li>
<li>npm install plugman -g</li>
</ol>

<h3>Create a project for in-app purchases</h3>
<ol>
<li>cordova create cordova-inapp-sample</li>
<li>cd cordova-inapp-sample</li>
<li>cordova platforms add ios</li>
<li>cd platforms/ios</li>
<li>plugman install --platform ios --project ./ --plugin https://github.com/j3k0/PhoneGap-InAppPurchase-iOS.git</li>
</ol>

<h3>open the project in Xcode</h3>

Go to the Build Phases tab and add "-fno-objc-arc" to inapppurchase.m and SKProduct+LocalizedProce.m under compiled sources.

* Look at cordova_plugins.js in the platforms/ios/www root to see the JavaScript bridge and where storekit is assigned. 
* Look at config.xml at the top of the tree (not in www) to see the reference to the InAppPurchase plugin

At this point, you now have the PhoneGap-InAppPurchase-iOS plugin installed and can code for it.

NOTE: running cordova build ios will overwrite so if you want to use that command, make sure you copy files from www up to the merges/ios folder. 
