# Remote Notifications

Remote notifications are push notifications sent from a server to a user's device through a cloud messaging service. In Unity mobile games, the most common solution is **Firebase Cloud Messaging (FCM)** for Android and iOS.

Unlike local notifications, remote notifications allow you to communicate with players even after the game has been installed, making them an essential tool for live operations, marketing campaigns, and player retention.

---

# What Are Remote Notifications?

Remote notifications are created on a server and delivered to users through Firebase Cloud Messaging.

Common examples include:

- 🎉 New game update available
- 🏆 Weekend tournament starts now
- 🎁 Limited-time reward waiting
- 💎 50% discount on in-game items
- ⚔️ New battle event is live

These notifications require an active internet connection.

---

# How Remote Notifications Work

A typical notification delivery process looks like this.

```
Unity Game
      │
      ▼
Firebase SDK
      │
      ▼
Firebase Cloud Messaging
      │
      ▼
Android / iOS Device
      │
      ▼
Player Receives Notification
```

---

# Why Use Firebase Cloud Messaging?

Firebase Cloud Messaging is Google's official push notification platform.

Benefits include:

- Free to use
- Reliable delivery
- Android support
- iOS support
- Topic messaging
- Device targeting
- Notification analytics
- Easy Unity integration

It is one of the most widely used notification services for Unity developers.

---

# Common Use Cases

Remote notifications are ideal for:

- Game updates
- Live events
- Tournament announcements
- Flash sales
- Seasonal content
- New character releases
- Daily challenges
- Maintenance notifications
- Community announcements

---

# Remote vs Local Notifications

| Remote Notifications | Local Notifications |
|----------------------|---------------------|
| Requires internet | Works offline |
| Sent from Firebase | Scheduled by the app |
| Supports campaigns | Best for reminders |
| Server controlled | Device controlled |
| Dynamic content | Static schedules |

---

# Firebase Components

Implementing remote notifications usually involves:

- Firebase Console
- Firebase Cloud Messaging
- Unity Firebase SDK
- Android Configuration
- Apple Push Notification Service (APNs)
- Device Registration Token

Each component plays an important role in delivering notifications successfully.

---

# Notification Flow

The typical workflow is:

1. Player installs the game.
2. Firebase generates a device token.
3. Unity registers the token.
4. Your server or Firebase Console sends a notification.
5. Firebase delivers the message.
6. The player receives the notification.
7. Opening the notification launches the game.

---

# Best Practices

To improve engagement:

- Send relevant notifications only.
- Segment players based on activity.
- Schedule notifications at appropriate times.
- Personalize messages whenever possible.
- Avoid excessive notifications.
- Monitor notification performance using analytics.

Thoughtful notification strategies help increase retention without frustrating players.

---

# Common Mistakes

Avoid these common problems:

- Forgetting to register the Firebase token
- Missing Android notification channels
- Incorrect APNs configuration
- Sending duplicate notifications
- Ignoring notification permissions
- Testing only in the Unity Editor
- Not handling notification clicks properly

Always test on physical Android and iOS devices.

---

# Summary

Remote notifications enable Unity developers to communicate with players long after installation. Powered by Firebase Cloud Messaging, they are ideal for promoting live events, updates, and special offers while improving player retention and engagement.

---

## Next Guide

➡ **Firebase Cloud Messaging**

Learn how to configure Firebase Cloud Messaging (FCM) for Unity and connect your game to Android and iOS push notification services.

---

## Related Documentation

- [Introduction](introduction.md)
- [Local Notifications](local-notifications.md)
- [Firebase Cloud Messaging](firebase-cloud-messaging.md)
- [Android Setup](android-setup.md)
- [iOS Setup](ios-setup.md)
- [Unity C# Example](unity-csharp-example.md)
