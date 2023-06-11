# Page 1

To build a simple "Hello, World!" web application using Flutter and host it using Firebase, you can follow these steps:

1. Install Flutter: Visit the Flutter website ([https://flutter.dev/](https://flutter.dev/)) and follow the installation instructions for your operating system.
2. Create a new Flutter project: Open your terminal or command prompt and run the following command to create a new Flutter project:
3. Copy codeflutter create hello\_world
4.  Open the project: Navigate to the project directory by running the following command:

    ```bash
    bashCopy codecd hello_world
    ```
5.  Update dependencies: Open the `pubspec.yaml` file in your project and update the `dependencies` section as follows:

    ```yaml
    yamlCopy codedependencies: flutter: sdk: flutter firebase_core: ^1.6.0
    ```

    Save the file and run the following command to download the updated dependencies:

    ```arduino
    arduinoCopy codeflutter pub get
    ```
6. Create a Firebase project: Go to the Firebase Console ([https://console.firebase.google.com/](https://console.firebase.google.com/)) and create a new project.
7. Set up Firebase for Flutter: In the Firebase Console, click on "Add app" and select "Web" as the platform. Follow the instructions to register your app and download the `firebaseConfig` object.
8.  Integrate Firebase in your Flutter app: In your Flutter project, open the `lib/main.dart` file and import the necessary packages:

    ```dart
    dartCopy codeimport 'package:flutter/material.dart'; import 'package:firebase_core/firebase_core.dart';
    ```

    Initialize Firebase in the `main` function:

    ```dart
    dartCopy codevoid main() async { WidgetsFlutterBinding.ensureInitialized(); await Firebase.initializeApp(); runApp(MyApp()); }
    ```
9.  Create the main app widget: In the `lib/main.dart` file, replace the existing code with the following:

    ```dart
    dartCopy codeclass MyApp extends StatelessWidget { @override Widget build(BuildContext context) { return MaterialApp( title: 'Hello, World!', home: Scaffold( appBar: AppBar( title: Text('Hello, World!'), ), body: Center( child: Text('Hello, World!'), ), ), ); } }
    ```
10. Test the app: Run the app on a web emulator or a physical device using the following command:

    ```arduino
    arduinoCopy codeflutter run -d chrome
    ```

    You should see the "Hello, World!" text displayed.
11. Set up Firebase Hosting: Install the Firebase command-line tools by running the following command:

    ```
    Copy codenpm install -g firebase-tools
    ```
12. Initialize Firebase Hosting: In your terminal, navigate to your Flutter project directory and run the following command:

    ```
    Copy codefirebase login
    ```

    Log in with your Firebase account credentials.
13. Initialize Firebase Hosting for your project: Run the following command and select your Firebase project from the list:

    ```csharp
    csharpCopy codefirebase init hosting
    ```
14. Configure Firebase Hosting: When prompted, choose the following options:
    * What do you want to use as your public directory? **build/web**
    * Configure as a single-page app? **Yes**
    * Set up automatic builds and deploys with GitHub? **No**
15. Build your Flutter app for the web: Run the following command to generate the optimized production build:

    ```
    Copy codeflutter build web
    ```
16. Deploy your app to Firebase Hosting: Run the following command to deploy your app:

    ```css
    cssCopy codefirebase deploy --only hosting
    ```

    Firebase will provide you with a hosting URL where you can access your deployed Flutter web app.

That's it! You have successfully built a simple "Hello, World!" web application using Flutter and hosted it using Firebase.
