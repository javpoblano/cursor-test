# Android Compose Fingerprint Authentication

A modern Android application built with Jetpack Compose featuring biometric fingerprint authentication and a clean main menu interface.

## Features

- **Biometric Authentication**: Secure fingerprint login using AndroidX Biometric API
- **Modern UI**: Built with Jetpack Compose and Material Design 3
- **Navigation**: Clean navigation between login and main menu screens
- **Responsive Design**: Adapts to different screen sizes and orientations
- **Error Handling**: Comprehensive error handling for authentication failures

## Tech Stack

- **Language**: Kotlin
- **UI Framework**: Jetpack Compose
- **Architecture**: MVVM with Compose Navigation
- **Authentication**: AndroidX Biometric
- **Theme**: Material Design 3
- **Minimum SDK**: Android 8.0 (API level 26)
- **Target SDK**: Android 14 (API level 34)

## Project Structure

```
app/
├── src/main/
│   ├── java/com/example/composefingerprint/
│   │   ├── MainActivity.kt                 # Main activity
│   │   ├── biometric/
│   │   │   └── BiometricManager.kt         # Biometric authentication helper
│   │   ├── navigation/
│   │   │   └── AppNavigation.kt            # Navigation setup
│   │   ├── screens/
│   │   │   ├── LoginScreen.kt              # Login screen with fingerprint
│   │   │   └── MainMenuScreen.kt           # Main menu screen
│   │   └── ui/theme/                       # Theme configuration
│   ├── res/                                # Resources (strings, colors, etc.)
│   └── AndroidManifest.xml                 # App manifest
└── build.gradle                            # App-level build configuration
```

## Setup Instructions

1. **Prerequisites**:
   - Android Studio Arctic Fox or later
   - Android SDK 34
   - Device with fingerprint sensor (for testing)

2. **Configuration**:
   - Update `local.properties` with your Android SDK path
   - Sync the project in Android Studio

3. **Building**:
   ```bash
   ./gradlew assembleDebug
   ```

4. **Running**:
   - Connect an Android device with fingerprint sensor
   - Install and run the app
   - Set up fingerprint authentication on your device if not already done

## Permissions

The app requires the following permissions:
- `USE_BIOMETRIC`: For fingerprint authentication
- `USE_FINGERPRINT`: Legacy fingerprint permission support

## Features Overview

### Login Screen
- Clean, modern interface with fingerprint icon
- Biometric authentication prompt
- Error handling and user feedback
- Fallback message for devices without biometric support

### Main Menu Screen
- Welcome header with user information
- Menu items with icons and descriptions
- Logout functionality
- Material Design 3 styling

### Navigation
- Seamless navigation between screens
- Proper back stack management
- Navigation state preservation

## Dependencies

Key dependencies include:
- `androidx.compose.ui:ui` - Compose UI
- `androidx.compose.material3:material3` - Material Design 3
- `androidx.navigation:navigation-compose` - Navigation for Compose
- `androidx.biometric:biometric` - Biometric authentication
- `androidx.activity:activity-compose` - Activity integration with Compose

## Customization

You can easily customize the app by:
- Modifying colors in `ui/theme/Color.kt`
- Updating strings in `res/values/strings.xml`
- Adding new menu items in `MainMenuScreen.kt`
- Implementing additional authentication methods

## License

This project is created as a template/example and can be used freely for learning and development purposes.
