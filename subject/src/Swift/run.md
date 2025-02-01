# Running Your iOS Application

This guide will help you run your iOS application using Xcode and the iOS Simulator with a free Apple Developer account.

## Using the iOS Simulator

1. **Open Your Project in Xcode**

    - Launch Xcode
    - Open your project

2. **Select a Simulator**

    - At the top of Xcode, you'll see a dropdown menu next to your project name
    - Click it to select your target device (e.g., "iPhone 16", "iPhone SE", etc.)
    - The simulator will use iOS versions that are compatible with your Xcode version

3. **Run the Application**
    - Click the "Play" button (▶️) in the top-left corner
    - Or use the keyboard shortcut: `Cmd + R`
    - Xcode will build your project and launch the simulator

## Limitations of Free Apple Developer Account

With a free Apple Developer account, you have some limitations:

-   Cannot publish apps to the App Store
-   Cannot test on physical devices
-   Limited access to certain iOS capabilities
-   Apps will expire after 7 days when installed on the simulator

## Tips for Testing

-   Test your app on different iPhone models in the simulator
-   Test both light and dark modes
-   Test different screen orientations
-   Use the simulator's features to simulate different conditions:
    -   Location changes
    -   Network conditions
    -   Different system settings

## Common Issues

If you encounter build errors:

1. Clean the build folder: `Xcode > Product > Clean Build Folder`
2. Clean the derived data: `Xcode > Product > Clean Build Folder`
3. Restart Xcode

**Note:** The simulator provides most features needed for development, but some features (like Push Notifications) require a paid Apple Developer account and a physical device for testing.
