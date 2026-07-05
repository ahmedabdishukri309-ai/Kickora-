# Kickora Android Build Guide

## Prerequisites

Before building the APK, ensure you have:

1. **Flutter SDK** - Download from https://flutter.dev/docs/get-started/install
2. **Android SDK** - Installed via Android Studio
3. **Java Development Kit (JDK 11+)** - Required for Gradle
4. **Git** - For cloning the repository

## Building the APK

### Step 1: Set Up Flutter (Local Machine Only)

```bash
# Clone the repository
git clone https://github.com/ahmedabdishukri309-ai/Kickora-.git
cd Kickora-

# Get Flutter dependencies
flutter pub get

# Run code generation (if needed)
flutter pub run build_runner build --delete-conflicting-outputs
```

### Step 2: Configure API Key

Create a `.env` file in the project root:
```
FOOTBALL_API_KEY=your_api_key_from_football_data_org
```

Or set as environment variable:
```bash
export FOOTBALL_API_KEY="your_api_key"
```

### Step 3: Build Release APK

```bash
# Build optimized release APK
flutter build apk --release

# Output location:
# build/app/release/app-release.apk
```

### Step 4: Build App Bundle (for Play Store)

```bash
flutter build appbundle --release

# Output location:
# build/app/release/app-release.aab
```

## Installation on Device

### Via APK (Development/Testing)

```bash
flutter install build/app/release/app-release.apk
```

Or manually:

1. Transfer APK to your Android phone
2. Enable "Unknown Sources" in Settings > Security
3. Open file manager and tap the APK
4. Follow installation prompts

### Via Play Store (Production)

1. Create Google Play Developer account ($25)
2. Upload AAB to Play Console
3. Configure store listing
4. Submit for review (1-3 hours)
5. Share store link with users

## Troubleshooting

### Common Issues

**Issue: `flutter: command not found`**
- Add Flutter to PATH: export PATH="$PATH:`pwd`/flutter/bin"

**Issue: `Android SDK not found`**
- Set ANDROID_HOME environment variable
- Install required Android build tools

**Issue: Gradle build fails**
- Clean build: `flutter clean && flutter pub get`
- Clear Gradle cache: `rm -rf ~/.gradle`

**Issue: API key errors**
- Verify `FOOTBALL_API_KEY` environment variable is set
- Check football-data.org API credentials

## File Structure

```
android/
├── app/
│   ├── build.gradle            # App-level build config
│   └── src/main/
│       ├── AndroidManifest.xml # App permissions & metadata
│       ├── java/               # Java source code
│       └── res/                # Resources (drawables, strings, etc.)
├── build.gradle                # Project-level build config
├── gradle.properties           # Gradle configuration
├── settings.gradle             # Gradle settings
└── gradlew                      # Gradle wrapper (Unix)
└── gradlew.bat                 # Gradle wrapper (Windows)
```

## CI/CD Deployment

### GitHub Actions (Optional)

Coming soon: Automated builds on every push to main branch.

## Support

For issues:
1. Check Flutter documentation: https://flutter.dev
2. Open issue on GitHub
3. Review Android build documentation

---

**All Android build files are now configured and ready!** 🚀
