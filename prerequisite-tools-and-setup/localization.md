---
description: >-
  we will use getx localization system which in the normal case code would look
  something like this
---

# Localization

```dart
class LocalizationService extends Translations {
    @override
    Map<String, Map<String, String>> get keys => {
        'en_US': { 'hello' : 'Hello' },
        'ar_AR': { 'hello' : 'مرحباً' },
    };
}

Text('hello'.tr);
```

but because we have so many words to translate we will separate keys file (strings\_enum.dart) and languages map into different classes so code will become like this

```dart
class LocalizationService extends Translations {
      @override
      Map<String, Map<String, String>> get keys => {
          'en_US': enUs,
          'ar_AR': arAR,
      };
  }
// keys
class Strings {
    static const String hello = 'hello';
}
// english words
const Map<String, String> enUs = {
    Strings.hello : 'Hello',
}
// arabic translate
final Map<String, String> arAR = {
    Strings.hello : 'مرحبا',
}
//result
Text(Strings.hello.tr)
```

and that explain why we have this file structure inside our translation package

```
   └── translations
       ├── ar_Ar
       │   └── ar_ar_translation.dart
       ├── en_US
       │   └── en_us_translation.dart
       ├── localization_service.dart
       └── strings_enum.dart
```
