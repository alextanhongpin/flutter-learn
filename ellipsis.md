# Ellipsis


```dart
Text("this is a long text", overflow: TextOverflow.ellipsis);
Text("this is a long text", overflow: TextOverflow.fade, maxLines: 1, softWrap: false);
Text("this is a long text", overflow: TextOverflow.clip, maxLines: 1, softWrap: false);
```

If you are using `Text` inside a `Row`, you can put above `Text` inside `Expanded`:

```dart
Expanded(child: Text())
```
