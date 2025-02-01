# Running Your Ionic Angular Application

This guide will help you run your Ionic Angular application in the browser. All necessary dependencies are already installed in the project's `node_modules`.

## Running the Application

### Install Dependencies

First, install all project dependencies:

```bash
npm install
```

### Start the Development Server

Launch the application in your browser:

```bash
npm run ionic serve
```

This will:

-   Start a local development server
-   Open your default browser at `http://localhost:8100`
-   Enable live reload for development

### Mobile Testing in Browser

To test how your app looks on mobile devices:

1. **Using Browser DevTools**
    - Open Chrome DevTools (F12 or Right Click > Inspect)
    - Click the "Toggle Device Toolbar" button or press (Ctrl+Shift+M)
    - Select a mobile device from the dropdown menu to simulate different screen sizes

## Common Issues

-   **Port Already in Use**

    ```bash
    npm run ionic serve -- --port=8101
    ```

-   **Build Errors**
    Try cleaning your dependencies:
    ```bash
    rm -rf node_modules/
    npm install
    ```
