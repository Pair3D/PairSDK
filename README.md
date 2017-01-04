# README #

Welcome to the Pair SDK.

## Setup ##

### 1. Get your SDK License Key ###
 * Contact Pair for a key: contact@pair3d.com

### 2. Integrate The SDK With Your App ###
* Download and extract the PairSDK.
* Add the `include` and `PairSDKAssets` folders to your project.
* Navigate to your app's target Build Settings. Add to `Header Search Paths` the relative path to the include folder . Example 'PairSDK/include`.
* Set `Enable Bitcode` to `NO`.
* Add `Other Linker Flags` `-l"stdc++"`.
* Navigate to your app's target Build Phases. Add `libPairSDK.a` to `Link Binary With Libraries`.
* Navigate to your app's target Build Settings. Add to `Library Search Paths` the path to the PairSDK library. Example `$(PROJECT_DIR)/PairSDK`.

### 3. Using The SDK In Your App ###
* The SDK requires access to the camera. Add the `NSCameraUsageDescription` key to your apps Info.plist file.
* In your Application delegate, add `#import "Pair.h"`and inside applicationDidFinishLaunching: add: `Pair.licenseKey = @"YOUR_PAIR_SDK_KEY";` Replace YOUR_PAIR_SDK_KEY with the key provided to you by Pair.
* Add the PairView class to one of your view controllers just like you would attach any other UIView. Note that only one can be added at a time.
* Invoke `resume` on the PairView instance: `[self.pairView resume];`
