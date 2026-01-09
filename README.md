# 📲 Try the App (APK Installation)
If you just want to test the GS1-128 scanning logic on your device, you can download the pre-compiled APK.
### (App doesnt work for IOS)
1. Enable "Unknown Sources"
Because this is a custom build and not on the Play Store, Android will block the installation by default.


Go to Settings > Apps > Special app access.

Select Install unknown apps.

Toggle "Allow from this source" for your Browser or File Manager.

2. Install & Scan
Open the downloaded .apk file.

Grant Camera Permissions when prompted.

Point the scanner at a GS1-128 weight label (AI 310n).

# ⚖️ GS1-128 Custom Weight Scanner
 A custom made Android implementation for scanning and parsing GS1-128 barcodes, specifically optimized for weight-based logistics. It extracts weight data from GS1 strings.


# 🚀 Key Features
GS1-128 targeted: Specifically tuned to handle the long, high-density nature of GS1-128 (Code 128) barcodes.

Automatic Weight Extraction: Built-in logic to identify and extract weight values using AI (310n). AI - applicable identifiers!

Custom Scan Overlay: A simple viewfinder optimized for the wide aspect ratio of GS1 labels.

Real-time Feedback: Instant visual confirmation of parsed weight and units (kg).

# 📱 Minimum SDK Requirement
For a modern ZXing implementation on Android:

Minimum SDK: 24 (Android 7.0) is the default for current zxing-android-embedded versions.

Target SDK: 34 or 35 (to meet 2026 Google Play requirements).


# 🛠 Tech Stack
Engine: ZXing (Zebra Crossing) for core decoding.

Environment: Android Studio (Kotlin/gradle).

View Layer: Custom ViewfinderView library for enhanced scanning accuracy.

# 📦 Implementation
To get the best results with GS1-128 in ZXing, I've optimized the scanner to focus on 1D formats and custom widths:

Parsing Logic Example
The scanner identifies the Application Identifier (310n) to determine the decimal point for the weight:

Example Data: (01)90012345678908(3103)000175

Result: AI 3103 indicates 3 decimal places → 0.175 kg.
* 3100 -> 0 decimal
* 3101 -> 1 decimal
* 3102 -> 2 decimal
* 3103 -> 3 decimal

# 🏗 Setup
Clone the repository

Open in Android Studio.

Sync Gradle and run on a physical device (camera required).


# 🤝 Contributing
Found a bug? Feel free to open an issue or submit a pull request!
