DAILY PLAN APP - build an installable APK (no Android Studio needed)

Option A: free cloud build with GitHub (easiest)
1. Create a free account at github.com and make a new repository.
2. Upload ALL files from this folder (keep the .github folder and www folder).
3. Open the repository's "Actions" tab -> "Build APK" -> wait ~5 minutes.
4. Open the finished run -> download "daily-plan-apk" (a zip containing app-debug.apk).
5. Send app-debug.apk to your phone, open it, and allow "install unknown apps" when asked.

Option B: on your computer (needs Node 18+, Java 17, Android Studio/SDK)
  npm install
  npx cap add android
  npx cap sync android
  cd android && ./gradlew assembleDebug
  APK: android/app/build/outputs/apk/debug/app-debug.apk

To change the app, edit www/index.html and rebuild.
