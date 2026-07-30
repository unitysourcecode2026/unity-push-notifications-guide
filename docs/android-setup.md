# Android Setup

This guide explains how to configure Android push notifications for a Unity mobile game using Firebase Cloud Messaging (FCM). By the end of this guide, your Unity project will be ready to receive push notifications on Android devices.

---

# Prerequisites

Before you begin, ensure you have:

- Unity 2021 LTS or newer
- Firebase Project
- Firebase Unity SDK
- Android Build Support installed
- Android SDK
- Android device for testing

---

# Step 1: Create a Firebase Project

1. Open the Firebase Console.
2. Create a new project.
3. Enter your project name.
4. Enable Google Analytics (optional).
5. Wait for project creation.

Once the project is ready, you can register your Android application.

---

# Step 2: Register Your Android App

Inside Firebase:

1. Click **Add App**.
2. Choose **Android**.
3. Enter your package name.
4. Register the application.
5. Download the **google-services.json** file.

The package name must exactly match your Unity Android package name.

Example:

```
com.company.mygame
```

---

# Step 3: Add google-services.json

Place the downloaded file inside your Unity project.

```
Assets/
    google-services.json
```

Firebase automatically detects this configuration file during initialization.

---

# Step 4: Import Firebase SDK

Import the required Firebase Unity packages.

Recommended packages include:

- Firebase App
- Firebase Messaging
- External Dependency Manager

After importing, allow the External Dependency Manager to resolve Android dependencies.

---

# Step 5: Configure Unity

Open:

```
File
    Build Settings
        Android
```

Then configure:

- Package Name
- Minimum API Level
- Target API Level
- Internet Permission

Verify that the package name matches the one registered in Firebase.

---

# Step 6: Initialize Firebase

Initialize Firebase when the application starts.

Typical workflow:

```
Game Starts
      │
      ▼
Initialize Firebase
      │
      ▼
Check Dependencies
      │
      ▼
Messaging Ready
```

Initialization should complete before attempting to receive notifications.

---

# Step 7: Request Notification Permission

Recent Android versions may require runtime notification permission.

Always request permission at an appropriate moment rather than immediately on launch.

Good examples:

- After completing the tutorial
- After finishing the first level
- Before enabling daily rewards

---

# Step 8: Obtain the Device Token

When Firebase initializes successfully, it generates a registration token.

The token identifies the player's device.

Typical flow:

```
Firebase
      │
      ▼
Generate Token
      │
      ▼
Unity Receives Token
      │
      ▼
Store Token
```

This token is required for sending remote notifications.

---

# Step 9: Send a Test Notification

Open the Firebase Console.

Navigate to:

```
Messaging
      │
      ▼
Create Notification
```

Send a test notification to your Android device using its registration token.

Verify that:

- The notification appears.
- The game launches correctly.
- Notification data is received.

---

# Common Issues

If notifications are not working, check the following:

- Incorrect package name
- Missing google-services.json
- Firebase SDK not initialized
- Dependency resolution failed
- Notification permission denied
- Device not connected to the internet

Most Android notification issues are caused by configuration errors.

---

# Best Practices

Follow these recommendations:

- Always test on a real device.
- Keep Firebase SDK updated.
- Store device tokens securely.
- Handle token refresh events.
- Send notifications only when useful.
- Avoid notification spam.

These practices improve reliability and player experience.

---

# Summary

Android integration with Firebase Cloud Messaging is straightforward once the project is configured correctly. After importing the Firebase SDK, registering the application, and obtaining a device token, your Unity game is ready to receive push notifications.

---

## Next Guide

➡ **iOS Setup**

Learn how to configure Apple Push Notification Service (APNs) and Firebase Cloud Messaging for Unity iOS projects.

---

## Related Documentation

- [Introduction](introduction.md)
- [Firebase Cloud Messaging](firebase-cloud-messaging.md)
- [iOS Setup](ios-setup.md)
- [Unity C# Example](unity-csharp-example.md)
- [Testing & Debugging](testing-debugging.md)
