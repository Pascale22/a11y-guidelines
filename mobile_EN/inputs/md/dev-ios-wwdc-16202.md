# WWDC 2016 : What's New in Accessibility

<script>$(document).ready(function () {
    setBreadcrumb([{"label":"Developer guide", "url": "./dev-mobile.html"},
                   {"label":"iOS WWDC", "url": "./dev-ios-wwdc.html"},
                   {"label":"2016 - What's New in Accessibility"}
	]);
    addSubMenu([
        {"label":"Android guide","url":"dev-android.html"}, 
        {"label":"iOS guide","url":"dev-mobile.html"},
        {"label":"iOS WWDC","url":"dev-ios-wwdc.html"}
    ]);
});</script>

<span data-menuitem="dev-mobile"></span>

This video available on the **official Apple website** ([session 202](https://developer.apple.com/videos/play/wwdc2016/202/)) points out the new accessibility features and some reminders of good practices dealing mostly with VoiceOver.
</br><img style="max-width: 700px; height: auto;" alt="" src="./images/iOSdev/wwdc16-202.png" />
</br></br>Various contents and their video timelapse are indicated hereunder :

- **Functionalities**
    - [MOTOR - Switch Control](#SwitchControl) (02:29)
    - [MOTOR - Dwell Control](#DwellControl) (03:36)
    - [VISION - Display adjustments](#DisplayAdjustments) (04:15)
    - [VISION - Taptic time](#TapticTime) (04:53)
    - [VISION - Magnifier](#Magnifier) (05:17)
    - [HEARING - TTY](#SoftwareTTY) (06:51)
    - [LEARNING - Enhanced typing feedback](#EnhancedTypingFeedback) (07:51)
- **Programing**
    - [UIAccessibilityProtocol](#UIAccessibilityProtocol) (14:19)
    - [accessibilityElements](#accessibilityElements) (18:00)
    - [accessibilityFrameInContainerSpace](#accessibilityFrameInContainerSpace) (19:02)
    - [accessibilityCustomRotors](#accessibilityCustomRotors) (24:19)
    - [tvOS header elements](#tvOS) (31:20)
- **Example** : during this presentation, the hereunder solutions for VoiceOver development pitfalls are suggested thanks to a simple application that's highly recommended [to be watched](https://developer.apple.com/videos/play/wwdc2016/202/?time=698) before going further. Once implemented, these solutions give rise to an application whose VoiceOver efficiency is shown in a [live demonstration](https://developer.apple.com/videos/play/wwdc2016/202/?time=1753).
    - Activate a `table view cell` [(19:58)](https://developer.apple.com/videos/play/wwdc2016/202/?time=1198).
    - Put a dynamic `label` on a button [(20:21)](https://developer.apple.com/videos/play/wwdc2016/202/?time=1221).
    - Make `CALayer` elements accessible *(used to create a graph for instance)* [(20:45)](https://developer.apple.com/videos/play/wwdc2016/202/?time=1245).
    - Understand the navigation problems on a `mapview` with VoiceOver [(23:33)](https://developer.apple.com/videos/play/wwdc2016/202/?time=1413).
    - Searching elements in a `table view` [(25:37)](https://developer.apple.com/videos/play/wwdc2016/202/?time=1537) and in a `mapview` [(27:45)](https://developer.apple.com/videos/play/wwdc2016/202/?time=1665) thanks to the `rotor` item.

Thereafter, the selection of a title will give rise to the video playback directly at the proper moment.
</br></br>
<a name="SwitchControl"></a>
### [MOTOR - Switch Control (02:29)](https://developer.apple.com/videos/play/wwdc2016/202/?time=149)
After a brief reminder about this iOS functionality, a specific focus is invoked in this **new tvOS feature**.
</br><img style="max-width: 700px; height: auto;" alt="" src="./images/iOSdev/wwdc16-202-SwitchControl.png" />
</br></br>
<a name="DwellControl"></a>
### [MOTOR - Dwell Control (03:36)](https://developer.apple.com/videos/play/wwdc2016/202/?time=216)
Connected remote devices allow a user to control their mouse.
</br>When the mouse dwells on a location, the Dwell Control feature displays a timer at the expiration of which an action is triggered *(new MacOS feature)*. 
</br><img style="max-width: 700px; height: auto;" alt="" src="./images/iOSdev/wwdc16-202-DwellControl.png" />
<a name="DisplayAdjustments"></a>
### [VISION - Display adjustments (04:15)](https://developer.apple.com/videos/play/wwdc2016/202/?time=255)
People who are light sensitive or have color issues already use the MacOS and iOS supported features *(inverted colors...)* that are now **available for tvOS**.
</br></br></br>
<a name="TapticTime"></a>
### [VISION - Taptic time (04:53)](https://developer.apple.com/videos/play/wwdc2016/202/?time=293)
Introduced in **WatchOS 3**, this new VoiceOver feature includes a **series of distinct taps** to help people tell time silently and discretely.
</br></br></br>
<a name="Magnifier"></a>
### [VISION - Magnifier (05:17)](https://developer.apple.com/videos/play/wwdc2016/202/?time=317)
This **new iOS 10 feature** allows the device's camera to be used in order to magnify the user environment with many possible functionalities *(steadiness, zoom, color filters...)* whose efficiency is shown in a [live demonstration](https://developer.apple.com/videos/play/wwdc2016/202/?time=344).
</br></br></br>
<a name="SoftwareTTY"></a>
### [HEARING - TTY (06:51)](https://developer.apple.com/videos/play/wwdc2016/202/?time=411)
The typewriter technology that allows to hold text conversations over standard telephone calls for someone with hearing loss is now **available for iOS**.
</br>This **new iOS 10 feature** is a software implementation that prevents from adding any additional TTY hardware while using this technology only with an iOS device. 
</br></br></br>
<a name="EnhancedTypingFeedback"></a>
### [LEARNING - Enhanced typing feedback (07:51)](https://developer.apple.com/videos/play/wwdc2016/202/?time=471)
Besides the improvements for `Speech Selection` and `Speech Screen` in the `Accessibility - Speech` part, an audio typing feedback has also been implemented.
</br>This **new iOS 10 feature** helps people with dyslexia to catch and prevent mistakes in their writings, highlighted by a [live demonstration](https://developer.apple.com/videos/play/wwdc2016/202/?time=496).
</br></br>
<a name="UIAccessibilityProtocol"></a>
### [UIAccessibilityProtocol (14:19)](https://developer.apple.com/videos/play/wwdc2016/202/?time=859)
Reminder on the `UIAccessibility` informal protocol fundamentals that will be used during the presentation. 
</br><img style="max-width: 550px; height: auto;" alt="" src="./images/iOSdev/wwdc16-202-UIAccessibilityProtocol.png" />
</br></br>
<a name="accessibilityElements"></a>
### [accessibilityElements (18:00)](https://developer.apple.com/videos/play/wwdc2016/202/?time=1080)
The implementation and the purpose of this element are explained and introduced inside the demo application. 
</br><img style="max-width: 575px; height: auto;" alt="" src="./images/iOSdev/wwdc16-202-accessibilityElements.png" />
</br></br>
<a name="accessibilityFrameInContainerSpace"></a>
### [accessibilityFrameInContainerSpace (19:02)](https://developer.apple.com/videos/play/wwdc2016/202/?time=1142)
This **new iOS 10 feature** allows the automatic handling of the accessible element coordinates inside its `container`.
</br><img style="max-width: 575px; height: auto;" alt="" src="./images/iOSdev/wwdc16-202-accessibilityFrameInContainerSpace.png" />
</br></br>
<a name="accessibilityCustomRotors"></a>
### [accessibilityCustomRotors (24:19)](https://developer.apple.com/videos/play/wwdc2016/202/?time=1459)
Customed elements can be added to a native `rotor` thanks to this **new iOS 10 feature**.
</br><img style="max-width: 775px; height: auto;" alt="" src="./images/iOSdev/wwdc16-202-accessibilityCustomRotors.png" />
</br>The programming implementation of this feature is detailed in the [development part](./dev-ios.html#custom-rotor).
</br></br>
<a name="tvOS"></a>
### [tvOS header elements (31:20)](https://developer.apple.com/videos/play/wwdc2016/202/?time=1880)
This last section deals with reminders of header elements implementation and purpose inside a VoiceOVer navigation with tvOS.
</br><img style="max-width: 500px; height: auto;" alt="" src="./images/iOSdev/wwdc16-202-tvOS_1.png" />
</br><img style="max-width: 450px; height: auto;" alt="" src="./images/iOSdev/wwdc16-202-tvOS_2.png" />
</br></br>
<!--  This file is part of a11y-guidelines | Our vision of mobile & web accessibility guidelines and best practices, with valid/invalid examples.
 Copyright (C) 2016  Orange SA
 See the Creative Commons Legal Code Attribution-ShareAlike 3.0 Unported License for more details (LICENSE file). -->