# Web equivalent patterns


## Break

Html:
```html
<br/>
```

Flutter:
```dart
SizedBox(height: 20.0)
```

## Text Alignment

Css:
```css
element {
  text-align: center;
}
```

Flutter:
```dart
Align(
  alignment: Alignment.centerLeft,
  child: Text(
    "Hello world",
    style: TextStyle(fontSize: 20.0),
  ),
),
```

## Fonts

Css:
```css
element {
  font-size: 20px;
  font-weight: bold;
}
```


Flutter:
```dart
Text('hello world', style: FontStyle(fontWeight: FontWeight.bold, fontSize: 20.0));
```

## Padding/margin/height/width/border

Css:
```css
element {
  width: 20px;
  height: 20px;
  padding: 20px;
  margin: 20px;
  border: 1px solid darkblue;
  background: blue;
}
```

Flutter:

```dart
Container(
  width: 20.0,
  height: 20.0,
  padding: EdgeInsets.all(20.0),
  margin: EdgeInsets.all(20.0),
  // color: Colors.blueAccent, // Not required if color is specified in BoxDecoration.
  decoration: BoxDecoration(
      color: Colors.blueAccent, 
      border: Border.all(color: Colors.blueAccent)
  ),
)
```
