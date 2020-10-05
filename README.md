# CoindarAPI

[![CI Status](https://img.shields.io/travis/alephao/CoindarAPI.svg?style=flat)](https://travis-ci.org/alephao/CoindarAPI)
[![Version](https://img.shields.io/cocoapods/v/CoindarAPI.svg?style=flat)](https://cocoapods.org/pods/CoindarAPI)
[![License](https://img.shields.io/cocoapods/l/CoindarAPI.svg?style=flat)](https://cocoapods.org/pods/CoindarAPI)
[![Platform](https://img.shields.io/cocoapods/p/CoindarAPI.svg?style=flat)](https://cocoapods.org/pods/CoindarAPI)
[![Swift 5.0](https://img.shields.io/badge/Swift-5.0-orange.svg?style=flat)](https://developer.apple.com/swift/)

A wrapper around the [Coindar API](https://coindar.org/en/api) written in Swift

## Quick Start

Import `CoindarAPI` and create an instance of `Coindar` with your token.

You can get a Coindar token [here](https://coindar.org/en/api/tokens)

```swift
import CoindarAPI

let api = Coindar(token: "MyCoindarToken")
```

Available methods:

```swift
func getEvents(params: EventsParams, onSuccess: ([Event]) -> Void, onError: (Error) -> Void) -> Cancellable

func getCoins(progress: (Double) -> Void, onSuccess: ([Coin]) -> Void, onError: (Error) -> Void) -> Cancellable

func getTags(progress: (Double) -> Void, onSuccess: ([Tag]) -> Void, onError: (Error) -> Void) -> Cancellable

func getSocial(coins: [Coin], onSuccess: ([Social]) -> Void, onError: (Error) -> Void) -> Cancellable
```

## Installation

CoindarAPI is available through [CocoaPods](https://cocoapods.org) and [Swift Package Manager](https://swift.org/package-manager/).

### Cocoapods
Simply add the following line to your `Podfile`:

```ruby
pod 'CoindarAPI'
```

### Swift Package Manager
#### Through Xcode UI (Xcode 11+)

Go to _File -> Swift Packages -> Add Package Dependency..._ and enter package repository URL https://github.com/alephao/CoindarAPI.git, then follow the instructions.

#### Without Xcode

Simply add the following as a dependency to your `Package.swift`, under dependencies:
```swift
.package(url: "https://github.com/alephao/CoindarAPI.git", .upToNextMajor(from: "1.0.0"))
```
then specify "CoindarAPI" as a dependency of the Target in which you wish to use CoindarAPI.

## License

CoindarAPI is available under the MIT license. See the LICENSE file for more info.
