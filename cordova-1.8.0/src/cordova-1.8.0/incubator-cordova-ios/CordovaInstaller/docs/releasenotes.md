<!--
#
# Licensed to the Apache Software Foundation (ASF) under one
# or more contributor license agreements.  See the NOTICE file
# distributed with this work for additional information
# regarding copyright ownership.  The ASF licenses this file
# to you under the Apache License, Version 2.0 (the
# "License"); you may not use this file except in compliance
# with the License.  You may obtain a copy of the License at
# 
# http://www.apache.org/licenses/LICENSE-2.0
# 
# Unless required by applicable law or agreed to in writing,
# software distributed under the License is distributed on an
# "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
#  KIND, either express or implied.  See the License for the
# specific language governing permissions and limitations
# under the License.
#
-->
## Release Notes for Cordova ({VERSION})  ##
  
Cordova is a static library and static framework that enables developers to include the Cordova API in their iOS application projects easily, and also create new Cordova-based iOS application projects through an Xcode project template.

### 1.8.0 (20120605) ###

* Fixes CB-819 fail callback not invoked
* [CB-794] Add HTTP status code to FileTransferError object for iOS
* [CB-359] Updates to adhere to W3C spec for geolocation. Changing actions based on changes incorporated into cordova-js
* [CB-683] pause/resume events now should pass in event object into handlers
* [CB-464] rewrite of accel plugin, simplified accel to start/stop actions.
* [CB-623] added Logger plugin
* Fixed CB-513 - Remove cast functionality from CDVPluginResult, obsolete
* Fixed CB-594 - Remove checks for retainCount
* Fixed CB-637 - Add a doc on how to update the template project in the bin subfolder
* Updated bin folder scripts.
* Fixed CB-669 - verify.sh file in a new Cordova-based application project should not be included in the .app bundle
* Fixes CB-471 - LocalFileSystem.PERSISTENT "do not back up" file attribute iOS
* Fixed typo in File.getMetadata - error callback had OK instead of ERROR status
* Fixes CB-610 - Capture.bundle missing microphone image resources for retina iPad results in mis-drawn recording interface
* Fixes CB-751 - Undefined function is called when orientation change
* Fixes CB-754 - Use of -weak_library in 'other library flags' of generated template XCode app causes crashes in Simulator when Obj-C Blocks are used
* Fixes CB-628 - Scrub installation process, document artifacts of Xcode 3 support, mention no ARC
* Fixed CB-628 - Scrub installation process, document artifacts of Xcode 3 support, mention no ARC
* Fixes CB-684 - Not enough time for background execution of WebSQL/LocalStorage backup (when app goes to the background)
* Fixes CB-766 - Update bin/debug shell script to point to Homebrew ios-sim 1.4 download
* Fixes CB-464 - Refactor accelerometer native code in iOS
* Fixes CB-760 - Camera returns incorrect image size
* Fixed warning in CDVLocation
* Fixed EXC_BAD_ACCESS error in CDVAccelerometer
* Fixes CB-818 - Make CDVViewController also implement initWithNibName
* Fixes CB-825 - Makefile: remove direct download of Markdown and wkhtmltopdf (uses homebrew to download)
* Fixes CB-328 - Cordova crashes on iOS 3.x devices
* Fixes CB-851 - guide for using url schemes in iOS

<br />

### 1.7.0 (20120430) ###

