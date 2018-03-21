# Android_Session14_Assignment1
Concepts of Saving data and Permissions

a) What is the difference between Internal Storage & External Storage?
    When building an app that uses the internal storage, the Android OS creates a unique folder, which will only be accessible from the app, so no other app, or even the user, can see what's in the folder.
The external storage is more like a public storage, it's like sdcard, (remote hard drive).
The internal storage should only be used for application data

b) For how long the data resides in the cache?
    Cache is temporary files. One example might be thumbnails for contacts in a social media app. These can be cleared without any major effect — the app can just download them again when it needs to — and if space is low the Android OS may remove cache files itself. Users can manually clear the data but it is not recommended till then data resides in the cache.
    
c) What are the critical Permissions and Normal Permissions? What are the
examples of each?
Normal Permissions:
   When you need to add a new permission, first check if the permission is considered a PROTECTION_NORMAL permission. In Marshmallow, Google has designated certain permissions to be "safe" and called these "Normal Permissions". These are things like ACCESS_NETWORK_STATE, INTERNET, etc. which can't do much harm. Normal permissions are automatically granted at install time and never prompt the user asking for permission.

Important: Normal Permissions must be added to the AndroidManifest:

Example:
<uses-permission android:name="android.permission.INTERNET" />

Critical Permissions:
    critical is unclear and dangerous permissions, such as a camera app that needs camera permission, ask up-front for it. 
    
    Example:
    <uses-permission android:name="android.permission.CAMERA" />
