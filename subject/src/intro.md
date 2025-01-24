# Workshop - AppDev

Welcome to the "AppDev" workshop! This guide provides the necessary instructions to install Node.js on different operating systems. Node.js is a crucial platform for modern application development.

## Prerequisites
Before starting, ensure you have administrator access to your system to install software.

---

## Installing Node.js

### Windows
1. Visit the official Node.js website: [https://nodejs.org/](https://nodejs.org/).
2. Click on the "Windows Installer" button to download the installer (.msi file).
3. Run the installer and follow the instructions:
    - Accept the terms of the license agreement.
    - Choose an installation location.
    - Enable the option "Automatically install the necessary tools" (optional but recommended).
4. After installation, open a command prompt (Cmd or PowerShell) and verify the installed version:
    ```
    node -v
    npm -v
    ```

### Ubuntu
1. Update the package list:
    ```bash
    sudo apt update
    sudo apt upgrade
    ```
2. Install Node.js via the "NodeSource" package manager:
    ```bash
    curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -
    sudo apt install -y nodejs
    ```
3. Verify the installed version:
    ```bash
    node -v
    npm -v
    ```

### Fedora
1. Add the official NodeSource repository:
    ```bash
    curl -fsSL https://rpm.nodesource.com/setup_20.x | sudo bash -
    ```
2. Install Node.js:
    ```bash
    sudo dnf install -y nodejs
    ```
3. Verify the installed version:
    ```bash
    node -v
    npm -v
    ```

### MacOS
1. Install Homebrew if not already installed:
    ```bash
    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
    ```
2. Install Node.js with Homebrew:
    ```bash
    brew install node
    ```
3. Verify the installed version:
    ```bash
    node -v
    npm -v
    ```

---

## Additional Resources
- Official Node.js Documentation: [https://nodejs.org/en/docs/](https://nodejs.org/en/docs/)
- Node.js Version Manager (NVM): [https://github.com/nvm-sh/nvm](https://github.com/nvm-sh/nvm)
