# How to Create a New Xcode Project Using the GUI

This guide will walk you through creating a new Xcode project using the graphical user interface (GUI).

## Steps to Create a New Project

1. **Open Xcode**
   - Launch Xcode from your Applications folder or using Spotlight Search.

2. **Start a New Project**
   - On the welcome screen, click `Create a new Xcode project`.  
     If you don't see the welcome screen, go to `File > New > Project` in the menu bar.

3. **Select a Template**
   - Choose a blank app from the list of available templates and make sure you have IOS selected.

4. **Configure Your Project**
   - Fill in the following details:
     - **Product Name**: The name of your app or project.
     - **Team**: Select your Apple Developer account (if applicable).
     - **Organization Name**: Your name or your organization’s name.
     - **Organization Identifier**: A unique identifier, usually in reverse domain name format (e.g., `com.example`).
     - **Bundle Identifier**: Auto-generated based on the product and organization name.
     - **Language**: Choose Swift or Objective-C.
     - **Interface**: Select SwiftUI
     - **Life Cycle**: Choose SwiftUI App.
     - **Include Tests**: No test.
   - Click `Next`.

5. **Choose a Location to Save the Project**
   - Select a directory to save your project files.
   - Optionally, check `Create Git repository on my Mac` to initialize version control.
   - Click `Create`.

---

## Tips

- **Run Your Project**: Click the `Run` button (a play icon) in the toolbar to build and launch your app in the simulator.
- **Switch Targets**: Use the scheme selector in the toolbar to switch between devices or targets.
- **Use Version Control**: If you checked the Git option, you can start tracking changes immediately using Xcode’s source control features.

---

You’re now ready to start building your application in Xcode! For additional resources, visit [Apple’s Developer Documentation](https://developer.apple.com/documentation/).
