# Android - Onboarding Sample Apps


## Prerequisites

[Build the Android sample apps][build-android] and deploy them to individual
Android devices.

## Running Sample Onboarding Server

The Android *Onboarding Server* (AboutConfOnbServer.apk) provides a sample
Android implementation of an app that uses the Onboarding server, to allow the
device to be onboarded by another device running the Onboarding client.

**NOTE:** The *Onboarding Server* will only work on devices that are capable of
acting as a portable hotspot.

1. On the device to be onboarded, first set up your Wi-Fi hotspot settings.
Under **Settings** > **Wireless & networks**, select **More**, then select
**Tethering & portable hotspot**. By default on some devices, this will be an
open Access Point (AP) named *"AndroidAP"*.

  ![][1.TetheringAndPortableHotspot]

2. Configure your Wi-Fi hotspot *name*, *security type*, and depending on
security type, *password*, by selecting **Set up Wi-Fi hotspot**. Setting
*security type* to *None* or *Open* will not require a password to be set.
  * The hotspot name should include a prefix of *"AJ_"* (e.g.
  *"AJ_AndroidAP"*), as this prefix is used by the Onboarding service framework
  to determine which APs are for AllJoyn devices that support the Onboarding
  service framework.

  ![][2.SetUpWiFiHotspot]

3. Load AboutConfOnbServer.apk, and start app *Onboarding Server*. You should
see Wi-Fi hotspot notification bar icon pop up along with the text "Tethering
or hotspot active". This device is now ready to be onboarded.

  ![][3.StartAppEnableHotspot]


## Running Sample Onboarding Client
The Android *Onboarding Client* provides a sample Android implementation of an
app that uses the Onboarding client, to allow the app to onboard another
device.

1. Load OnboardingSampleClient.apk, and start app *Onboarding Client*.

  ![][1.StartScreen]

2. Press **Scan WiFi networks**.

  ![][2.ScanNetworks]
  ![][3.NetworkList]

3. Select the Wi-Fi hotspot you configured on the device running the
*Onboarding Server*, and enter a password if needed, then press **OK**.

  ![][4.EnterAccessPointPasswordIfNeeded]

4. Press the **Connect to AllJoyn** button, then press **OK** in the popup
dialog - 'realm name' here is not important.

  ![][5.ChooseNetwork]
  ![][6.PressedConnectToAllJoyn]

5. A list of AllJoyn apps will be displayed. Long press on the *Hello* app, 
and select the **Onboarding** option.

  ![][7.DeviceList]
  ![][8.LongPressOnDevice]

6. Enter the Access Point (AP) configuration information for the network that
is being onboarded to.

  ![][9.SelectOnboarding]
  ![][10.EnterAccessPointInfoToOnboardTo]

7. Press **Configure** to configure the device with the AP information.

  ![][11.PressConfigure]

8. Press **Connect** to have the device connect with the configured AP information.

  ![][12.PressConnect]

9. If properly configured, the other device running the *Onboarding Server*
will be onboarded to the AP, after which the Wi-Fi hotspot notification bar
icon disappears and the Wi-Fi icon appears in the notification bar.

  ![][4.OnboardedSuccessfully]

[1.TetheringAndPortableHotspot]: /files/develop/run-sample-apps/android-onboardingserver-sample/1.TetheringAndPortableHotspot.png
[2.SetUpWiFiHotspot]: /files/develop/run-sample-apps/android-onboardingserver-sample/2.SetUpWiFiHotspot.png
[3.StartAppEnableHotspot]: /files/develop/run-sample-apps/android-onboardingserver-sample/3.StartAppEnableHotspot.png
[4.OnboardedSuccessfully]: /files/develop/run-sample-apps/android-onboardingserver-sample/4.OnboardedSuccessfully.png

[1.StartScreen]: /files/develop/run-sample-apps/android-onboardingclient-sample/1.StartScreen.png
[2.ScanNetworks]: /files/develop/run-sample-apps/android-onboardingclient-sample/2.ScanNetworks.png
[3.NetworkList]: /files/develop/run-sample-apps/android-onboardingclient-sample/3.NetworkList.png
[4.EnterAccessPointPasswordIfNeeded]: /files/develop/run-sample-apps/android-onboardingclient-sample/4.EnterAccessPointPasswordIfNeeded.png
[5.ChooseNetwork]: /files/develop/run-sample-apps/android-onboardingclient-sample/5.ChooseNetwork.png
[6.PressedConnectToAllJoyn]: /files/develop/run-sample-apps/android-onboardingclient-sample/6.PressedConnectToAllJoyn.png
[7.DeviceList]: /files/develop/run-sample-apps/android-onboardingclient-sample/7.DeviceList.png
[8.LongPressOnDevice]: /files/develop/run-sample-apps/android-onboardingclient-sample/8.LongPressOnDevice.png
[9.SelectOnboarding]: /files/develop/run-sample-apps/android-onboardingclient-sample/9.SelectOnboarding.png
[10.EnterAccessPointInfoToOnboardTo]: /files/develop/run-sample-apps/android-onboardingclient-sample/10.EnterAccessPointInfoToOnboardTo.png
[11.PressConfigure]: /files/develop/run-sample-apps/android-onboardingclient-sample/11.PressConfigure.png
[12.PressConnect]: /files/develop/run-sample-apps/android-onboardingclient-sample/12.PressConnect.png


[build-android]: /develop/building/android
