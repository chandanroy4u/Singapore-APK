# Build the APK without installing Android Studio

This project includes a GitHub Actions workflow that builds the APK in the cloud.

1. Sign in to GitHub and create a new repository (for example `SingaporeLotteriesAndroid`).
2. Upload all files and folders from this project to the repository, including the hidden `.github` folder.
3. Open the repository's **Actions** tab.
4. Select **Build Singapore Lotteries APK** and click **Run workflow** (or push to `main` to trigger a build).
5. Wait for the workflow to finish successfully.
6. Open the completed workflow run and download the `Singapore-Lotteries-APK` artifact.
7. Extract the downloaded artifact ZIP. It contains `app-debug.apk`, which can be installed for testing.

Important: This workflow creates a debug APK for testing, not a signed production release. For wider distribution, use a release APK signed with a private signing key. Never commit a signing key or passwords to the repository.
