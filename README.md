# tanvrit-sdk · commerceapp

> Full commerce application shell with top-level navigation, app initialisation, and platform entry points.

[![Maven](https://img.shields.io/badge/maven.tanvrit.com-1.0.12-blue)](https://maven.tanvrit.com)
![KMP](https://img.shields.io/badge/Kotlin_Multiplatform-7_targets-blueviolet)

## Install

### Option A — Tanvrit Gradle plugin _(recommended)_

```kotlin
// settings.gradle.kts
pluginManagement {
    repositories { maven { url = uri("https://maven.tanvrit.com") } }
}
```

```kotlin
// build.gradle.kts
plugins { id("com.tanvrit.sdk") version "1.0.12" }

tanvrit {
    version = "1.0.12"
    modules = listOf("commerceapp")
}
```

### Option B — Direct dependency

```kotlin
// settings.gradle.kts
dependencyResolutionManagement {
    repositories { maven { url = uri("https://maven.tanvrit.com") } }
}
```

```kotlin
// build.gradle.kts  (KMP)
kotlin {
    sourceSets {
        commonMain.dependencies {
            implementation("com.tanvrit:commerceapp:1.0.12")
        }
    }
}
```

## Targets

| Platform | Artifact |
|----------|----------|
| Android | `commerceapp-android` |
| Iosarm64 | `commerceapp-iosarm64` |
| Iossimulatorarm64 | `commerceapp-iossimulatorarm64` |
| Iosx64 | `commerceapp-iosx64` |
| Jvm | `commerceapp-jvm` |
| Js | `commerceapp-js` |
| Wasm Js | `commerceapp-wasm-js` |

## Quick start

```kotlin
// Initialise the SDK before launching the app
TanvritSDK.init(
    context  = applicationContext,   // Android only
    appId    = "your-app-id",
    apiKey   = "your-api-key",
    baseUrl  = "https://api.tanvrit.com",
)

// Entry point Composable
CommerceApp()
```

## Resources

- **Full SDK source:** [tanvrit/sdk](https://github.com/tanvrit/sdk)
- **All modules:** [maven.tanvrit.com](https://maven.tanvrit.com)
- **Issues:** [tanvrit/sdk/issues](https://github.com/tanvrit/sdk/issues)
