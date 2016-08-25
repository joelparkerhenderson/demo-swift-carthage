# Demo Swift Carthage

<img src="README.png" alt="Carthage" style="width: 100%;"/>

This demonstration shows:

 * The [Swift](http://swift.org) programming language with
   [Apple](http://apple.com)
   [iOS](http://www.apple.com/ios/)
   [Xcode](https://developer.apple.com/xcode/)

 * The [Carthage](https://github.com/Carthage/Carthage) dependency manager.

 * The [Prelude](https://github.com/robrix/Prelude) Swift micro-framework of simple functional programming tools.

This README describes how to create the project, if you want to try doing it yourself.

## How to create the project

1. Launch Xcode and create a new project. We call ours "Demo Swift Carthage". 

  * Need help? See our repo [demo_swift_hello_world](https://github.com/joelparkerhenderson/demo_swift_hello_world).

1. Use the [Carthage instructions](https://github.com/Carthage/Carthage)

  * We are focusing this project on iOS.

  * Go to the Xcode project "Build Phases" settings area.

  * Click the "+" icon and choose to add a new "Run Script".

  * Set the "Shell" field to `/bin/sh`. 

  * Set the command field to `/usr/local/bin/carthage copy-frameworks`

  * Set the "Input Files" to `$(SRCROOT)/Carthage/Build/iOS/Prelude.framework`

## Create a Cartfile
 
1. Create a file named `Cartfile` at the top level of the project. 
   
1. In the `Cartfile`, list any framework you want, such the Prelude Swift micro-framework of simple functional programming tools.

    github "robrix/Prelude"

1. Run an update, and you see the system is cloning the framework and building it.

    $ carthage update
    *** Cloning Prelude
    *** Checking out Prelude at "1.6.0"
    *** xcodebuild output can be found in /var/folders/g9/6q8fc2h97bgdy60yvd97vgmc0000gn/T/carthage-xcodebuild.3cvsN5.log
    *** Building scheme "Prelude-Mac" in Prelude.xcodeproj
    *** Building scheme "Prelude-iOS" in Prelude.xcodeproj

 * You can now see a new file `Cartfile.resolved` that lists the version number.

 * You can now see a new directory `Carthage` that contains the build.

## Verify

1. Run the app as usual.

  * This will verify that Carthage can connect the files.

  * The app will launch normally. 

  * Success!
  
## Tracking

* Package: demo_swift_carthage
* Version: 1.0.0
* Created: 2016-04-09
* Updated: 2016-08-25
* License: BSD, MIT, GPL
* Contact: Joel Parker Henderson (joel@joelparkerhenderson.com)
