#MotionKit
A nice and clean wrapper for the **CoreMotion Framework**. The Core Motion framework lets your application receive motion data from device hardware and process that data.
The data can be retrieved from **Accelerometer**, **Gyroscope** and **Magnetometer**.
You can also get the *composited gyroscope and accelerometer data* from the **deviceMotion** datatype itself instead of using raw Gyroscope or Accelerometer.

#How It Works:
You can retrieve all the values either by a trailing closure or by a delegate method. Both the methods are fully supported.

##Getting Accelerometer Values
You can get the accelerometer values using just a few lines of code.

```swift
    var motionKit = MotionKit()

    motionKit.getAccelerometerValues(interval: 1.0){

        (x:Double, y:Double, z:Double) in
        // Do whatever you want with the x, y and z values
        println("X: \(x) Y: \(y) Z \(z)")
      }
    }

```
##Getting Gyroscope Values
Gyroscope values could be retrieved by the following few lines of code.

```swift
    var motionKit = MotionKit()

    motionKit.getGyroValues(interval: 1.0){

        (x:Double, y:Double, z:Double) in
        // Do whatever you want with the x, y and z values
        println("X: \(x) Y: \(y) Z \(z)")
      }
    }

```
##Getting Magnetometer Values
Getting Magnetometer values is as easy as grabing a cookie.

```swift
    var motionKit = MotionKit()

    motionKit.getMagnetometerValues(interval: 1.0){

        (x:Double, y:Double, z:Double) in
        // Do whatever you want with the x, y and z values
        println("X: \(x) Y: \(y) Z \(z)")
      }
    }

```
##Getting DeviceMotion Values
Get the composited Accelerometer and Gyroscope values from the Device Motion.

```swift
    var motionKit = MotionKit()

    motionKit.getDeviceMotionValues(interval: 1.0){

        (x:Double, y:Double, z:Double) in
        // Do whatever you want with the x, y and z values
        println("X: \(x) Y: \(y) Z \(z)")
      }
    }

```
##Installation
Just copy **MotionKit.swift** file into your Xcode project, and you're ready to go.
MotionKit would soon be available from CocoaPods and Carthage.

##Precautions
For performance issues, it is suggested that you should use only one instance of CMMotionManager throughout the app. Make sure to stop receiving updates from the sensors as soon as you get your work done.
You can do this in MotionKit like this.
```swift

    // Make sure to call the required function when you're done
    motionKit.stopAccelerometerUpdates()
    motionKit.stopGyroUpdates()
    motionKit.stopDeviceMotionUpdates()
    motionKit.stopmagnetometerUpdates()

```
#Requirements
* iOS 7.0+
* Xcode 6.1

#TODO
- [ ] Add More Methods
- [ ] Adding Background Functionality

#License
<a rel="license" href="http://creativecommons.org/licenses/by-nc/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc/4.0/">Creative Commons Attribution-NonCommercial 4.0 International License</a>.
