# Ring my Phone for Home Assistant

this automation is intended to interact with HA using the notification service and it allows a mobile phone to ring within automations.
It can be used to find the telephone or to interact with HA by sending sound alarms when it is not possible or it is not convenient to use a graphical interface.

## How it works

the automation awaits a notice from ha with the title _RingMyPhone4HA_ and one of the following text in the body of the message to specify the desired behaviour:
- **Ring**: the phone will ring for almost a minute and a half unless the user stops the automation tapping the proper message. this mode can be used to find the phone or to alert the user for urgent matters. for instance it can be used to implement a simple timer inside HA. By using this mode the volume will grow up by 10% every 11 seconds until it reaches 100%.
- **Single**: the phone will ring only once. This mode can be used to notify any commit action inside HA. You may use this mode to notify that a command was successfull.
- **Cancel**: the behaviour of this mode is equivalent to _Single_ mode but it uses a different sound so it can be used to notify the user in a different way. For instance it can be used to notify that a command was not successful or cancelled.

Any sound is played in the _Alarm Audio Stream_.

## Customizing
to use this automation you should review the sounds file to be played for every mode according to your preferences.

## Authorizations
this automation need for the following authorizations:
- access notifications and Do Not Disturb
- ignore battery optimizations

## Usage

to test the automation you can use the notify service as shown below:

```
service: notify.mobile_app_xxxxxx
data:
  message: Ring
  title: RingMyPhone4HA
```
