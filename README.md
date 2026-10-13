# Survey Data Conversion — Android project

This Android WebView app packages the supplied Survey Data Conversion HTML for Android phones and tablets.

## Build an APK without installing Android Studio (GitHub cloud build)

1. Download and extract `SurveyDataConversionAndroid_Project.zip`.
2. Sign in to GitHub and create a **new private repository**.
3. Upload the *contents* of the extracted folder to the repository root (including the `.github` folder). Commit to `main`.
4. Open the repository's **Actions** tab and select **Build Survey Data Conversion APK**.
5. Press **Run workflow** if it has not started automatically.
6. When the run finishes successfully, open the run, scroll to **Artifacts**, and download `SurveyDataConversion-debug-apk`.
7. Extract the downloaded artifact; it contains `app-debug.apk`. Transfer it to the Android phone/tablet and install it. If prompted, allow installation from that source.

No Android Studio is required on your computer. GitHub performs the build in its cloud environment.

## Included
- Android WebView wrapper and local HTML assets
- Android document picker for file inputs
- Geolocation permission handling
- Export download handling
- GitHub Actions workflow for cloud APK compilation

## Important limitations
- The HTML loads several GIS libraries and map tiles from public CDNs, so those features need internet. The app is not fully offline-map capable.
- Browser local storage is local to the app. Clearing app data or uninstalling the app can remove saved records; export important data.
- The APK has not been compiled or device-tested in this environment. The workflow compiles it in GitHub Actions; test import, chainage, GPS and exports on your devices.
