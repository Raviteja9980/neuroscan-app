# 🧠 Neuro Scan — Android App

WebView wrapper for the Neuro Scan dashboard.

- **Frontend:** http://alzhem-frontend.s3-website.ap-south-1.amazonaws.com/
- **Backend:**  http://13.232.95.102

---

## 🚀 How to Get Your APK (3 Methods)

---

### ✅ Method 1 — GitHub Actions (Easiest, No Setup)

1. Create a free account at https://github.com
2. Create a **new repository** (name it `neuroscan-app`)
3. Upload all files from this folder to the repo
4. Go to **Actions** tab → select **"Build NeuroScan APK"** → click **"Run workflow"**
5. Wait ~3 minutes → Download `NeuroScan-debug.apk` from the Artifacts section
6. Transfer APK to your phone and install it

> Enable **"Install from unknown sources"** in phone Settings → Security

---

### ✅ Method 2 — Android Studio (Local Build)

1. Download Android Studio: https://developer.android.com/studio
2. Open this folder as a project
3. Click **Build → Build Bundle(s)/APK(s) → Build APK(s)**
4. APK will be at: `app/build/outputs/apk/debug/app-debug.apk`
5. Transfer to phone via USB or Google Drive

---

### ✅ Method 3 — Online Builder (No Install)

Use **Appetize.io** or **AppGyver** to upload and test, or use
**GitHub Codespaces** (free) to build in the cloud:

1. Push this repo to GitHub
2. Open in Codespaces
3. Run: `./gradlew assembleDebug`
4. Download the APK from `app/build/outputs/apk/debug/`

---

## 📱 App Features

- Loads your S3 frontend inside a native Android shell
- Backend URL (`http://13.232.95.102`) injected as `window.BACKEND_URL`
- Pull-to-refresh support
- No internet connection dialog with retry
- Hardware back button navigates within the app
- Branded splash screen with Neuro Scan branding

---

## 🔧 Customization

To change URLs, edit `MainActivity.java`:
```java
private static final String FRONTEND_URL = "http://alzhem-frontend.s3-website.ap-south-1.amazonaws.com/";
private static final String BACKEND_URL  = "http://13.232.95.102";
```
