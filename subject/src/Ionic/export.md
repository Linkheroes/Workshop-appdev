# Exporting Your Ionic Angular Application

This guide explains how to export your Ionic Angular application to Android and iOS platforms.

## Android Export

To export your application for Android:

1. **Install Android Studio**

    - Download and install [Android Studio](https://developer.android.com/studio)
    - Make sure to install the Android SDK during setup

2. **Build for Android**

    ```bash
    npm run ionic capacitor build android
    ```

    This command will:

    - Add the Android platform if not present
    - Build your application
    - Copy the files to the Android project
    - Open Android Studio

3. **Generate APK**
    - In Android Studio, go to `Build > Build Bundle(s) / APK(s) > Build APK(s)`
    - The APK will be generated in `android/app/build/outputs/apk/debug/`

## iOS Export (macOS Only)

**⚠️ Important: iOS development is only possible on macOS systems with Xcode installed.**

1. **Install Xcode**

    - Download Xcode from the Mac App Store
    - Launch Xcode once to install additional components

2. **Build for iOS**

    ```bash
    npm run ionic capacitor build ios
    ```

    This command will:

    - Add the iOS platform if not present
    - Build your application
    - Copy the files to the iOS project
    - Open Xcode

3. **Generate IPA**
    - In Xcode, select a development team
    - Choose `Product > Archive`
    - Follow the distribution process in the Organizer window

## Common Issues

-   **Android Build Fails**

    -   Make sure Android Studio and SDK are properly installed
    -   Check that JAVA_HOME environment variable is set correctly

-   **iOS Build Fails**
    -   Ensure you're using a Mac
    -   Verify Xcode is up to date
    -   Check that you have a valid Apple Developer account

**Note:** Remember that iOS development and export are exclusively available on macOS systems with Xcode installed.
