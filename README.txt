ScanPro Android project (source project, not a prebuilt APK)

This project packages the supplied ScanPro HTML in app/src/main/assets/index.html and opens it with AndroidX WebViewAssetLoader at:
https://appassets.androidplatform.net/assets/index.html

The app includes camera permission handling and WebView file chooser support for the gallery.

Build requirements:
- AndroidIDE or another Android Gradle build environment on Android phone
- Internet connection during first build to download Gradle/Android dependencies
- Android SDK Platform 35 and a compatible JDK (AndroidIDE may manage these)

Import the ScanProAndroid folder as an existing Gradle project in AndroidIDE, allow Gradle sync, then Build > Assemble Debug APK. The debug APK is usually at app/build/outputs/apk/debug/app-debug.apk.

Important limitations:
- This is a source project, not an already compiled APK.
- PDF export in the current HTML loads jsPDF from a CDN, so PDF export needs internet unless the library is bundled locally.
- Please test camera, gallery import, local document save and PDF export before relying on the app.
