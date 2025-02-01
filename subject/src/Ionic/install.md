# Installation for Developing with Ionic using NVM

In this guide, we will prioritize installing NVM (Node Version Manager) and then use it to install the latest version of Node.js.

---

## Installing NVM and Node.js

### macOS and Linux

1. **Install NVM:**

    Open your terminal and run the following command to install NVM:

    ```bash
    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
    ```

    After installation, close and reopen your terminal, or source your profile:

    ```bash
    source ~/.bashrc   # Or ~/.bash_profile, ~/.zshrc depending on your shell
    ```

2. **Verify NVM Installation:**

    Check that NVM is installed correctly by running:

    ```bash
    nvm --version
    ```

3. **Install the Latest Version of Node.js:**

    Once NVM is installed, use it to install Node.js by executing:

    ```bash
    nvm install node
    ```

    This command installs the latest available version of Node.js.

4. **Verify Node.js and NPM Versions:**

    After installation, verify the installed versions:

    ```bash
    node -v
    npm -v
    ```

---

### Windows

For Windows, the preferred method is to use NVM for Windows.

1. **Download NVM for Windows:**

    Visit the [nvm-windows releases page](https://github.com/coreybutler/nvm-windows/releases) and download the latest installer (`nvm-setup.zip`).

2. **Install NVM for Windows:**

    Run the installer and follow the on-screen instructions.

3. **Install the Latest Version of Node.js:**

    Open Command Prompt or PowerShell and execute:

    ```powershell
    nvm install latest
    nvm use latest
    ```

4. **Verify the Installation:**

    Check that Node.js and NPM are installed correctly:

    ```powershell
    node -v
    npm -v
    ```

---

## Additional Resources

-   Official NVM Repository (macOS/Linux): [https://github.com/nvm-sh/nvm](https://github.com/nvm-sh/nvm)
-   NVM for Windows: [https://github.com/coreybutler/nvm-windows](https://github.com/coreybutler/nvm-windows)
-   Official Node.js Documentation: [https://nodejs.org/en/docs/](https://nodejs.org/en/docs/)
