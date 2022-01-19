# StoreChecker

This Flutter plugin is useful to find the origin of currently installed apk/ipa.

**Android**: It's very common to have Android applications republished on alternate markets or their APKs made available for download. The plugin detects whether app is installed from local source or Play Store or other stores

**iOS**: Detects whether app is installed from TestFlight Beta or App Store build

# Usage
You can use the StoreChecker to find the origin of apk/ipa. This works both on iOS and Android.
Add this to your package's pubspec.yaml file:
dependencies:
  store_checker: ^0.0.6

```dart
import 'package:store_checker/store_checker.dart';

Source installationSource = await StoreChecker.getSource;

String source = "";
switch (installationSource) {
        case Source.IS_INSTALLED_FROM_PLAY_STORE:
          // Installed from Play Store
          source = "Play Store";
          break;
        case Source.IS_INSTALLED_FROM_LOCAL_SOURCE:
          // Installed using adb commands or side loading or any cloud service
          source = "Local Source";
          break;
        case Source.IS_INSTALLED_FROM_AMAZON_APP_STORE:
          // Installed from Amazon app store
          source = "Amazon Store";
          break;
        case Source.IS_INSTALLED_FROM_HUAWEI_APP_GALLERY:
          // Installed from Amazon app store
          source = "Huawei App Gallery";
          break;
        case Source.IS_INSTALLED_FROM_SAMSUNG_GALAXY_STORE:
          // Installed from Amazon app store
          source = "Samsung Galaxy Store";
          break;
        case Source.IS_INSTALLED_FROM_XIAOMI_GET_APPS:
          // Installed from Amazon app store
          source = "Xiaomi Get Apps";
          break;
        case Source.IS_INSTALLED_FROM_OPPO_APP_MARKET:
          // Installed from Amazon app store
          source = "Oppo App Market";
          break;
        case Source.IS_INSTALLED_FROM_VIVO_APP_STORE:
          // Installed from Amazon app store
          source = "Vivo App Store";
          break;
        case Source.IS_INSTALLED_FROM_OTHER_SOURCE:
          // Installed from other market store
          source = "Other Source";
          break;
        case Source.IS_INSTALLED_FROM_APP_STORE:
          // Installed from app store
          source = "App Store";
          break;
        case Source.IS_INSTALLED_FROM_TEST_FLIGHT:
          // Installed from Test Flight
          source = "Test Flight";
          break;
        case Source.UNKNOWN:
          // Installed from Unknown source
          source = "Unknown Source";
          break;
      }
```

## Issues and feedback

Please file [issues](https://github.com/ravitejaavv/store_checker/issues) to send feedback or report a bug. Thank you!