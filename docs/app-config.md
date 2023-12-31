<h1>Preferences</h1>

App configuration Preferences are currently required to load the CSV file location through the `edu.nebraska.ImageViewer.dataURL` preferences key. All available keys are shown here:
***
**`edu.nebraska.ImageViewer.dataURL` (required)** <br />
URL of the CSV file containing image information. There is no default option for this key and the App will not function as built without this value loaded. Your CSV file must be available over https.
```xml
<key>edu.nebraska.ImageViewer.dataURL</key>
<string>https://link.to.preferences.csv</string>
```
***
**`edu.nebraska.ImageViewer.dataType`**  <br />
Set this value to "csv" for Google Drive support or for situations where a CSV file does not include the .csv extension in the url.

```xml
<key>edu.nebraska.ImageViewer.dataType</key>
<string>csv</string>
```
***
**`edu.nebraska.ImageViewer.deviceName`** <br />
In tvOS 16, Apple requires an App entitlement for accessing the user-assigned device name instead of the generic device name. Exhibit does not yet have this entitlement and therefore the name of the device will always show as "Apple TV". This preference value allows the setting of device name from MDM.

Jamf Pro and Jamf School both support variables in App Config so you can pass the name of the device to the Apple TV. You may need to check with your MDM provider to see if they support passing variables through App Config.

Jamf Pro: `$DEVICENAME`
Jamf School: `%Name%`
```xml
<key>edu.nebraska.ImageViewer.deviceName</key>
<string>$DEVICENAME</string>
```
***

**`edu.nebraska.ImageViewer.imageTimer`** (optional) <br />
Time (in seconds) of the image timer default. Image display time length is specified in the CSV file but will default to this option if nothing is entered in the file. <br />
```xml
<key>edu.nebraska.ImageViewer.imageTimer</key>
<integer>10</integer>
```
***

**`edu.nebraska.ImageViewer.airplayViewHide`** (optional) <br />
Boolean value set to `false` by default, override with a `true` value to hide the floating AirPlay box. <br />
```xml
<key>edu.nebraska.ImageViewer.airplayViewHide</key>
<true/>
```
***

**`edu.nebraska.ImageViewer.airplayViewHideOnVideo`** (optional) <br />
Boolean value set to `false` by default, override with a `true` value to hide the floating AirPlay box only when a video is shown. <br />
```xml
<key>edu.nebraska.ImageViewer.airplayViewHideOnVideo</key>
<true/>
```
***

**`edu.nebraska.ImageViewer.airplayViewTimer`** (optional) <br />
Time (in seconds) between movements of the AirPlay box. The default time is set to `33` seconds. <br />
```xml
<key>edu.nebraska.ImageViewer.airplayViewTimer</key>
<integer>25</integer>
```
***

**`edu.nebraska.ImageViewer.dataCheckTimer`** (optional) <br />
Time (in seconds) between checks for updates in the CSV file. The default time is set to `180` seconds. <br />
```xml
<key>edu.nebraska.ImageViewer.dataCheckTimer</key>
<integer>180</integer>
```
***

**`edu.nebraska.ImageViewer.defaultBackground`** (optional) <br />
This value can be set to `DefaultBackgroundNoLogo` in order to remove the MDM Image Viewer logo from the default background image. <br />
```xml
<key>edu.nebraska.ImageViewer.defaultBackground</key>
<string>DefaultBackgroundNoLogo</string>
```
***

**`edu.nebraska.ImageViewer.airplayDescription`** (optional) <br />
Change the value of the description within the Airplay box. The default value is: `Wirelessly send what's on your iOS device or computer to this display using AirPlay. Learn more at help.apple.com/appletv.`  <br />
```xml
<key>edu.nebraska.ImageViewer.airplayDescription</key>
<string>Wirelessly send what's on your iOS device or computer to this display using AirPlay. Learn more at help.apple.com/appletv.</string>
```
***

**`edu.nebraska.ImageViewer.airplaySubtitle`** (optional) <br />
Change the value of the subtitle within the Airplay box. The default value is: `CHOOSE THIS APPLE TV`  <br />
```xml
<key>edu.nebraska.ImageViewer.airplayDescription</key>
<string>CHOOSE THIS APPLE TV</string>
```
***

**`edu.nebraska.ImageViewer.airplayViewPositionX`** (optional) <br />
Set the default position of the Airplay box on the 'X' axis. This should be a value between `0` and `1920`. The default value is `1354`.  <br />
```xml
<key>edu.nebraska.ImageViewer.airplayViewPositionX</key>
<integer>1354</integer>
```
***

**`edu.nebraska.ImageViewer.airplayViewPositionY`** (optional) <br />
Set the default position of the Airplay box on the 'Y' axis. This should be a value between `0` and `1080`. The default value is `638`.  <br />
```xml
<key>edu.nebraska.ImageViewer.airplayViewPositionY</key>
<integer>638</integer>
```
***

**`edu.nebraska.ImageViewer.airplayViewMovement`** (optional) <br />
The the movement behavior of the Airplay box. The following options are applicable:  <br />
* `Fade` (Default) - Airiplay box fades out of one location on the screen and into another location.
* `Slide` - Airplay box slides from one location on the screen to another.
* `Inactive` - Airplay box has no movement and is left in the default position. Use with airplayViewPositionX and airplayViewPositionY to set the inactive locaiton on the screen.
```xml
<key>edu.nebraska.ImageViewer.airplayViewMovement</key>
<string>Fade</string>
```
***

**`edu.nebraska.ImageViewer.playVideosInFull`** (optional) <br />
Boolean value set to `false` by default. Videos will follow the "Duration" value set in the playlist file unless overridden with a `true` value in which case, the video will show in its entirety. <br />
```xml
<key>edu.nebraska.ImageViewer.playVideosInFull</key>
<true/>
```
***

**`edu.nebraska.ImageViewer.playVideosWithAudio`** (optional) <br />
Boolean value set to `false` by default, override with a `true` value to allow videos to play their audio. <br />
```xml
<key>edu.nebraska.ImageViewer.playVideosWithAudio</key>
<true/>
```
***
