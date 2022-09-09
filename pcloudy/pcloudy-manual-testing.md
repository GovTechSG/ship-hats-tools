# Run manual testing


### Prerequisites
To access the [pCloudy web dashboard](https://hats.pcloudy.com), make sure you have the following:
- SHIP VPN
- Internet access and Firefox browser/ Firefox Developer Edition browser, preferably on a non-government issued laptop/ development laptop
- The required proxy configuration will be provided during on-boarding.

As the dashboard can only be accessed via the proxy:
- We strongly recommend the use of Firefox browser as it is tied to browser-level settings. If Chrome is used, it will affect the system-level settings.
- Please note that only pCloudy site will be accessible, all other Internet sites are blocked. Unauthorized access to other websites are being monitored and logged.

>**Notes:**
>- Applicable for users doing manual testing - the account password will expire every year.
>- The current video format provided is in FLV. The pCloudy team is working on making the default video format to be MP4.
>- The devices in pCloudy are not meant to be used to develop functional testing script. Please use emulators/simulators from Android Studio and Xcode for respective OS.
>- When installing an app on an iOS device the app has to be re-signed with the UDID of the device. If you are unable to do the automated resigning, then you can resign manually using the UDID. You can copy the UDID and paste it in your Apple Developer account to resign manually
>- Please raise a service ticket for us to dedicate a Linux elastic agent to your Bamboo plan. The  elastic agent dedicated would have pcloudy-cli and another required packages installed.
>- When developing your functional testing scripts with Robot Framework, please do note the versions of Python and the following packages:  
    >- Appium Server, v1.19
    >- Python, v3.8.5 and above
    >- Robot Framework, v3.2.2 or pabot, v1.10.0