* Fixed CB-183, CB-54 - ios camera targetWidth/Height don't match the documentation Fixes CB-183 and CB-54
* Fixed CB-511 Changed deviceproperties version to "cordova" property
* Fixed CB-483 - FileTransfer - unknown property attribute 'atomic' when building from source (Xcode 3 only)
* Fixed CB-507 - Remove excessive debug logging in execute delegate method in CDVViewController
* Implemented CB-536 - Add new selector to CDVViewController to create a new CDVCordovaView, so subclasses can override it
* Workaround for CB-509 - geolocation.clearWatch doesn't shut the GPS down under iOS
* Fixed CB-537 - media.seekTo fails with NSRangeException
* Fixed CB-544 - iOS Geolocation fails if Cordova.plist EnableLocation = YES
* Fixed CB-543 - FileTransfer.upload WebKit discarded an uncaught exception
* Fixed CB-391 - camera.getPicture crash
* Implemented CB-535 - Add a way to log JavaScript exceptions, parse errors, and get JS stack frame events (with line numbers, etc)
* Fixed CB-494 - Move Cordova.plist section from "How to use Cordova as a Component Guide" to its own doc
* Fixed CB-571 - stubbed out create method to remove error when creating Media objects, also added another check if file does not exist.
* Fixed CB-386 - added retina iPad splash screens. made sure retina ipad icon files shows up during load.
* Re-fix CB-347 - localStorage / SQLDatabase Error after App update (timing issue for applying fix)
* Adjust splash screen position based on orientation and status bar size

<br />

### 1.6.1 (20120416) ###

* Fixed CB-496 - Camera.getPicture - will always return FILE\_URI even though DATA\_URL specified
* Fixed CB-497 - online and offline events are not being fired in 1.6.0
* Fixed CB-501 - orientationchange event is not being fired in 1.6.0
* Fixed CB-302 - orientation change event fired off twice on iOS 5.x
* Fixed CB-507 - Remove excessive debug logging in execute delegate method in CDVViewController

<br/>

### 1.6.0 (20120409) ###
* Updates for Media API
* Contacts updates for Unified JavaScript
* Fixed Contacts.save return value and Notification.confirm
* Changed Device initialization to use a require-based pattern
* Added require syntax for firing events in ios
* Added a getConnectionInfo method for compatibility
* Added require in pluginresult helper funcs
* Updated plist of plugin names -> classes to adhere to common labels in other platforms
* Rewrite of accelerometer code and removed DeviceInfo old init approach
* Added warning about changing compiler settings in xcode
* Changed Accel values to doubles
* Tweaked battery plugin for cordova-js use
* Updated interface to get Camera working. 
* Rewrote Location class to use cordova-js unified approach.
* Updated refs from require("cordova") to just "cordova", and other require calls to cordova.require
* Updated sub-project cordovalib steps
* Fixed Compass, Location for cordova-js integration
* Added unification of accelerometer values on ios (based on android values)
* Removed old JS, added cordova-js version
* Changes to CordovaLib makefile for generating JS
* Fixed CB-260: Can't install Phonegap with new Xcode 4.3
* Fixed Xcode app detection (using Spotlight) in Makefile
* Fixed CB-306 - Remove extra template App delegate methods
* Fixes CB-255 - iOS: a parameter with value 'null' is not passed to 'arguments' array
* Fixed CB-236 - Add ContentLength Header in Upload request
* Fixed CB-300 - CDVFileTransfer crashes with 303 and empty response
* Fixed CB-148, CB-316: Playing HTTP / HTTPS urls using the Media API is not working
* Improved Makefile for mixed Xcode 4.2 and Xcode 4.3.1 environment.
* Fixed CB-329 - Add warning if multi-tasking is not supported on an iOS device (to console log)
* Fixed CB-317 : Xcode: Shell Script Invocation Error when directory has spaces in name
* Fixed CB-330 - localStorage / SQLDatabase no longer persistent after iOS 5.01 update
* Fixed CB-347 - iOS 5.1 localStorage / SQLDatabase error after upgrading an app
* Fixed shell script error - picks up new location of cordova.js (unified) now
* Fixed NOTICE file with correct project name
* Fixed CB-49 - UUID replacement
* Fixed CB-361 & use timeout to turn off compass sensor
* Fixed CB-427 - add back iOS only getPicture options
* Fixed CB-349 - Remove sessionKey usage (unused) in CDVViewController
* Fixed CB-237 - Updated splash screen assets
* Fixed CB-387 - try/catch wrapper in native iOS code for cordova-js initialization firing alerts when page without cordova.js is loaded in
* Fixed CB-425 - Notification buttons and title are not working for confirm and alert
* Fixed CB-440 - (LLVM-GCC only) Wrong number of arguments specified for 'deprecated' attribute
* Fixed CB-441 - make fails if PackageMaker.app installed at a path with spaces in a folder name.
* Fixed CB-444 - Xcode template new project - AppDelegate's self.invokeString usage was removed
* Fixed CB-380 - Update Cordova Upgrade Guide for 1.6.0
* Fixed CB-445 - Update "How to use Cordova as Component" Guide for 1.6.0
* Fixed CB-381 - Update Cordova Plugin Upgrade Guide for 1.6.0
* Fixed CB-406 - Update README.md
* Fixed CB-433 - CDVFileTransfer.m methods - convert use of "options" object into "arguments" array
* Fixed CB-377 - add a check for PM_APP,  XC_APP, and DEVELOPER in the Makefile
* REMOVED: navigator.splashscreen JavaScript interface (was unofficial) - use **cordova.exec(null, null, "SplashScreen", "hide", [])** OR **cordova.exec(null, null, "SplashScreen", "show", [])**

