# Notification Permissions

Before your Unity game can display push notifications, players must grant permission on their device. Understanding when and how to request notification permissions is essential for improving opt-in rates while maintaining a positive user experience.

This guide explains how notification permissions work on Android and iOS, along with best practices for requesting them.

---

# Why Notification Permissions Matter

Notification permissions give players control over whether your game can send alerts.

Without permission:

- Push notifications cannot be displayed.
- Player re-engagement becomes more difficult.
- Daily reminders and live event notifications will not reach the user.

Always respect the player's decision and avoid repeatedly asking for permission after it has been denied.

---

# Android Notification Permissions

Recent versions of Android require users to explicitly allow notifications.

Typical workflow:

```
Install Game
      │
      ▼
Launch Game
      │
      ▼
Request Notification Permission
      │
      ▼
Player Chooses
      │
      ├── Allow
      │      │
      │      ▼
      │ Receive Notifications
      │
      └── Deny
             │
             ▼
No Notifications
```

Older Android versions may grant notification access automatically, but your app should still handle permission checks gracefully.

---

# iOS Notification Permissions

On iOS, notification permission has always required user approval.

The workflow is:

```
Launch Game
      │
      ▼
Request Permission
      │
      ▼
iOS Permission Dialog
      │
      ├── Allow
      │
      └── Don't Allow
```

If the player denies permission, they must manually re-enable notifications in the device's Settings app.

---

# When Should You Ask?

Timing has a significant impact on whether players accept notification requests.

Good moments include:

- After completing the tutorial
- After finishing the first level
- Before unlocking daily rewards
- When introducing a feature that benefits from reminders

Avoid requesting permission immediately after the game launches.

---

# Explain the Benefit

Before displaying the system permission dialog, explain why notifications are useful.

For example:

> Enable notifications to receive daily rewards, event reminders, and important game updates.

Providing context helps players make an informed decision.

---

# Respect the Player's Choice

If a player declines notification permission:

- Do not repeatedly show the system dialog.
- Continue providing a great gameplay experience.
- Offer a settings screen where players can learn how to enable notifications later.

Respecting user preferences builds trust.

---

# Best Practices

To improve notification opt-in rates:

- Ask at the right moment.
- Explain the value before requesting permission.
- Keep notification messages relevant.
- Avoid sending excessive notifications.
- Allow players to manage notification preferences in-game.

A thoughtful permission strategy often leads to better long-term engagement.

---

# Common Mistakes

Avoid these common issues:

- Asking for permission immediately on launch
- Requesting permission multiple times
- Sending too many notifications
- Using vague or misleading messages
- Ignoring the player's choice
- Failing to provide notification settings

Poor permission handling can reduce trust and lower engagement.

---

# Testing Permissions

When testing your implementation, verify that:

- Permission requests appear correctly.
- The game behaves properly if permission is denied.
- Notifications are delivered after permission is granted.
- Permission status persists between sessions.
- Settings changes are handled correctly.

Always test on physical Android and iOS devices.

---

# Summary

Notification permissions are a key part of any push notification strategy. Requesting permission at the right time, clearly explaining the benefits, and respecting player choices can improve opt-in rates while creating a better overall experience.

---

## Next Guide

➡ **Testing & Debugging**

Learn how to test push notifications, troubleshoot common issues, and verify your Unity implementation before releasing your game.

---

## Related Documentation

- [Introduction](introduction.md)
- [Android Setup](android-setup.md)
- [iOS Setup](ios-setup.md)
- [Unity C# Example](unity-csharp-example.md)
- [Testing & Debugging](testing-debugging.md)
- [Notification Best Practices](notification-best-practices.md)
