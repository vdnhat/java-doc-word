---
description: >-
  The Insight SDK collects data of shopper's activities. Which enables you to
  make informed decisions regarding app marketing and performance optimizations.
---

# Getting Started

#### Prerequisites

* Use Xcode 10 or higher
* Target iOS 10.0 or higher

{% hint style="warning" %}
**`Note:`**Begining with iOS 9, iOS app use App Transport Security \(ATS\), a data in transit security feature that enforces encrypted conections. See App Transport Security to configure your info. plist continuing to ensure your ads are not impacted bey ATS
{% endhint %}

#### Import the Insight SDK

* **CocoaPods**

The simplest way to import the SDK into an iOS project is to use CocoaPods. Open your project's Podfile and add this line to your app's target:

```swift
pod 'ANInsight'
```

Then from the command line run:

```swift
pod install --repo-update
```

 This creates an `.xcworkspace` file for your application. Use this file for all future development on your application.

{% hint style="warning" %}
**`Note:`** _****_If you're new to Cocoapods, see their official documentation for in to how to create and use Podfiles
{% endhint %}

* **Manual**

1. Download an unzip the SDK framework directly, and import the following frameworks into your Xcode project: [`ANInsight.framework`](https://drive.google.com/file/d/1nthKLSgsfJ6dBRDCDvo2Q8j4o-gXXlXY/view?usp=sharing)\`\`
2. Add the -ObjC linker flag to **Other Linker Flags** in your project's build settings.

#### **Add ANInsight Configuration File**

1. Download [ANInsight.plist](https://drive.google.com/file/d/1GjD6jXKydje6PI-syPEYEGhC8xQfJDoY/view?usp=sharing) to obtain your ANInsight iOS configure file.
2. Move your config file into the root of your Xcode project.

#### Initialize Insight SDK

First, configure the shared `ITAnalytics` object inside `AppDelegate`. This make it possible for your app to send data to Analytics. Following:

* Include the necessary headers.
* Set the ITAnalytics tracker inside `didFinishLaunchingWithOptions`.

Import the Insight module in your `AppDelegate`:

{% tabs %}
{% tab title="Swift" %}
```swift
import InsightSDK
```
{% endtab %}

{% tab title="Objective-C " %}
```objectivec
#import <InsightSDK/InsightSDK-Swift.h>
```
{% endtab %}
{% endtabs %}

  
Typically in your app's `didFinishLaunchingWithOption`method:

{% tabs %}
{% tab title="Swift" %}
```swift
ITAnalytic.configure()
```
{% endtab %}

{% tab title="Objective-C" %}
```objectivec
[ITAnalytics configure];
```
{% endtab %}
{% endtabs %}