<br/>

### 1.5.0 (20120302) ###

* Fix NSLog crash in CDVWhitelist.m - parameter order reversed
* Updated the Upgrade Guide for 1.4.1
* Added UIWebViewBounce key to PhoneGap.plist (default is YES) (originally from an @alunny pull request)
* Updated README.md FAQ item #5 (upgrades)
* Added the German and Swedish resources to the Xcode templates
* Fixes CB-149 - Black Bar visible after landscape video
* Fixes CB-221 - On an orientation change, the orientationchange event not fired on iOS 3 and 4 
* Rename PhoneGap to Cordova.
* Completed Cordova Guides for 1.5.0
* Fixed CB-253 - Xcode 4 Cordova-based Application - DEBUG macro not defined
* Default GCC_VERSION is com.apple.compilers.llvm.clang.1_0 now
* Removed Xcode and iOS SDK checks in the installer (for the Xcode 4.3 install which goes under the /Applications folder)

<br/>

### 1.4.1 (20120201) ###
* Fixed CB-212 - iOS orientation switch broken in 1.4.0

<br/>

### 1.4.0 (20120130) ###
* Fixed CB-143 - Removing address from iOS contact causes crash
* Fixed CB-153 - Camera default destination should be FILE_URI
* Fixed CB-7 - Update source headers to apache license
* Fixed CB-42 - MediaPlaybackRequiresUserAction can now be set to NO
* Added stand-alone PGViewController (Cleaver - PhoneGap as a Component)
* Fixed iOS 5 quirks with presenting/dismissing modal viewcontrollers.
* Added 'How to Use PhoneGap as a Component' doc to the .dmg  (as a PDF)
* Added 'PhoneGap Upgrade Guide' doc to the .dmg  (as a PDF)
* Added for legacy support of deprecated PhoneGapDelegate - in core plugins.
* Removed PhoneGapLibTest project and folder
* Updated the app icons, splash-screens, and template icons for the Xcode template to Cordova ones.
* Added Battery core plugin to PhoneGap.plist

<br />

### 1.3.0 (20111219) ###
* added battery into PhoneGap framework compilation
* Fixes CB-101 can't access media in documents://subDir
* Added download method to filetransfer, interface is the same like on Android
* When playing audio from remote URL, stop as soon as download fails and make loading cacheable.
* Fixed #197 errors on repeated getCurrentPosition calls. If the location services were off when getCurrentPosition was called, turn them off again after the position is received.
* Don't force an orientation change unless the current orientation is unsupported
* Fixed callback/callback-ios#15 - Xcode 3.2.6 Linker error when Build for Active Architecture Only = YES
* Fixed callback/callback-ios#23 - on app resume, it always throws either an offline/online event even though the online state never changed
* Fixed warning - implicit conversion of UIInterfaceOrientation to UIDeviceOrientation (which are equivalent, for the two Portraits and two Landscape orientations)
* Fixed callback/callback-ios#22 - Removed unused DetectPhoneNumber and EnableAcceleration values in PhoneGap.plist
* Fixed CB-96 PGWhitelist does not handle IPv4 host addresses with wild-cards
* Added 'resign' and 'active' lifecycle events.

<br />

