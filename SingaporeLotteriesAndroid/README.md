# Singapore Lotteries — Android WebView starter project

This Android Studio project wraps `https://singaporelotteries.online/app/` in a native WebView. It includes an Android splash screen, immersive fullscreen mode, Android back navigation, a page-load progress indicator, and a simple main-page error/retry message.

## Build a signed APK

1. Install the latest stable Android Studio and a compatible JDK (Android Studio's bundled JDK is suitable).
2. Open this `SingaporeLotteriesAndroid` folder in Android Studio and allow Gradle sync to finish. Internet is needed to download Gradle and Android dependencies.
3. Test on an Android device or emulator. Confirm login/forms and any site-specific features work in WebView.
4. Select **Build > Generate Signed Bundle / APK > APK**.
5. Create a new keystore in the signing wizard and save it somewhere secure with a backup. Do not share the keystore or passwords. Use the same key for every future update.
6. Choose the `release` build variant and finish. Android Studio will show the generated APK location (typically `app/release/` or `app/build/outputs/apk/release/`).
7. Install and test the signed APK on a separate device before distributing it.

## Publish the APK on your website (not Google Play)

Upload the signed APK to your web hosting, then add a download link on your site, for example:

`<a href="/downloads/singapore-lotteries.apk" download>Download Singapore Lotteries for Android</a>`

Use the actual uploaded filename/path. Users may need to approve installation from their browser/file manager. Direct APK distribution is subject to Android's applicable developer-verification rules and local laws.

## Important notes

- This project has source code only; the APK is not prebuilt or signed because a signing key must be created and protected by you. The project must be built and tested in Android Studio.
- The website must remain online and accessible. This is not an offline version of the site.
- The supplied Singapore Lotteries logo is used for the launcher icon and splash screen. Review the icon on target Android devices before release.
- JavaScript and DOM storage are enabled because many web apps need them. Do not add a JavaScript bridge to native Android unless necessary and carefully secured.
- The wrapper sends non-site links to the Android browser. If the website requires pop-ups, file uploads/downloads, camera, location, or payment integrations, additional implementation and testing may be needed.
- Keep the signing keystore private. If you lose it, updating the installed app with the same package ID may be difficult or impossible.
