# Getting Started (Build & Run)

### **Important**

All below steps are must be followed to build and run application

****[**Download Project**](https://codecanyon.net/downloads)****

Download and find the your project folder, use your preferred IDE **(Android Studio / Visual Studio Code / IntelliJ IDEA)** to run the project.

<figure><img src="../.gitbook/assets/build_img1 (1).png" alt=""><figcaption></figcaption></figure>

## **Get Dependencies**

After you loaded project successfully, run the following command in the terminal to install all the dependencies listed in the [`pubspec.yaml`](https://dart.dev/tools/pub/pubspec) file in the project's root directory or just click on Pub get in pubspec.yaml file if you don't want to use command.

```cpp
 flutter pub get 
```

**Important**

All below steps are must be followed to build and run application

<figure><img src="../.gitbook/assets/build_img2 (2).png" alt=""><figcaption></figcaption></figure>

## **Build and Run App**

1. Locate the main Android Studio toolbar.
2. In the target selector, select an Android device for running the app. If none are listed as available, select Tools > Android > AVD Manager and create one there. For details, see [Managing AVDs](https://developer.android.com/studio/run/managing-avds).
3. Click the run icon in the toolbar, or invoke the menu item Run > Run.

<figure><img src="../.gitbook/assets/build_img3 (1).png" alt=""><figcaption></figcaption></figure>

After the app build completes, you’ll see the app on your device.

If you don’t use Android Studio or IntelliJ you can use the command line to run your application using the following command

**Important**

Below step requires flutter path to be set in your Environment variables. See https://flutter.dev/docs/get-started/install/windows

```cpp
flutter run
```

You will see below like screen after you have build your app successfully

<figure><img src="../.gitbook/assets/build_img4 (1).png" alt=""><figcaption></figcaption></figure>

## **Try hot reload**

Flutter offers a fast development cycle with Stateful Hot Reload, the ability to reload the code of a live running app without restarting or losing app state. Make a change to app source, tell your IDE or command-line tool that you want to hot reload, and see the change in your simulator, emulator, or device.

**Important**

Do not stop your app. let your app run.
