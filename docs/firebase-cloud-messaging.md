# Firebase Cloud Messaging (FCM)

Firebase Cloud Messaging (FCM) is Google's official cloud messaging service that enables developers to send push notifications to Android and iOS devices. It is free, reliable, and widely used in Unity mobile game development.

FCM acts as the communication bridge between your Unity game and the player's mobile device, allowing notifications to be delivered even when the game is not running.

---

# What is Firebase Cloud Messaging?

Firebase Cloud Messaging is a cloud-based messaging platform provided by Google.

It allows developers to:

- Send push notifications
- Deliver data messages
- Notify players about live events
- Promote updates
- Re-engage inactive users
- Target specific groups of players

FCM supports both Android and iOS from a single Firebase project.

---

# How FCM Works

The notification delivery process follows these steps.

```
Unity Game
      │
      ▼
Firebase SDK
      │
      ▼
Generate Device Token
      │
      ▼
Firebase Cloud Messaging
      │
      ▼
Android / iPhone
      │
      ▼
Player Receives Notification
```

---

# Why Use Firebase?

Firebase is one of the most popular backend platforms for Unity developers.

Advantages include:

- Free notification service
- Official Google platform
- Android support
- iOS support
- Topic messaging
- Device targeting
- Cloud Functions integration
- Analytics support
- High reliability

---

# Features

Firebase Cloud Messaging provides several powerful features.

- Notification messages
- Data messages
- Topic subscriptions
- Device token targeting
- Scheduled campaigns
- Notification analytics
- Cross-platform delivery

These features make FCM suitable for both indie games and large-scale mobile titles.

---

# Typical Unity Workflow

A standard Unity implementation looks like this.

1. Create a Firebase project.
2. Register your Android application.
3. Register your iOS application.
4. Download the Firebase configuration files.
5. Import the Firebase Unity SDK.
6. Initialize Firebase.
7. Request notification permissions.
8. Obtain the FCM registration token.
9. Send test notifications.
10. Handle notification clicks inside Unity.

---

# Firebase Console

Most notification campaigns are managed through the Firebase Console.

From the console you can:

- Create notification campaigns
- Send test messages
- Target topics
- Target devices
- View delivery reports
- Monitor engagement

For advanced scenarios, notifications can also be sent using the Firebase Admin SDK or Cloud Functions.

---

# Device Registration Token

Each device receives a unique Firebase registration token.

The token is used to identify a specific device.

Example workflow:

```
Player Installs Game
        │
        ▼
Firebase Generates Token
        │
        ▼
Unity Receives Token
        │
        ▼
Server Stores Token
        │
        ▼
Notification Sent
```

Whenever the token changes, your application should update the server.

---

# Notification Types

FCM supports two primary message types.

## Notification Messages

These are automatically displayed by Android and iOS.

Best for:

- Promotions
- Announcements
- Updates
- Daily rewards

---

## Data Messages

These are processed directly by Unity.

Best for:

- Custom gameplay events
- Silent updates
- Background synchronization
- Dynamic game logic

Many developers combine both message types depending on the use case.

---

# Best Practices

For a successful implementation:

- Keep Firebase SDK updated.
- Store registration tokens securely.
- Handle token refresh events.
- Test on physical devices.
- Use topic messaging when possible.
- Send relevant notifications only.
- Monitor notification performance.

---

# Common Mistakes

Avoid these common issues.

- Incorrect Firebase configuration
- Missing google-services.json
- Missing GoogleService-Info.plist
- Forgetting notification permissions
- Ignoring token refresh
- Testing only in Unity Editor
- Using outdated Firebase SDK

Always test notifications on real Android and iOS devices.

---

# Summary

Firebase Cloud Messaging is the foundation of most Unity push notification systems. It provides reliable cross-platform notification delivery, powerful targeting options, and easy integration with Unity.

Understanding FCM is essential before configuring Android and iOS notification settings.

---

## Next Guide

➡ **Android Setup**

Learn how to configure Firebase Cloud Messaging for Android, install the required files, and prepare your Unity project for push notifications.

---

## Related Documentation

- [Introduction](introduction.md)
- [Local Notifications](local-notifications.md)
- [Remote Notifications](remote-notifications.md)
- [Android Setup](android-setup.md)
- [iOS Setup](ios-setup.md)
- [Unity C# Example](unity-csharp-example.md)
