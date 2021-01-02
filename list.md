## Horizontal Scroll List

Use `SingleChildScrollView` to avoid complications when nesting in another view (compared to when using `ListView`:

```dart
import 'package:flutter/material.dart';

// Horizontal ListView is hard to nest...
class CountryList extends StatelessWidget {
  final countries = ['Malaysia', 'Singapore', 'Bangkok', 'Thailand', 'Japan', 'Korea', 'China'];

  @override
  Widget build (BuildContext context) {
    return SingleChildScrollView(
        scrollDirection: Axis.horizontal,
        child: Row(
            children: countries.map((String country) => _buildListItem(context, country)).toList()
        )
    );
  }

  Widget _buildListItem(context, String country) {
    return Card(
      child: Column(
        children: [
          FlutterLogo(size: 100.0),
          SizedBox(height: 20.0),

          Text(country),
        ],
      )
    );
  }
}
```
