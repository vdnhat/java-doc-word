---
description: >-
  The CDP365Analytic SDK collects data of shopper's activities. Which enables
  you to make informed decisions regarding app marketing and performance
  optimizations.
---

# Getting Started

#### Prerequisites

* Use Xcode 10 or higher.
* Target iOS 12.0 or higher.

{% hint style="warning" %}
**`Note:`**Begining with iOS 9, iOS app use App Transport Security \(ATS\), a data in transit security feature that enforces encrypted conections. See App Transport Security to configure your info. plist continuing to ensure your ads are not impacted bey ATS
{% endhint %}

#### Import the CDP365Analytic SDK

* **CocoaPods**

The simplest way to import the SDK into an iOS project is to use CocoaPods. Open your project's Podfile and add the line to your app's target:

```c
pod 'CDP365Analytic'
```

Then from the command line run:

```c
pod install --repo-update
```

This creates an .xcworkspace file for your application. Use this file for all future development on your application.

{% hint style="warning" %}
**Note:** If you're new to CocoaPods, see their official documentation for in to how to create and use Podfiles
{% endhint %}

* **Manual**

1. Download an unzip the SDK framework directly, and import the following frameworks into your Xcode project: [`CDP365Analytic.framework`](https://drive.google.com/drive/folders/118p2mnQG-xzd3HI2gCL0zpTvHocw2OnK?usp=sharing)\`\`
2. Add the -ObjC linker flag to **Other Linker Flags** in your project's build settings.

#### **Add CDP365 Configuration File**

1. Download [CDP365\_Config.plist](https://drive.google.com/file/d/1rZgTC5V_CprKPwNLKQ8K54IWT4f0Z5pC/view?usp=sharing) to obtain your CDP365 iOS configure file.
2. Move your config file into the root of your Xcode project.

#### Initialize CDP365Analytic SDK

First, configure the shared `CDP365Analytic` object inside `AppDelegate`. This make it possible for your app to send data to Analytics. Following:

* Include the necessary headers.
* Set the CDP365Analytic tracker inside `didFinishLaunchingWithOptions`.

Import the Insight module in your `AppDelegate`:

{% tabs %}
{% tab title="Swift" %}
```swift
import CDP365Analytic
```
{% endtab %}

{% tab title="Objective-C " %}
```objectivec
#import <CDP365Analytic/CDP365Analytic-Swift.h>
```
{% endtab %}
{% endtabs %}

  
Typically in your app's `didFinishLaunchingWithOption`method:

{% tabs %}
{% tab title="Swift" %}
```swift
CDP365Analytic.configure()
```
{% endtab %}

{% tab title="Objective-C" %}
```objectivec
[CDP365Analytic configure];
```
{% endtab %}
{% endtabs %}