### 1.2.0 (20111103) ###

* Update for iOS 5 - Switched to using LLVM Compiler and fixed associated warnings. Added armv6 to architectures so can use devices running < iOS5
* Fixed phonegap/phonegap-iphone#313 - return MediaError in error callback
* Added documentation for correctOrientation and saveToAlbum options of camera.getPicture
* Fixed phonegap/phonegap-iphone#302 Compiler warnings in PGMotion
* Fixed phonegap/phonegap-iphone#296 iFrames open in Mobile Safari
* Fixed callback/callback-ios#5 - Optimization: If white-list contains "*" (wildcard), do not do URL processing
* Fixed callback/callback-ios#3 - UniversalFramework target of PhoneGapLib does not compile under Xcode 4.2
* Fixed callback/callback-ios#2 - Convert SBJson library use to JSONKit use
* Fixed problem where deploying to device using PhoneGap.framework, the armv7 slice is missing from the fat binary 
* Connection plugin (Reachability) - stop/start notifier on pause/resume of app (attempt at Reachability crash fix)
* Added OpenAllWhitelistURLsInWebView setting in PhoneGap.plist (to open all white-listed URLs in the PhoneGap webview)

<br />

### 1.1.0 (20110930) ###
  
* fixes issue #212 media play not always calling success callback
* added support for W3C battery status events
* fix audio view sizing on iPad when built for iPhone
* refs #277 regression in camera due to PluginResult changes
* fix broken file tests in mobile-spec
* fix #265 display contact not restoring after pause
* issue #230 Update compass implementation
* fixes #271 Implemented selecting picture type when getting images from library.
* fix #289 update contact to deal with an address with no type specified
* fix #293  Now clearing callback function when battery events stopped
* fix #232 Allow media playback to work when device locked or       add correctOrientation option to rotate images before returning them  
* add option for saving photo to the album
* add success,error method sugar to PGPlugin
* moved `device.js` before `capture.js` because `Capture`'s install function depends on `Device`'s constructor.
* fix, simplify, and extend PluginResult's toJSONString function.
* add unit-test target/product to PhoneGapLib.
* update Capture, Contacts, and File to not rely on PluginResult's previous bug.
* allow for using a custom UIWebView object. Just set self.webView in application:didFinishLaunchingWithOptions: before calling super.
* rework PhoneGap.exec() to execute commands much faster.
* fix a race condition in PhoneGap.exec().
* put the PhoneGap.exec() before deviceready warning in the right place.
* fixed issue #219: geolocation.watchposition() delayed
* fixes #207 iOS 3.x crash: NSConcreteGlobalBlock symbol not found
* fixed #228 getPicture crashes when getting picture from photobook on iPad
* added failing unit-tests for PGContacts.
* updated sample index.html with notes about the white-list.
* fixed #290 regression - modalViewController does not retain the UINavigationController as expected. This will still cause a static analyzer issue though
* restructuring for cli scripts, first pass at test automation, mobile-spec automation
* fixed #215 Add sha1 checksum for the .dmg file
* PhoneGapLib: Re-applied IPHONEOS_DEPLOYMENT_TARGET = 3.0 setting that was clobbered in a pull-request
* fixes #202 PhoneGapViewController code cleanup
* updated PhoneGapLibTest for 1.0.0 release, updated test submodule to latest
* fixed #221 Add linker flags for weak-linking frameworks, to templates
* fixed #225 Xcode 4 www folder warning - add additional help text
* fixed #224 make the default projects universal
* fixed #201 README.pdf - links from converted README.md not clickable, plus re-structure
* converted installer docs to markdown
* updated Makefile for new markdown docs.
* fixed #241 navigator.notification.alert - cannot set empty title
* fixed #199 Unnecessary warnings in console (about:blank)
* fixed #194 Enable white listing of domains that an application can access. All http and https urls MUST be in PhoneGap.plist/ExternalHosts or they will not be handled.
* fixed #233 wildcard support for ACL
* set properties to readonly in the AppDelegate, and removed some of the properties from the public interface.
* fixed #243 Splash screen spinner not visible
Removed GetFunctionName.js (unused)
* fixed #246 Add whitelist capability that includes XMLHttpRequest calls
* usage of VERIFY_ARGUMENTS macro in File plugin - related to #244
* fixed #259: PluginResult toJSONString does not quote strings in arrays
* added ability so that unhanded URLs (i.e. custom schemes in a web-page) will notify PhoneGap plugins of this custom url so that the plugins can handle it themselves. This would give the ability to handle callbacks for OAuth logins (Twitter/Facebook) in the main PhoneGap UIWebview, and not require the ChildBrowser plugin.
* fixes #263 Phone call - tel: scheme handling hides default behaviour
* fixes #269 - Add Obj-C unit-tests for whitelist implementation
* fixed #256 PhoneGapDelegate (UIApplicationDelegate) property hides new property in iOS 5
* fixed #254 Prefix the SBJSON classes included in PhoneGap with 'PG'
* updated README FAQ to be up to date, and numbered the questions for easy reference.
* removed user cruft in .xcodeproj - project.workspace and xcuserdata folders.
* fixed geolocation authorizationStatus on first use. Changes to help debug issue #197
* fixed #197 navigator.geolocation.getCurrentPosition timeouts when native app works
* fixed #255 ability to play inline videos

