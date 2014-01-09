BIFF
===

Set up your environment
-----------------------
##### Install Xcode 5.x
Install this from Apple App Store. After install make sure you also install the *command line tools*.
Open xCode and choose "Xcode -> Preferences -> Downloads" and click on the "Command Line Tools" download arrow located in the rightmost column.

##### Install NodeJS
Install NodeJS by visiting http://nodejs.org and click the big button that sais "Install". This will donload a MacOSX install package (PKG). 
You will find it in your downloads folder. Just doubleclick it and follow the instructions.

##### Install Cordova command line interface (cordova-cli)
Open a terminal and type this command
     
     sudo npm install -g cordova


Sencha Touch code
-----------------

The Sencha Touch Development environment is located in the */src* folder.

Tools used for this was
*    Sencha Touch SDK 2.3.0
*    Sencha Cmd 4.0.1.45


Xcode code
-------------

The Xcode project is */platforms/ios/BIFF.xcodeproj*
This is opened by either double clikcing it or opening it from Xcodes *File -> Open* menu


Building
--------

    cd /<clonefolder>/BIFF/src
    sencha app build testing
    
This will build the Sencha Touch app AND copy the builded files down to the cordova app *platforms/ios/www* 

Debugging
---------

##### Alternative 1: Chrome browser
For general sencha code not involving cordova API the best way to debug is by opening the sencha touch app in Chrome. 
Do this by starting a local web server:

     sencha fs web start -m /<projectfolder>/BIFF/src
     
And the visit http://localhost:1841

##### Alternative 2: Xcode Iphone/Ipad Simulator and Safari
To debug the cordova api´s you need to run the cordova built version of your app and debug it using the Safari web inspector. 

* Open the Xcode project and select your build target. You can choose from simulators and connected devices. 
* Press the big "play" button in Xcode. This will build the app and open it on your device or simulator
* Open safari and select the "developer". Select your web page in the sub menu
* The Safari web inspector will open up connected to the webview in the cordova app.
