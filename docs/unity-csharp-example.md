# Unity C# Example

After configuring Firebase Cloud Messaging (FCM) for Android and iOS, the next step is integrating it into your Unity project. This guide explains the typical workflow for initializing Firebase, requesting notification permissions, receiving a registration token, and handling incoming notifications.

---

# Overview

A basic notification workflow in Unity looks like this:

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
Request Notification Permission
      │
      ▼
Receive Registration Token
      │
      ▼
Listen for Incoming Messages
      │
      ▼
Handle Notification
```

Each step should complete successfully before moving to the next.

---

# Project Structure

A simple project structure might look like this:

```
Assets/
    Scripts/
        Firebase/
            FirebaseInitializer.cs
            NotificationManager.cs
            NotificationHandler.cs
```

Keeping notification-related scripts together makes maintenance easier.

---

# Initialize Firebase

Initialize Firebase as early as possible during application startup.

Typical initialization flow:

1. Check Firebase dependencies.
2. Initialize Firebase.
3. Enable Firebase Messaging.
4. Register notification callbacks.
5. Request notification permissions if required.

Do not attempt to receive notifications before initialization has completed.

---

# Request Notification Permission

Modern Android and all iOS versions require user permission before notifications can be displayed.

Good times to request permission include:

- After the tutorial
- After the first completed level
- Before enabling daily rewards

Avoid requesting permission immediately after launching the game.

---

# Receive Registration Token

Firebase generates a unique registration token for each device.

Typical workflow:

```
Firebase

↓

Generate Token

↓

Unity Receives Token

↓

Send Token to Server

↓

Ready for Push Notifications
```

Store the token securely if you plan to send notifications from your own backend.

---

# Handle Incoming Notifications

Your Unity application should listen for incoming notification events.

Typical behavior includes:

- Display an in-game message.
- Open a specific screen.
- Grant rewards.
- Navigate to a special event.
- Update player data.

Handling notifications consistently creates a better user experience.

---

# Handle Notification Clicks

Players may tap a notification while:

- The game is closed
- The game is running
- The game is in the background

Your game should detect the notification data and navigate the player to the appropriate content.

Examples include:

- Daily rewards
- Limited-time offers
- Live events
- Shop promotions
- Tournament screens

---

# Organize Your Code

Avoid placing all notification logic inside one script.

A cleaner architecture separates responsibilities.

Example:

```
FirebaseInitializer

↓

NotificationManager

↓

NotificationHandler

↓

Game Systems
```

This approach makes the project easier to test and maintain.

---

# Best Practices

Follow these recommendations:

- Initialize Firebase only once.
- Handle initialization errors gracefully.
- Store registration tokens securely.
- Update tokens when they change.
- Keep notification handling modular.
- Test notification behavior on Android and iOS.
- Remove unused notification listeners.

These practices improve stability and scalability.

---

# Common Mistakes

Avoid these common issues:

- Initializing Firebase multiple times
- Ignoring dependency checks
- Not handling token refresh events
- Requesting permissions too early
- Hardcoding notification logic
- Testing only in the Unity Editor

Always validate your implementation on physical devices.

---

# Testing Your Integration

Before publishing your game, verify that:

- Firebase initializes successfully.
- Notification permission is requested.
- Registration token is generated.
- Test notifications are delivered.
- Notification clicks open the correct screen.
- Background notifications work correctly.

A complete testing checklist helps prevent production issues.

---

# Summary

Integrating Firebase Cloud Messaging into a Unity project involves more than simply receiving notifications. A well-structured implementation includes proper initialization, permission handling, token management, and user-friendly notification processing. Following these practices will make your notification system more reliable and easier to maintain.

---

## Next Guide

➡ **Notification Permissions**

Learn how Android and iOS handle notification permissions and discover the best time to request them for higher opt-in rates.

---

## Related Documentation

- [Introduction](introduction.md)
- [Firebase Cloud Messaging](firebase-cloud-messaging.md)
- [Android Setup](android-setup.md)
- [iOS Setup](ios-setup.md)
- [Notification Permissions](notification-permissions.md)
- [Testing & Debugging](testing-debugging.md)
