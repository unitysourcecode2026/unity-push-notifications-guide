# Unity Push Notifications Guide

A practical guide to implementing push notifications in Unity using **Firebase Cloud Messaging (FCM)** for Android and iOS. This repository includes documentation, setup instructions, Unity C# examples, testing tips, and best practices to help you improve player engagement and retention.

---

## Features

- Firebase Cloud Messaging (FCM) integration
- Local Notifications
- Remote Push Notifications
- Android Setup
- iOS Setup
- Unity C# Code Examples
- Notification Permissions
- Testing & Debugging
- Best Practices
- Troubleshooting Guide

---

# Documentation

This repository is organized into individual guides for each topic.

- 📘 [Introduction](docs/introduction.md)
- 🔔 [Local Notifications](docs/local-notifications.md)
- 🌐 [Remote Notifications](docs/remote-notifications.md)
- 🔥 [Firebase Cloud Messaging (FCM)](docs/firebase-cloud-messaging.md)
- 🤖 [Android Setup](docs/android-setup.md)
- 🍎 [iOS Setup](docs/ios-setup.md)
- 💻 [Unity C# Example](docs/unity-csharp-example.md)
- 🔐 [Notification Permissions](docs/notification-permissions.md)
- 🧪 [Testing & Debugging](docs/testing-debugging.md)
- ⭐ [Notification Best Practices](docs/notification-best-practices.md)
- 🛠️ [Troubleshooting](docs/troubleshooting.md)

---

# Notification Architecture

```
Unity Game
      │
      ▼
Firebase SDK
      │
      ▼
Firebase Cloud Messaging
      │
 ┌────┴────┐
 │         │
 ▼         ▼
Android   iPhone
      │
      ▼
Push Notification
      │
      ▼
Player Opens Game
```

---

# What You'll Learn

- Difference between Local and Remote Notifications
- Setting up Firebase Cloud Messaging
- Configuring Android Notifications
- Configuring iOS Notifications
- Requesting Notification Permissions
- Receiving Notifications in Unity
- Scheduling Local Notifications
- Sending Push Notifications from Firebase
- Testing Notifications
- Common Problems and Solutions
- Notification Best Practices for Better Retention

---

# Requirements

- Unity 2021 LTS or later
- Firebase Unity SDK
- Android Studio (Android)
- Xcode (iOS)
- Firebase Project
- Google Play Console (Optional)
- Apple Developer Account (for iOS deployment)

---

# Best Practices

- Ask for notification permission at the right time.
- Avoid sending too many notifications.
- Personalize notification messages whenever possible.
- Schedule notifications based on player activity.
- Test on real Android and iOS devices.
- Use analytics to measure notification performance.

---

## Related Repositories

- [Unity ScriptableObject Examples](https://github.com/unitysourcecode2026/unity-scriptableobject-examples)
- [Unity Save Load System Guide](https://github.com/unitysourcecode2026/unity-save-load-system-guide)
- [Unity Mobile Optimization Guide](https://github.com/unitysourcecode2026/unity-mobile-optimization-guide)
- [Unity Game Projects](https://github.com/unitysourcecode2026/unity-game-projects)

  ---

# Learn More

For detailed Unity tutorials, game development guides, and ready-made Unity source code projects, visit:

**Website:** https://unitysourcecode.net

Related article:

**How to Add Push Notifications to a Unity Mobile Game (Step-by-Step)**

[https://unitysourcecode.net/blog/](https://unitysourcecode.net/blog/add-push-notifications-to-a-unity-mobile-game)

---

# Contributing

Contributions are welcome. Feel free to improve the documentation, fix issues, or add practical Unity examples.

---

# License

This repository is provided for educational purposes. Please review the license before using any included code or documentation.

