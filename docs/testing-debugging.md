# Testing & Debugging

Testing push notifications is an essential step before publishing your Unity mobile game. A notification system that works in the Unity Editor may still fail on real devices due to configuration issues, permissions, or platform-specific requirements.

This guide covers a practical checklist for testing and troubleshooting Firebase Cloud Messaging (FCM) integration on Android and iOS.

---

# Why Testing Matters

Push notifications involve multiple services working together:

- Unity
- Firebase SDK
- Firebase Cloud Messaging (FCM)
- Android or iOS operating system
- Internet connection
- Device notification settings

A problem in any one of these components can prevent notifications from being delivered.

---

# Testing Checklist

Before releasing your game, verify the following:

- Firebase initializes successfully.
- Dependencies are resolved.
- Notification permissions are granted.
- Device registration token is generated.
- Test notifications are delivered.
- Notification tap opens the correct screen.
- Background notifications work correctly.
- Foreground notifications are handled properly.

Testing each step individually makes it easier to identify issues.

---

# Android Testing

For Android devices, check:

- Correct package name
- Valid `google-services.json`
- Firebase SDK imported correctly
- Google Play Services available
- Notification permission granted (Android 13+)
- Internet connection active

Also verify that notification channels are configured correctly.

---

# iOS Testing

For iPhone and iPad devices, confirm:

- Correct Bundle Identifier
- Valid `GoogleService-Info.plist`
- APNs configured
- Push Notifications capability enabled
- Background Modes enabled
- Notification permission granted

Always test on a physical device, as push notifications are not fully supported in the iOS Simulator.

---

# Verify Device Registration Token

Every device should receive a unique Firebase registration token.

Typical workflow:

```
Game Launch

↓

Firebase Initialize

↓

Registration Token Generated

↓

Token Available

↓

Ready for Notifications
```

If no token is generated, review your Firebase configuration and initialization process.

---

# Send a Test Notification

Use the Firebase Console to send a notification to a registered device.

Verify that:

- The notification is delivered.
- The notification title and message display correctly.
- Tapping the notification opens the game.
- Any associated data is processed correctly.

Testing with real devices provides the most reliable results.

---

# Common Issues

The following problems are frequently encountered during setup:

| Issue | Possible Cause |
|-------|----------------|
| No notification received | Missing permission or incorrect Firebase setup |
| Token not generated | Firebase failed to initialize |
| App opens but data missing | Notification payload not handled correctly |
| Android only works | APNs configuration incomplete |
| iOS only works | Android configuration incorrect |
| Duplicate notifications | Multiple listeners registered |

Work through one issue at a time rather than changing several settings simultaneously.

---

# Debugging Tips

When troubleshooting:

- Confirm Firebase initialization completed successfully.
- Verify configuration files are present.
- Check device internet connectivity.
- Review Unity Console logs.
- Inspect Android Logcat or the Xcode Console.
- Test with a newly generated registration token.
- Update to the latest supported Firebase SDK.

Detailed logs often reveal the root cause more quickly than repeated trial and error.

---

# Best Practices

To keep your notification system reliable:

- Test on multiple devices.
- Test different Android versions.
- Test different iOS versions.
- Test foreground and background scenarios.
- Verify behavior after app updates.
- Monitor notification delivery after release.

Routine testing helps prevent issues that only appear in production.

---

# Before Publishing

Complete this final checklist:

- Firebase configured correctly
- Android configuration verified
- iOS configuration verified
- Notification permissions tested
- Registration token confirmed
- Test notifications successful
- Notification click behavior verified
- No duplicate notifications
- No Console errors

Completing these checks reduces the risk of notification failures after launch.

---

# Summary

Testing and debugging are essential parts of implementing push notifications in Unity. By validating each step—from Firebase initialization to notification delivery—you can identify issues early and provide players with a reliable notification experience across Android and iOS devices.

---

## Next Guide

➡ **Notification Best Practices**

Learn how to design effective notification strategies that improve player engagement without overwhelming users.

---

## Related Documentation

- [Introduction](introduction.md)
- [Firebase Cloud Messaging](firebase-cloud-messaging.md)
- [Android Setup](android-setup.md)
- [iOS Setup](ios-setup.md)
- [Notification Permissions](notification-permissions.md)
- [Notification Best Practices](notification-best-practices.md)
- [Troubleshooting](troubleshooting.md)
