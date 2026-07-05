# Project Setup Instructions

## Initial Setup (Required First Time Only)

Before building or running the app, you MUST complete this setup:

### 1. Install Flutter

Visit: https://flutter.dev/docs/get-started/install

Choose your operating system:
- **Windows**: Download installer or use Chocolatey
- **macOS**: Use homebrew or download SDK directly
- **Linux**: Use package manager or download SDK directly

### 2. Verify Flutter Installation

```bash
flutter doctor
```

This command checks all dependencies. You should see:
- ✓ Flutter SDK
- ✓ Android toolchain
- ✓ Android Studio / VS Code with Flutter extension
- ✓ Java Development Kit (JDK)

### 3. Clone Repository

```bash
git clone https://github.com/ahmedabdishukri309-ai/Kickora-.git
cd Kickora-
```

### 4. Get Dependencies

```bash
flutter pub get
```

### 5. Get API Key

1. Visit: https://www.football-data.org/
2. Sign up for a free account
3. Get your API key from the dashboard
4. Save it securely (don't commit to Git)

### 6. Set API Key

**Option A: Environment Variable (Recommended)**
```bash
# macOS/Linux
export FOOTBALL_API_KEY="your_api_key_here"

# Windows (PowerShell)
$env:FOOTBALL_API_KEY="your_api_key_here"
```

**Option B: Create .env file** (add to .gitignore)
```
FOOTBALL_API_KEY=your_api_key_here
```

## Running the App

### On Emulator

```bash
flutter emulators
flutter emulators launch <emulator_name>
flutter run
```

### On Real Device

1. Connect Android phone via USB
2. Enable USB Debugging in phone settings
3. Run: `flutter run`

## Building APK

```bash
flutter build apk --release
```

Output: `build/app/release/app-release.apk`

## Next Steps

After initial setup, you can:
- Run on Android device/emulator
- Build release APK
- Submit to Play Store
- Contribute to development

See `ANDROID_BUILD_GUIDE.md` for detailed build instructions.

---

**Questions?** Check the README.md or ANDROID_BUILD_GUIDE.md
