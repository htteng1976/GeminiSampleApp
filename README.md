# GeminiSampleApp

A minimal Android app built with **Jetpack Compose** and **Material 3**.

The app currently has a single screen with:
- a top app bar,
- a floating action button (FAB),
- and a simple text body.

## Overview

This repository is a single-module Android project intended as a small sample app.

- Build system: Gradle (Kotlin DSL)
- Language: Kotlin
- UI: Jetpack Compose
- Minimum SDK: 21
- Target/Compile SDK: 34

## Project Structure

```text
GeminiSampleApp/
├── app/
│   ├── build.gradle.kts
│   └── src/
│       ├── main/
│       │   ├── AndroidManifest.xml
│       │   ├── java/com/example/geminisampleapp/MainActivity.kt
│       │   ├── kotlin/org/example/App.kt
│       │   └── res/
│       └── test/kotlin/org/example/AppTest.kt
├── gradle/libs.versions.toml
├── settings.gradle.kts
└── README.md
```

## Main Runtime Flow

1. Launcher activity is declared in `app/src/main/AndroidManifest.xml`.
2. `MainActivity` calls `setContent { MainScreen() }`.
3. `MainScreen()` renders a `Scaffold` with top bar, FAB, and body content.

## Key Files

- `app/src/main/java/com/example/geminisampleapp/MainActivity.kt`
  - Contains `MainActivity`, `MainScreen()`, and preview.
- `app/src/main/AndroidManifest.xml`
  - Defines app metadata and launcher activity.
- `app/build.gradle.kts`
  - Android/Compose configuration and dependencies.
- `gradle/libs.versions.toml`
  - Plugin version catalog.

## Build and Run

### Prerequisites

- Android Studio (latest stable recommended)
- Android SDK for API 34
- JDK compatible with Android Gradle Plugin 8.2.0

### Build (CLI)

```bash
./gradlew assembleDebug
```

### Install to a connected device/emulator

```bash
./gradlew installDebug
```

Or run directly from Android Studio using the **app** run configuration.

## Testing

Run unit tests:

```bash
./gradlew test
```

## Current Notes

- The active Android app code is under:
  - `app/src/main/java/com/example/geminisampleapp/`
- There are leftover Gradle-init sample files under:
  - `app/src/main/kotlin/org/example/`
  - `app/src/test/kotlin/org/example/`

These `org.example` files are scaffold artifacts and are not part of the main Android UI flow.

## Future Improvements

- Introduce package-level structure for UI/features/domain/data.
- Replace scaffold artifact tests with tests targeting actual app behavior.
- Add navigation and feature modules if the app grows.
