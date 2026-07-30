# Local Notifications

Local notifications are notifications that are scheduled directly from your Unity application. Unlike remote push notifications, they do not require an internet connection or a backend server once they have been scheduled.

They are commonly used to remind players to return to the game after a certain period or when an in-game event has completed.

---

# What Are Local Notifications?

A local notification is created and managed entirely on the user's device.

For example:

- 🎁 Your daily reward is ready.
- ❤️ Your energy has been restored.
- 🏗️ Your building has finished upgrading.
- 🪙 Your offline rewards are waiting.
- 🎮 Continue your adventure.

Because these notifications are generated locally, they continue to work even if the device is offline.

---

# Benefits of Local Notifications

Local notifications offer several advantages for Unity developers.

- No internet connection required
- No backend server required
- Easy to implement
- Low maintenance
- Improves player retention
- Works on both Android and iOS

They are ideal for casual, idle, simulation, and puzzle games.

---

# Common Use Cases

Local notifications can be used for:

- Daily login rewards
- Energy refill reminders
- Idle game income collection
- Construction completion
- Crafting completion
- Tournament reminders
- Daily missions
- Limited-time events

The goal is to encourage players to return without becoming intrusive.

---

# Unity Notification Package

Unity provides the **Mobile Notifications** package for scheduling local notifications.

It supports:

- Android Notifications
- iOS Notifications
- Scheduled notifications
- Repeating notifications
- Custom notification icons
- Notification channels

You can install it through the Unity Package Manager.

---

# Basic Workflow

A typical local notification workflow looks like this:

```
Player Opens Game
        │
        ▼
Schedule Notification
        │
        ▼
Game Closes
        │
        ▼
Notification Appears
        │
        ▼
Player Returns
```

---

# Best Practices

Follow these recommendations when using local notifications.

- Only send useful reminders.
- Avoid sending too many notifications.
- Respect user preferences.
- Schedule notifications based on gameplay.
- Test notifications on real devices.
- Give players the option to disable notifications.

---

# Common Mistakes

Avoid these common issues.

- Sending notifications every hour
- Generic notification messages
- Ignoring time zones
- Forgetting notification permissions
- Scheduling duplicate notifications
- Not cancelling outdated notifications

Poor notification practices often lead users to disable notifications entirely.

---

# Local vs Remote Notifications

| Local Notifications | Remote Notifications |
|---------------------|----------------------|
| No internet required | Internet required |
| No backend server | Backend server required |
| Scheduled by the app | Sent from Firebase |
| Simple implementation | More advanced setup |
| Best for reminders | Best for live events |

---

# Summary

Local notifications are one of the easiest ways to improve player engagement in Unity games. They require minimal setup, work offline, and are perfect for reminding players about rewards, completed tasks, or daily activities.

When used responsibly, local notifications can significantly increase player retention without requiring a complex backend infrastructure.

---

## Next Guide

➡ **Remote Notifications**

Learn how Firebase Cloud Messaging (FCM) delivers notifications from the cloud to Android and iOS devices.

---

## Related Documentation

- [Introduction](introduction.md)
- [Remote Notifications](remote-notifications.md)
- [Firebase Cloud Messaging](firebase-cloud-messaging.md)
- [Android Setup](android-setup.md)
- [iOS Setup](ios-setup.md)