<br />

### 1.0.0 (20110728) ###
  
* **CHANGED:** Update media implementation to match documentation. Significant modifications to match documentation. Using media.js from Android so significant changes to the code to match that architecture.  Created wrapper for AVAudioPlayer and Recorder to store the mediaId. Kept iOS only prepare() method but removed downloadCompleteCallback. Added seekTo method. 
* **CHANGED:** Default-Landscape.png width increased to 1024px for #185 fix below 
* **FIX:** #188 Xcode 3 Template does not weak-link UIKit, AVFoundation and CoreMedia by default 
* **FIX:** #183 make fails when a user's Developer (Xcode) folder has spaces in it 
* **FIX:** #180 Add README.md to the installer package 
* **FIX:** #186 return null when no organization information. iOS was incorrectly returning an organization object with all null values when there was no organization information. It now correctly returns null. 
* **FIX:** #182 updated getCurrentPosition to update _position variable. Fixed bug where seekTo was setting the _position value in milliseconds rather than seconds. getCurrentPosition was not setting _position to -1 when media was not playing. 
* **FIX:** #191 (CRASH) PhoneGap app re-suspends when resumed after Airplane Mode toggled 
* **FIX:** #196 PhoneGapInstaller.pkg should be signed 
* **FIX:** #185 splash screen ignores supported device orientations (fixed for Universal only - iPhone only on iPad has an iOS bug) 
* **REMOVED:** Installer readme.html is now generated from README.md markdown in the root 
* **REMOVED:** Default~ipad.png is removed from the project templates 
* **ADDED:** Prevents iframes from executing PhoneGap calls via gap urls 
* **ADDED:** Added warning log if splash-screen image is missing. 
* **NOTE:** 1.0.0rc3 tagged in the repo is essentially this release 

<br />

### 1.0.0rc2 (20110719) ###
  
