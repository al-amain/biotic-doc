# Imagery

## Add local images

If you want to add your local custom image you need to insert those images in **assets/images/** folder. Then in your code use following to show image

```dart
Image.asset(
    'assets/images/file-name-of-your-image'
),
```

## Add network images

Use below code snippet to load images from url

```dart
import 'package:cached_network_image/cached_network_image.dart';

CachedNetworkImage(
    imageUrl: 'your-image-url-in-string-format',
 ),
```

