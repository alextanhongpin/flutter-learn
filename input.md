## Input Number

```dart
TextFormField(
  onSaved: (val) => _cardDetails.securityCode = int.parse(val),
  keyboardType: TextInputType.number,
  decoration: InputDecoration(
    labelText: 'Security Code',
    icon: Icon(Icons.lock_outline),
  ),
  maxLength: 4,
),
```

## Dropdown

```dart
DropdownButtonFormField(
  onSaved: (val) => _cardDetails.expiryYear = val.toString(),
  value: expiryYear,
  items: yearsList.map<DropdownMenuItem>(
    (val) {
      return DropdownMenuItem(
        child: Text(val.toString()),
        value: val.toString(),
      );
    },
  ).toList(),
  onChanged: (val) {
    setState(() {
      expiryYear = val.toString();
    });
  },
  decoration: InputDecoration(
    labelText: 'Expiry Year',
    icon: Icon(Icons.calendar_today),
  ),
),
```
