# SecurePreferencesX

[![Build Status](https://travis-ci.com/drilonrecica/secure-preferencesX.svg?branch=master)](https://travis-ci.com/drilonrecica/secure-preferencesX)
[![API](https://img.shields.io/badge/API-23%2B-brightgreen.svg?style=flat)](https://android-arsenal.com/api?level=23)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?v=103)](https://github.com/ellerbrock/open-source-badges/)

### Secure SharedPreferences wrapper for the new Jetpack Security solution


##### Note: This library is currently available as an alpha library and may be subject to sudden API breaks and changes between versions.

The SecurePreferencesX library is a wrapper around the new Security library, part of Android Jetpack, which provides an implementation of the security best practices related to reading and writing data at rest, as well as key creation and verification.

SecurePreferencesX abstracts the Security library so you only have to once initialize SecurePreferencesX with your app's `packageName` and a `preferenceFileName` and after that you can start storing and retrieving data from the SecurePreferences.

#### How to use the Library:

Initialize the library:
``` kotlin
SecurePreferences.initSecurePreferences(packageName, "SecurePreferencesFileName")
```

Store value in SecurePreferencesX:
``` kotlin
SecurePreferences.storeValue(context, "key", "value")
```

Retrieve value from SecurePreferencesX:
``` kotlin
SecurePreferences.getValue(context, "key", "yourDefaultValue")
```

#### Important Information & Links:

* This library works only from API 23 and upwards

* The creation, storage and handling of the encryption/decryption keys is all handled by the Android Jetpack Security library

* https://developer.android.com/jetpack/androidx/releases/security

* https://developer.android.com/topic/security/data.md