FIXWORX ANDROID APP — SOURCE PROJECT

This is an Android Studio project for the FixWorx quotation app. It wraps the offline quotation/invoice maker in an Android app shell, keeps browser storage on the device, and connects the Print / Save PDF and Share buttons to Android.

IMPORTANT: This ZIP is the Android source project, not a compiled APK. A signed APK must be built with Android Studio (or another Android build service). This chat environment cannot compile/sign Android APKs.

BUILD THE APK
1. On a Windows/Mac/Linux computer, install Android Studio.
2. Extract this ZIP.
3. In Android Studio choose Open, then select the extracted FixWorxAndroid folder.
4. Allow Gradle sync and install the Android SDK Platform 35 if prompted.
5. Choose Build > Build Bundle(s) / APK(s) > Build APK(s).
6. Android Studio will show a notification with a link to the APK (usually app/build/outputs/apk/debug/app-debug.apk).
7. Copy that APK to your Samsung phone and tap it to install. If Android asks, allow installation from that source.

APP FEATURES
- Quotation and invoice modes
- Customer and job details
- Line items with description, quantity, unit (each/metre/hour/etc.) and unit price
- Automatic subtotal, discount, VAT and grand total
- Save/reopen documents in the app on that device
- Android print dialog, including Save as PDF
- Share a document summary
- Offline operation after installation

NOTES
- The app starts with VAT 15% selected; choose 0% if you are not VAT registered. Only charge VAT if registered.
- Data is stored locally on the phone and is not synced or backed up automatically. Export important quotes as PDFs.
- This is a first working build; test PDF output and saved documents before relying on it for business records.


BUILD APK USING ONLY YOUR SAMSUNG PHONE (CLOUD BUILD)
This project includes a GitHub Actions workflow at .github/workflows/build-apk.yml. GitHub's cloud computer builds the APK; you do not need Android Studio on your phone.

1. In Chrome, open github.com and create/sign in to a GitHub account.
2. Create a NEW PUBLIC repository named FixWorx (public repositories allow GitHub Actions use on free accounts; do not upload customer data or private information).
3. Extract this ZIP using Samsung My Files. In the GitHub repository, use Add file > Upload files and upload the CONTENTS of the FixWorxAndroid folder, including the hidden .github folder. If your phone's file picker hides .github, use the GitHub website's Add file > Create new file to create .github/workflows/build-apk.yml and paste the workflow from this project's same file.
4. Commit the files to the main branch. The workflow should start automatically. Alternatively open the Actions tab, select "Build FixWorx APK", tap Run workflow.
5. When the run finishes successfully, open it, find Artifacts, and download FixWorx-debug-apk.zip.
6. In My Files > Downloads, extract that ZIP. Tap app-debug.apk to install. If Android blocks it, allow Chrome or My Files to install unknown apps only for this installation, then install.
7. This is a debug APK for personal testing, not a Play Store release. Keep the GitHub repository private only if your GitHub plan permits Actions for private repositories; otherwise use a public repo but do not include personal/customer data.

The APK is built in GitHub's cloud. The downloaded artifact is a ZIP containing the APK; extract it before installing.
