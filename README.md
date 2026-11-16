# Laundry Tracker PWA

A no-login laundry tracking app for dorm students. Built with HTML, CSS, vanilla JavaScript, LocalStorage, a web manifest, and a service worker.

## Important data limitation
This version saves records in **the current browser on the current device**. A Load Code does not let another device retrieve the record. Shared, real-time multi-device tracking requires a backend or cloud database. LocalStorage is not a secure shared database, so do not store sensitive information.

## Run locally
1. Extract `Laundry-Tracker-PWA.zip`.
2. Open the `Laundry-Tracker` folder in Visual Studio Code.
3. Install the Live Server extension if needed.
4. Right-click `index.html` and choose **Open with Live Server**.
5. Use `http://localhost` for PWA service-worker testing. Opening the file directly with `file://` will not enable service workers.

## Deploy with GitHub and Netlify
1. Create a GitHub repository and upload the contents of this folder, preserving `icons/`.
2. In Netlify, choose **Add new site → Import an existing project** and connect the repository.
3. Leave the build command blank and set the publish directory to `.` (the project root).
4. Deploy. Netlify serves the site over HTTPS, which is required for service workers and PWA installation.
5. After changing files, commit and push to GitHub; Netlify will redeploy.

## Install
- **Android:** Open the deployed HTTPS site in Chrome. Use the Install App prompt or browser menu → Install app / Add to Home screen.
- **iPhone/iPad:** Open the site in Safari → Share → Add to Home Screen. Enable Open as Web App if offered → Add.
- **Windows / desktop:** Open the HTTPS site in compatible Chrome or Edge. Use the install icon in the address bar or browser menu → Install app.
- This is an installable **PWA**, not an Android APK.

## Features
- Dashboard statistics and recent activity
- Add loads with generated Load Codes
- Track one matching load by code
- Update status, edit, view, and delete active records
- Completed/cancelled history
- Search and filters
- JSON and CSV export
- Light/dark theme
- Cached application shell and offline fallback

## Testing notes
The source includes client-side validation, persistent LocalStorage, and service-worker caching. Test installation on the actual target browsers/devices after HTTPS deployment. Browser-specific PWA prompts and iOS installation behavior vary.
