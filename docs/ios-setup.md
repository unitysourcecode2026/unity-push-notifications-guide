# iOS Setup

This guide explains how to configure Apple Push Notification Service (APNs) and Firebase Cloud Messaging (FCM) for Unity iOS projects. Proper configuration ensures that your Unity game can deliver push notifications to iPhone and iPad users.

---

# Prerequisites

Before starting, make sure you have:

- Unity 2021 LTS or newer
- macOS
- Xcode (latest version)
- Apple Developer Account
- Firebase Project
- Firebase Unity SDK
- Physical iPhone or iPad for testing

Push notifications cannot be fully tested in the Unity Editor.

---

# Step 1: Register Your iOS App

Open the Firebase Console.

1. Select your Firebase project.
2. Click **Add App**.
3. Choose **iOS**.
4. Enter your Bundle Identifier.
5. Register the application.

Example Bundle Identifier:

```
com.company.mygame
```

The Bundle Identifier must exactly match the value used in your Unity project.

---

# Step 2: Download Configuration File

Download:

```
GoogleService-Info.plist
```

Copy it into your Unity project.

Example:

```
Assets/
    GoogleService-Info.plist
```

Firebase automatically reads this configuration when the application starts.

---

# Step 3: Configure Apple Developer Account

Log in to the Apple Developer portal.

Enable:

- Push Notifications
- App ID
- Apple Push Notification Service (APNs)

Generate the required certificates or authentication key.

These credentials allow Firebase to communicate with Apple's notification servers.

---

# Step 4: Configure APNs in Firebase

Open Firebase Console.

Navigate to:

```
Project Settings

↓

Cloud Messaging
```

Upload either:

- APNs Authentication Key (.p8)

or

- APNs Certificate

Once uploaded, Firebase can deliver notifications to iOS devices.

---

# Step 5: Configure Unity

Open:

```
Build Settings

↓

iOS
```

Configure:

- Bundle Identifier
- Target iOS Version
- Architecture
- Signing Team (inside Xcode)

Ensure the Bundle Identifier matches Firebase exactly.

---

# Step 6: Build the Xcode Project

Build your Unity project for iOS.

Open the generated Xcode project.

Inside Xcode enable:

- Push Notifications
- Background Modes
- Remote Notifications

These capabilities are required for receiving push notifications.

---

# Step 7: Request Notification Permission

Unlike Android, iOS always requires user permission before notifications can be displayed.

Request permission at an appropriate moment.

Examples:

- After the tutorial
- After completing Level 1
- Before Daily Rewards

Avoid requesting permission immediately when the game launches.

---

# Step 8: Obtain the Device Token

When Firebase initializes successfully, iOS generates a device token.

Workflow:

```
Unity Game

↓

Firebase SDK

↓

APNs

↓

Device Token

↓

Firebase Registration Token
```

This token allows Firebase to identify the player's device.

---

# Step 9: Send a Test Notification

Open Firebase Console.

Go to:

```
Messaging

↓

Create Notification
```

Send a test notification to your iPhone.

Verify:

- Notification appears.
- App launches correctly.
- Notification data is received.
- Deep links work as expected.

---

# Common Issues

If notifications fail on iOS, check:

- Incorrect Bundle Identifier
- Missing GoogleService-Info.plist
- APNs not configured
- Push Notifications capability disabled
- Background Modes disabled
- Notification permission denied
- Incorrect Apple Developer configuration

Most issues originate from APNs configuration rather than Unity.

---

# Best Practices

To improve reliability:

- Test on physical iPhone devices.
- Keep Firebase SDK updated.
- Keep Xcode updated.
- Handle notification permission carefully.
- Monitor APNs configuration after certificate renewal.
- Use meaningful notification messages.

---

# Android vs iOS

| Android | iOS |
|----------|-----|
| Uses Firebase directly | Uses APNs through Firebase |
| google-services.json | GoogleService-Info.plist |
| Notification Channels | Notification Categories |
| Google Play Services | Apple Push Notification Service |

Although both platforms use Firebase Cloud Messaging, their setup process differs.

---

# Summary

Configuring push notifications on iOS requires Firebase, Apple Push Notification Service (APNs), and the correct Xcode capabilities. Once configured, Unity games can reliably deliver notifications to iPhone and iPad users.

---

## Next Guide

➡ **Unity C# Example**

Learn how to initialize Firebase Messaging, receive notifications, and handle notification events in Unity using C#.

---

## Related Documentation

- [Introduction](introduction.md)
- [Firebase Cloud Messaging](firebase-cloud-messaging.md)
- [Android Setup](android-setup.md)
- [Unity C# Example](unity-csharp-example.md)
- [Testing & Debugging](testing-debugging.md)
