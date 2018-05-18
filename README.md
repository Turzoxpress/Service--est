# Service-test
Sending Push Notification to device with Service even the app is killed by force

Starting from android O . You can not call startService.

The startService() method now throws an IllegalStateException if an app targeting Android 8.0 tries to use that method in a situation when it isn't permitted to create background services.

This does not apply to foreground services, which are noticeable to the user. It can run in background with a notification on top. By default, these restrictions only apply to apps that target Android 8.0 (API level 26) or higher. However, users can enable most of these restrictions for any app from the Settings screen, even if the app targets an API level lower than 26. So in case if user enables the restrictions for below API 26 your Service will not work.


So Try to avoid using Service if you can . Make use of WorkManager if it fits the requirements. 
