# Create an Ionic Angular Project with a Local Installation of Ionic CLI

This guide explains how to install Ionic as a local dependency and use its executable to create a project with a `tabs` template.

## Prerequisites
- Node.js installed (v14 or higher recommended)
- npm installed (comes with Node.js)

---

## Steps

### 1. Initialize a Node.js Project

1. Create a folder for your project and navigate to it:
   ```bash
   mkdir workshop-appdev && cd workshop-appdev
   ```

2. Initialize the Node.js project:
   ```bash
   npm init -y
   ```
   This generates a `package.json` file.

---

### 2. Install Ionic CLI Locally

1. Install Ionic CLI as a local dependency:
   ```bash
   npm install @ionic/cli
   ```

2. Verify that Ionic CLI is installed locally:
   ```bash
   npx ionic --version
   ```
   If the version is displayed, Ionic is installed locally.

---

### 3. Create a Project with the Local Ionic CLI

1. Use `npx` to run the Ionic executable locally and create a project:
   ```bash
   npx ionic start my-ionic-angular-app tabs --type=angular
   ```

   Explanation:
   - `my-ionic-angular-app`: name of the project.
   - `tabs`: selected project template (tab-based menu).
   - `--type=angular`: framework used (Angular).

2. Respond to any prompts from the Ionic CLI.

3. Once completed, navigate to the generated folder:
   ```bash
   cd my-ionic-angular-app
   ```

---

### 4. Run the Application

1. Install the project dependencies:
   ```bash
   npm install
   ```

2. Start the application:
   ```bash
   npm start
   ```

3. Open your browser at the following address:
   ```
   http://localhost:8100
   ```

You will see your functional Ionic Angular application with the `tabs` template.

---

## Benefits of This Method
- **Isolation**: Keeps different versions of Ionic for each project.
- **No Global Installation**: No need to use `npm install -g` for Ionic CLI.
- **Ease of Use**: With `npx`, you directly use the local executable.

---
