# Colors

## Define custom color

You can easily define custom color in **lib/util/colors.dart** file

```dart
class Colour {
  static const secondaryTextColor = Color(0xFF8D8D93);
  static const darkBackgroundColor = Color(0xFF2C2C2E);
  static const darkForgroundColor = Color(0xFF3A3A3C);
  static const starIconColor = Color(0xFFA2845E);
  static const appTintColor = Color(0xFF40CBE0);
  static const headlineTextColor = Color(0xFF00CACF);
  static const violetColor = Color(0xFFA4A3FF);
  static const darkSecondaryColor = Color(0xFF48484A);
  static const greenTintColor = Color(0xFF30D158);
}
```

When you need to use this color first add below import

```dart
import 'package:Biotic/utils/base_import.dart';
```

Then use custom color in your code like this

```dart
Container(
      color: Colour.darkBackgroundColor,
      ...
),
```

## Convert Hex Color String

You can easily use **HexColor** class to convert hex color string to **Color** class

```dart
Container(
      color: HexColor("#FFFF00"),
      ...
),
```

## Customize theme Color

You can also customize color in theme by changing color in **lib/config/datk\_theme\_colors.dart** file