* **FIX:** #167 Generated (by script) Xcode 3 template file fails in Xcode 4 
* **FIX:** #162 better accessibility for timed audio  
* **FIX:** #168 Warning in Xcode 3 project that you haven't added phonegap.*.js, warning never goes away 
* **FIX:** iPhone splash screen not showing (no issue #, fixed in splash screen new feature below) 
* **ADDED:** New PhoneGap.plist options: AutoHideSplashScreen (bool=true), ShowSplashScreenSpinner (bool=true). If AutoHideSplashScreen is false, you can control hiding the splash screen in JavaScript by calling navigator.splashscreen.hide(). 
* **ADDED:** #164 Add phonegap version inside the JavaScript file itself 
* **ADDED:** #166 Create uninstaller for PhoneGapInstaller  
* **ADDED:** #6 implemented Camera.EncodingType to return images as jpg or png from getPicture. 
* **CHANGED:** Sample splash screen images are annotated 
* **REMOVED:** #165 Remove minification of phonegap.*.js file 

<br />

### 1.0.0rc1 (20110712) ###
  
* **FIX:** Splash screen fixes for iPad 
* **REMOVED:** Deprecated items **REMOVED:** Notification activityStart/activityStop, Notification loadingStart/loadingStop, Network.isReachable, debug.log, File.writeAsText, PhoneGapCommand base class for Plugins, unused Image and Movie plugins removed 
* **RESTORED:** Camera core plugin has been un-deprecated until a suitable replacement can be found to grab photos from the Camera Roll/Photo Library. 
* **NEW:** phonegap.js naming convention: now phonegap-1.0.0rc.js, was phonegap.1.0.0rc1.js 
* **NEW:** Camera core plugin supports image scaling 
* **NEW:** Contacts core plugin updated to W3C June 2011 Spec 
* **NEW:** Contacts core plugin supports display and edit contact 
* **NEW:** Capture core plugin supports localized files for a11y prompt in Audio capture. 
* **NEW:** EnableViewportScale key in PhoneGap.plist (to enable viewport initial-scale metadata tag) 
* **NEW:** Plugins: PhoneGap.exec supports service names in Reverse Domain Name (RDN) notation i.e "com.phonegap.MyPlugin" 
* **NEW:** Plugins: PhoneGap.exec should support new signature: PhoneGap.exec(successCallback, failCallback, serviceName, action, [arg0, arg1]) 
* **NEW:** Plugins: Ability to override onMemoryWarning() to handle app memory warnings 
* **NEW:** Plugins: Ability to override onAppTerminate() to handle app termination 
* **NEW:** Plugins: Ability to override handleOpenURL:(NSNotification*) to handle launch of the app from a custom URL 
* **UPGRADERS:** Create a new project, and copy in the new phonegap-1.0.0rc1.*.js and PhoneGap.plist into your existing project 

<br />

### 0.9.6 (20110628) ###
  
* Xcode 3 Template includes the CoreMedia framework (as a weak reference for iOS 3.x) for the W3C Media Capture API 
* Xcode 4 Template includes the CoreMedia framework (as a required reference, template spec limitation) for the W3C Network API. You must change this to an 'optional' reference to target iOS 3.x devices, if not they will crash. 
* **UPGRADERS:** add the existing framework "CoreMedia" to your project, set it to weak/optional in your Target, copy the new phonegap.*.js files in manually to your www folder, and update your script references. Copy the .js files from /Users/Shared/PhoneGap/Frameworks/PhoneGap.framework/www. Copy the "Capture.bundle" from /Users/Shared/PhoneGap/Frameworks/PhoneGap.framework and add it to your project as well (or copy from a new project) 
* **UPGRADERS:** set the existing frameworks "UIKit" and "AVFoundation" to weak/optional (for iOS 3.x support) 
* CoreTelephony.framework can be removed in all projects, it is not needed anymore for the W3C Network Information API 
* Plugins **MUST** add their plugin mapping to *PhoneGap.plist* Plugins key, if not they will not work. 
* **DEPRECATED:** Camera.getPicture will be removed in 1.0 and put in the plugins repo, use the Media Capture API instead 
* **DEPRECATED:** Network.isReachable will be removed in 1.0, use the Network Information API instead 
* **DEPRECATED:** Notification activityStart, activityStop, loadingStart, loadingStop core plugin functions will be removed in 1.0 and put in the plugins repo 
* **DEPRECATED:** Plugin base class 'PhoneGapCommand' will be removed in 1.0, use the base class 'PGPlugin' instead

<br />

### 0.9.5.1 (20110524) ###
  
* Xcode 3 Template includes the CoreTelephony framework (as a weak reference for iOS 3.x) for the W3C Network Information API 
* Xcode 4 Template includes the CoreTelephony framework (as a required reference, template spec limitation) for the W3C Network Information API. You must change this to an 'optional' reference to target iOS 3.x devices, if not they will crash. 
* **UPGRADERS:** add the existing framework "CoreTelephony" to your project, set it to weak/optional in your Target, copy the new phonegap.*.js files in manually to your www folder, and update your script references. Copy the .js files from */Users/Shared/PhoneGap/Frameworks/PhoneGap.framework/www* 
* Xcode 3 Template does not copy the PhoneGap javascript files anymore into your www folder, the javascript files are now part of the template (**Xcode 3 UPGRADERS:** you will need to grab the .js files manually from *~/Documents/PhoneGapLib/javascripts* after building your project at least once) 
* PhoneGapLib use is considered deprecated, for a future installer the Xcode 3 Template will use the PhoneGap.framework exclusively 
* Xcode 4 Template has an improved build script - it will detect whether the 'www' folder reference was added and will warn you if it has not been added (**Xcode 4 UPGRADERS:** you will need to grab the .js files manually from */Users/Shared/PhoneGap/Frameworks/PhoneGap.framework/www*) 
* Added Xcode 4 Template (need to add in www folder reference manually - sample 'www' folder created after first run) 
* Added PhoneGap static framework generation (as the UniversalFramework target in PhoneGapLib xcodeproj) 
* Modified Xcode 3 Template (for compatibility with the Xcode 4 template) 
* Installed PhoneGap static framework in */Users/Shared/PhoneGap/Frameworks/PhoneGap.framework* (for non-admin privilege users, this may change in further updates) 

<br />

### 0.9.5 (20110427) ### 
  
* Updated PhoneGap application template to handle project and PhoneGapLib locations with spaces in it 
* Removed iPad template 
* Updated compiler of application template and PhoneGapLib to LLVM GCC 4.2 
* Cleaned up static analyzer warnings. 
* Updated PhoneGap application template to handle project and PhoneGapLib locations with spaces in it 
* Removed iPad template 
* Updated compiler of application template and PhoneGapLib to LLVM GCC 4.2 
* Cleaned up static analyzer warnings. 

<br />

### 0.9.4 (20110203) ###
  
* phonegap.js is minified using the YUI compressor, and also renamed to phonegap.{ver}.min.js where {ver} is the version number of PhoneGapLib from the VERSION file 
* the PhoneGap template is changed as well, at build time it will replace any references to 'src="phonegap.js"' to the new versioned js file (and copy the new phonegap.{ver}.min.js file). This replacement will look in all files in the 'www' folder. 
* note that with the new PhoneGapLib phonegap.{ver}.min.js renaming, existing PhoneGap templates must copy the new "Copy PhoneGap Javascript" post-build script from the new template (in Xcode, under Targets/[ProjectName]) 

<br />

### 20101102 ###
  
* Updated the Base SDK to "Latest iOS" (iOS 4.2 is the minimum to submit to the App Store) for the project files. This setting requires the latest Xcode 3.2.5 (included with the iOS 4.2 SDK) 

<br />

### 20101019 ### 
  
* Updated the Base SDK to iOS 4.1 (the minimum to submit to the App Store) for the project files 

<br />

### 20100902 ###  
  
* Updated the Base SDK to iOS 4.0 (the minimum to submit to the App Store) for the project files 
* Added PhoneGapBuildSettings.xcconfig to the template. To override your PHONEGAPLIB folder on a project by project basis, modify the PHONEGAPLIB value in this file. 

<br />

### 20100416 ###
  
* Removed keys from PhoneGap.plist (AutoRotate, StartOrientation, RotateOrientation). 
* To support orientation in your app: edit/add the UISupportedInterfaceOrientations (iPhone) or UISupportedInterfaceOrientations~ipad (iPad) key into your app's [appname]-Info.plist, with an array of strings that show what orientation your app supports. The supported values are: UIInterfaceOrientationPortrait, UIInterfaceOrientationLandscapeLeft, UIInterfaceOrientationPortraitUpsideDown, UIInterfaceOrientationLandscapeRight.  
* The first value in the array is the orientation that your app starts in. If you have more than one value in the array, it will autorotate (to the other supported orientations). 

<br />

### 20100406 ###
  
* added iPad universal xcodeproj file (3.2 OS required) 

<br />

### 20091103  
  
* fixed permissions and initial run problems 

<br />

### 20091030 ### 
  
* initial release 
  
<br />
