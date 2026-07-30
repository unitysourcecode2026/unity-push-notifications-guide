# Troubleshooting

Even with a correct setup, push notifications may not work as expected due to configuration issues, missing permissions, or platform-specific requirements. This guide helps you identify common problems and provides practical steps to resolve them.

---

# Quick Troubleshooting Checklist

Before investigating a specific issue, verify the following:

- Firebase project is configured correctly.
- Firebase Unity SDK is installed.
- Android or iOS configuration files are present.
- Notification permissions are granted.
- Internet connection is available.
- Firebase initialization completes successfully.
- The application is tested on a physical device.

Most notification problems can be traced back to one of these areas.

---

# Problem: Notifications Never Arrive

## Possible Causes

- Firebase not initialized
- Incorrect package name or Bundle Identifier
- Invalid configuration files
- Notification permission denied
- Device offline
- Invalid registration token

## Solution

- Verify Firebase initialization.
- Confirm package identifiers match Firebase.
- Check notification permissions.
- Generate a new registration token.
- Test using Firebase Console.

---

# Problem: Registration Token Not Generated

## Possible Causes

- Firebase dependency errors
- SDK not imported correctly
- Initialization failed

## Solution

- Resolve Firebase dependencies.
- Confirm Firebase starts without errors.
- Restart the application.
- Test on a physical device.

---

# Problem: Android Notifications Do Not Work

## Check

- `google-services.json` exists.
- Package name matches Firebase.
- Notification permission granted (Android 13+).
- Notification channels created.
- Google Play Services available.

---

# Problem: iOS Notifications Do Not Work

## Check

- `GoogleService-Info.plist` exists.
- Bundle Identifier matches Firebase.
- APNs configured correctly.
- Push Notifications capability enabled.
- Background Modes enabled.
- Notification permission granted.

Most iOS notification issues are related to APNs configuration.

---

# Problem: Notifications Work on Android but Not iPhone

Possible causes include:

- Missing APNs Authentication Key
- Incorrect Apple Developer configuration
- Invalid APNs credentials
- Push capability disabled

Review your Firebase Cloud Messaging and Apple Developer settings.

---

# Problem: Notifications Work on iPhone but Not Android

Verify:

- Android package name
- Firebase configuration
- Google Play Services
- Notification channels
- Runtime notification permission

---

# Problem: Duplicate Notifications

Duplicate notifications are usually caused by:

- Multiple notification listeners
- Sending the same notification twice
- Local and remote notifications triggering together

Review your notification flow to ensure each message is processed only once.

---

# Problem: Notification Opens the Game but Does Nothing

Possible causes:

- Notification data not processed
- Missing deep-link handling
- Navigation logic incomplete

Always validate the notification payload before attempting to navigate to a specific screen.

---

# Problem: Notifications Stop Working After an Update

Check the following:

- Firebase SDK version
- Configuration files
- Registration token refresh
- Android target SDK changes
- iOS capabilities
- Firebase project settings

After major updates, test the complete notification flow again.

---

# Debugging Tips

When investigating notification issues:

- Review Unity Console logs.
- Check Android Logcat.
- Inspect the Xcode Console.
- Verify Firebase initialization messages.
- Confirm registration token generation.
- Test with a fresh installation.
- Test using Firebase Console before testing your own backend.

Logs are often the fastest way to identify configuration problems.

---

# Best Practices

To minimize future issues:

- Keep Firebase SDK updated.
- Test on real Android and iOS devices.
- Monitor token refresh events.
- Verify notification permissions regularly.
- Avoid hardcoding configuration values.
- Test after every major SDK or Unity upgrade.

---

# Frequently Asked Questions

## Can I test notifications in the Unity Editor?

No. Push notifications should be tested on physical Android and iOS devices.

---

## Why did my registration token change?

Firebase may refresh registration tokens for security or platform reasons. Your application should detect changes and update your backend if you store tokens.

---

## Why are notifications delayed?

Delays can occur because of network conditions, device battery optimization, operating system behavior, or notification delivery policies.

---

## Can I send notifications without Firebase?

Yes. Other notification providers exist, but Firebase Cloud Messaging is one of the most popular and widely supported solutions for Unity mobile games.

---

# Summary

Most push notification issues are caused by configuration mismatches, missing permissions, or incomplete platform setup. By following a structured troubleshooting process and testing on real devices, you can quickly identify problems and build a reliable notification system for your Unity game.

---

# Repository Documentation

- [Introduction](introduction.md)
- [Local Notifications](local-notifications.md)
- [Remote Notifications](remote-notifications.md)
- [Firebase Cloud Messaging](firebase-cloud-messaging.md)
- [Android Setup](android-setup.md)
- [iOS Setup](ios-setup.md)
- [Unity C# Example](unity-csharp-example.md)
- [Notification Permissions](notification-permissions.md)
- [Testing & Debugging](testing-debugging.md)
- [Notification Best Practices](notification-best-practices.md)
