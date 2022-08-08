# flutter_practice

A new Flutter project.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://docs.flutter.dev/cookbook)

For help getting started with Flutter development, view the
[online documentation](https://docs.flutter.dev/), which offers tutorials,
samples, guidance on mobile development, and a full API reference.

### Dart Example Program:
```void main(){
int myNumber=21;
myNumber=changeNumber(myNumber);
print(myNumber);         
}

int changeNumber(int  oldNumber){
return oldNumber*2;
}
```
### Flutter Setup
```
Install Flutter SDK 

Install android studio with android sdk cmdline-tools component 

Set ENV: 

1) C:\flutter_windows_3.0.5-stable\flutter\bin\ 

2) C:\Program Files\Git\bin\git.exe 

3) C:\Program Files\Git\cmd 

4) C:\WINDOWS\system32 

flutter doctor --android-licenses 

 

*************** 

Flutter create App_Name 

Flutter run 

 

*****to connect in mobile 

Enable developer option on mobile and also enable usb debugging 

Select usb configuration and click option MIDI 

Then check in vsc: flutter devices 

 

Remote connect: 

adb tcpip 5555 

adb connect 192.128.1.3:5555   //ip should be of mobile(see from aboutphone/status)  

 

Shortcut: 

Ctrl+ . (it will suggest the wrapper) 
```
### Flutter TextField example Program
```
import 'package:flutter/material.dart';

const Color darkBlue = Color.fromARGB(255, 18, 32, 47);

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      theme: ThemeData.dark().copyWith(
        scaffoldBackgroundColor: darkBlue,
      ),
      debugShowCheckedModeBanner: false,
      home: Scaffold(
        body: Center(
          child: HelloYou(),
        ),
      ),
    );
  }
}
class HelloYou extends StatefulWidget {
  @override
  _HelloYouState createState()=> _HelloYouState();
}

class _HelloYouState extends State<HelloYou> {
  String name= '';
  final TextEditingController txtName= TextEditingController();
  @override
  Widget build(BuildContext context){
    return Column(
    children: [
      TextField(
      controller: txtName,
      ),
      ElevatedButton(
      child: Text('Say Hello'),
      onPressed: () {
        setState(() {
          name=txtName.text;
        });
      }
      ),
      Text('Hello' +name)
    ],
    );
  }
  
}
```
