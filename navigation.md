# Navigation

Basic app with two pages/routes:

```dart
import 'package:flutter/material.dart';
import 'package:english_words/english_words.dart';

void main() => runApp(MyApp());


class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Welcome to Flutter',
      initialRoute: '/',
      routes: <String, WidgetBuilder> {
        '/': (BuildContext context) {
          return HomePage();
        },
        '/signup': (BuildContext context) {
          return SignUpPage();
        }
      }
    );
  }
}

class HomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    // TODO: implement build
    return Scaffold(
      appBar: AppBar(
        title: Text('Startup name generator'),
      ),
      body: Center(
        child: TextButton(
          child: Text("Sign Up"),
          onPressed: () {
            Navigator.pushNamed(context, '/signup');
          }
        )
      )
    );
  }
}


class SignUpPage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
        appBar: AppBar(
          title: Text('Startup Name Generator'),
        ),
        body: Text('sign up')
    );
  }
}
```
