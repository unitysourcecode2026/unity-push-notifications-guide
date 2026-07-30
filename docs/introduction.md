# Introduction

Push notifications are one of the most effective ways to re-engage players, increase retention, and encourage users to return to a mobile game. Whether you're building a casual puzzle game, an idle game, or a competitive multiplayer title, well-timed notifications can significantly improve player engagement.

This guide explains how to implement push notifications in Unity using **Firebase Cloud Messaging (FCM)** for Android and iOS. It covers the complete setup process, Unity integration, testing, and best practices for delivering notifications that provide value instead of becoming an annoyance.

---

# What Are Push Notifications?

Push notifications are messages sent directly to a user's mobile device, even when the game is not currently open.

Examples include:

- 🎁 Daily rewards are ready to collect.
- ❤️ Your lives have been fully restored.
- 🏆 A new challenge is available.
- 🎉 Limited-time event has started.
- 🎮 Continue where you left off.

Unlike in-game messages, push notifications appear on the device's notification screen and can encourage players to reopen the game.

---

# Types of Notifications

Unity games commonly use two types of notifications.

## Local Notifications

Local notifications are created and scheduled directly by the game.

Examples:

- Daily reward reminder
- Energy refill reminder
- Offline income available
- Construction completed
- Training finished

Local notifications do not require an internet connection after they have been scheduled.

---

## Remote Push Notifications

Remote notifications are sent from a server using Firebase Cloud Messaging (FCM).

Examples:

- New game update available
- Seasonal events
- Flash sales
- Tournament announcements
- Community news

These notifications require an internet connection and are delivered through Firebase.

---

# Why Use Firebase Cloud Messaging?

Firebase Cloud Messaging (FCM) is Google's free notification service that allows developers to send push notifications across Android and iOS devices.

Benefits include:

- Free to use
- Easy Unity integration
- Supports Android and iOS
- Reliable notification delivery
- Topic-based messaging
- Scheduled campaigns
- Analytics support

Because of its reliability and extensive documentation, FCM is one of the most popular notification solutions for Unity mobile games.

---

# Android and iOS Support

This repository covers both major mobile platforms.

## Android

- Firebase Cloud Messaging
- Notification Channels
- Android permissions
- AndroidManifest configuration

## iOS

- Apple Push Notification Service (APNs)
- Firebase integration
- Notification permissions
- Xcode configuration

The overall Unity workflow remains similar, but each platform requires its own setup process.

---

# Why Push Notifications Matter

When used correctly, push notifications can help:

- Increase player retention
- Improve Daily Active Users (DAU)
- Encourage players to complete unfinished sessions
- Promote limited-time events
- Increase in-app purchase opportunities
- Bring inactive players back

The goal is not simply to send more notifications, but to send relevant notifications at the right time.

---

# What You'll Learn

Throughout this repository you'll learn how to:

- Understand local and remote notifications
- Configure Firebase Cloud Messaging
- Set up Android notifications
- Configure iOS notifications
- Request notification permissions
- Schedule local notifications
- Receive remote notifications
- Test notifications on real devices
- Debug common notification issues
- Follow notification best practices

---

# Repository Structure

The documentation is divided into focused guides.

- Local Notifications
- Remote Notifications
- Firebase Cloud Messaging
- Android Setup
- iOS Setup
- Unity C# Examples
- Notification Permissions
- Testing & Debugging
- Notification Best Practices
- Troubleshooting

Each guide covers one topic in detail, making it easier to learn and implement push notifications step by step.

---

# Prerequisites

Before continuing, you should have:

- Unity 2021 LTS or newer
- Basic C# knowledge
- Android Studio (recommended)
- Xcode (for iOS development)
- A Firebase project
- An Android or iOS device for testing

---

# Next Step

Continue with the next guide:

➡ **Local Notifications**

This guide explains how to schedule notifications directly from a Unity game without requiring a remote server or Firebase.

---

## Related Resources

- [Local Notifications](local-notifications.md)
- [Remote Notifications](remote-notifications.md)
- [Firebase Cloud Messaging](firebase-cloud-messaging.md)
- [Android Setup](android-setup.md)
- [iOS Setup](ios-setup.md)

---

**Website**

https://unitysourcecode.net

For more Unity tutorials, game development guides, and ready-made Unity source code projects, visit the website above.
