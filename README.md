
# UHBConnectivityManager

[![Version](https://img.shields.io/cocoapods/v/UHBConnectivityManager.svg?style=flat)](http://cocoapods.org/pods/UHBConnectivityManager)
[![License](https://img.shields.io/cocoapods/l/UHBConnectivityManager.svg?style=flat)](http://cocoapods.org/pods/UHBConnectivityManager)
[![Platform](https://img.shields.io/cocoapods/p/UHBConnectivityManager.svg?style=flat)](http://cocoapods.org/pods/UHBConnectivityManager)

UHBConnectivity manager is an block oriented objective-c wrapper on Reachability. You can observe network changes by blocks.

## Example

You can register any object with a Unique Identifier 

```objective-c
[[UHBConnectivityManager shared] registerCallBack:^(ConnectivityManagerConnectionStatus status) {
      if (status == ConnectivityManagerConnectionStatusConnected) {
          // Device connected to internet: You may update your data here
      }
      else
      {
          // Show alert 
      }
} forIdentifier:self.memoryAddress];
```

You may unregister the callback in Dealloc method or anywhere you want.
```objective-c
[[UHBConnectivityManager shared] removeCallBackForIdentitfier:self.memoryAddress];
```
## Requirements

iOS Version 7.0 or greater

## Installation

UHBConnectivityManager is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod "UHBConnectivityManager"
```

## Author

Umair Hassan Baig, umairhassanbaig@gmail.com

## License

UHBConnectivityManager is available under the MIT license. See the LICENSE file for more info.



