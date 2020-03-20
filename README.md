
<div align="center">
<img src="https://raw.githubusercontent.com/ammarahm-ed/react-native-admob-native-ads/master/assets/react-native-admob-native-ads.png" ></img>
</div>
<div align="center">
	<p>
		Simple and highly customizable <b>AdMob Native Ads</b> for react native!
	</p>
</div
<p>
While you might have seen native ads on a react-native application, I have tried to take everything to another level so its really really really easy for you guys to get native ads up and running in a few steps with <b>with styling support</b>
</p>

<div align="center">
<h2> 💫 Features</h2>
</div>
<p align="center">

 1. Native Admob Ads  
 2. Cross Platform (iOS and Android)
 3. Identical Working on Android and iOS
 4. Style your ads as you wish!
 5. No need to manage .xml or .xib layout files to match ad style to app theme!
 6. Adding styles is as simple as adding styles to any other react-native `View`  
 7. AutoRefresh ad
 8. Multiple Ad Sizes
 9. Support Video Ads & Image Ads!

</p>

<div align="center">
<h2>🚀 Try out the example app!</h2>
</div>
To run the example app clone the project

    git clone https://github.com/ammarahm-ed/react-native-admob-native-ads.git
    
   then run ` yarn or npm install` in the example folder and finally to run the example app:
       
   
    react-native run-android

<div align="center">
<h2> 😋 Installation Guide </h2>
</div>

    npm install react-native-actions-sheet --save
or if you use yarn:

    yarn add react-native-actions-sheet

### iOS

**Step 1:** Follow the guide to add  [Google Mobile Ads SDK](https://developers.google.com/admob/ios/quick-start#import_the_mobile_ads_sdk)  to your Xcode project. Also don't forget to update your info.plist file also to add AppID.

**Step 2:** Add .xib files to your main project:

 1. Open **`.xcworkspace`**  file inside the `ios`  folder in your
    project in Xcode.
 2. Select the root folder of your project and right click for the dropdown menu.
 3. Click on **`Add files to YOUR_PROJECT_NAME`**
 4. In select file window, go to **`YOUR_PROJECT/node_modules/react-native-admob-native-ads/ios`**
 5. Select **`GADTMediumTemplateView.xib`** and **`GADTSmallTemplateView.xib`** files and add them to your project. **Make sure copy items if needed is checked and add groups is selected!**
   
### [](https://github.com/sbugert/react-native-admob#android)Android

Add your AdMob App ID to `AndroidManifest.xml`, as described in the  [Google Mobile Ads SDK documentation](https://developers.google.com/admob/android/quick-start#update_your_androidmanifestxml).



<div align="center">
<h2>Usage Example</h2>
</div>
For complete usage, see the example project.

```jsx
import  NativeAdView  from  "react-native-admob-native-ads";

const App = () => {
  let actionSheet;

  return (
    <View
      style={{
        justifyContent: 'center',
        flex: 1,
      }}>
      <NativeAdView
	 adUnitID="ca-app-pub-3940256099942544/3986624511"
	 
	 />
    </View>
  );
};

export default App;


```
<div align="center">
<h1>📃 Reference</h1>
</div>

## Props

#### `adUnitID`
Set Ad Unit ID for Native Advanced Ads that you created on your AdMob account.

| Type | Required | Platform|
| ---- | -------- |------|
| `string` | Yes |All

#

#### `adSize`
Select which size of ad you want to display.

| Type | Required | Default|Platform|
| ---- | --------|---- |------|
| `string` | no |"small"| All|

**Android adSizes:** "small",  "medium" , "large"
**iOS adSizes:** "small" and "medium" only.

#

#### `testDevices`
Set testDevices during testing ads or during development.

| Type | Required |Platform|
| ---- | -------- |------|
| `Array<string>` | no | All|


#

#### `buttonStyle`
style the callToAction button in Native ad according to your app look and feel. 

| Type | Required |Platform|
| ---- | -------- |---|
| `object` | no |All|

The following styles properties are available at the moment.

| Name | Type | Required|
| ---- | -------- |------|
| `backroundColor` | 6 digit hex color string only | Yes |
| `textColor` | 6 digit hex color string only | Yes |
| `borderColor` | 6 digit hex color string only | Yes |
| `borderWidth` | number | Yes |
| `borderRadius` | number | Yes |

**Note:** Currently you will need to set all available properties and give them a valid value. **value can't be null**


#

#### `backgroundStyle`
Style the background of Native Ad View.

| Type | Required |Platform|
| ---- | -------- |---|
| `object` | no |All|

The following styles properties are available at the moment.

| Name | Type | Required|
| ---- | -------- |------|
| `backroundColor` | 6 digit hex color string only | Yes |
| `borderColor` | 6 digit hex color string only | Yes |
| `borderWidth` | number | Yes |
| `borderRadius` | number | Yes |

**Note:** Currently you will need to set all available properties and give them a valid value. **value can't be null**


#

#### `headlineTextColor`
Set color for the heading text of Ad.

| Type | Required | Platform|
| ---- | -------- |------|
| 6 digit hex color string only | no |All

#

#### `descriptionTextColor`
Set color for the description text of Ad.

| Type | Required | Platform|
| ---- | -------- |------|
| 6 digit hex color string only | no |All

#

#### `advertiserTextColor`
Set color for the description text of Ad.

| Type | Required | Platform|
| ---- | -------- |------|
| 6 digit hex color string only | no |All

#

#### `ratingBarColor`
Set color for the description text of Ad.

| Type | Required | Platform|
| ---- | -------- |------|
| 6 digit hex color string only | no |Android Only

#

## Events

All events are available through props.The following event are available on both Android and iOS:

#### `onAdFailedToLoad` 
Called when ad has failed to load and returns reason due to which ad was not loaded.
#### `onAdLoaded`
Called when ad has successfully loaded without any errors.
#### `onAdOpened`
Called when ad is opened.
#### `onAdClosed`
Called when ad is closed.
#### `onAdLeftApplication`
Called when ad is loaded but user has left the application
#### `onAdImpression`
User impression has been recorded
#### `onAdClicked`
User has clicked on the ad.

#

## Find this library useful? ❤️
Support it by joining **stargazers** for this repository. ⭐️ and follow me for my next creations!

### MIT Licensed

