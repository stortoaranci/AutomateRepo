# Temporary Device

This automation automatically disables Bluetooth, GPS and NFC devices if they are not used after a certain period of time.
In particular, NFC turns off after a few seconds, Bluetooth goes offline if there are no devices that interact with the phone and finally the GPS turns off if the geolocation is not required by any of the applications identified by the user.

To setup the automation you have to modify the variables according to your needs:
- __foregroundApps__: this is the list of the applications authorized to activate the GPS. If the application that is actual in foreground is not in the list, then the GPS turns off. You have to specify the application in the extended form: _(ie:"com.google.android.apps.maps")_

According to the Automate documentation, mayebe some devices (ie:huawei) show a message when an application tries to disable the Bluetooth connection. For this reason you could try another automation i made for this purpose: __HuaweiBluetoothForceOff__

You may also want to revew the dealy in each child flow to fit the automation on your needs.

## Authorizations
this automation needs for the following authorizations:
- Access screen content and observe your actions
- Modify secure system settings
- Pair Bluetooth devices
- Bluetooth management
- NFC control
- Modify system settings
- Ignore battery optimizations
