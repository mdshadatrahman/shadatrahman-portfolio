+++
title = 'Google Maps Flutter Crash on Android'
date = 2023-10-03T01:37:58+06:00
+++

# Fixing google_maps_flutter Crash on Android

If you've encountered crashes while using the `google_maps_flutter` package on Android, you're not alone. This issue can be quite frustrating, but fortunately, there's a solution. In this guide, I'll walk you through the steps to resolve the problem and get your Google Maps functionality working smoothly on Android.

## The Problem

The `google_maps_flutter` package is a popular choice for integrating Google Maps into your Flutter application. However, some users have reported crashes specifically on Android devices when using this package. These crashes can be caused by various factors, but one common solution involves adding the `google_maps_flutter_android` package.

## The Solution

To fix the `google_maps_flutter` crash on Android, follow these steps:

1. **Add the `google_maps_flutter_android` package**:
   Start by adding the `google_maps_flutter_android` package to your Flutter project. You can find it on [pub.dev](https://pub.dev/packages/google_maps_flutter_android). Add it to your `pubspec.yaml` file under the dependencies section:

   ```yaml
		dependencies:
			google_maps_flutter_android: ^latest_version
	```

	 ```dart
		import 'package:flutter/material.dart';
		import 'package:google_maps_flutter_android/google_maps_flutter_android.dart';

		void main() async {
			if (Platform.isAndroid) {
				await GoogleMapsFlutterAndroid()
					.initializeWithRenderer(AndroidMapRenderer.latest);
			}
			runApp(MyApp());
		}
	 ```
