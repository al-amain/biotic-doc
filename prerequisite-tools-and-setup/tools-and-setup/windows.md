# Windows

## System requirements <a href="#system-requirements" id="system-requirements"></a>

To install and run Flutter, your development environment must meet these minimum requirements:

* **Operating Systems**: Windows 10 or later (64-bit), x86-64 based.
* **Disk Space**: 1.64 GB (does not include disk space for IDE/tools).
* **Tools**: Flutter depends on these tools being available in your environment.
  * [Windows PowerShell 5.0](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-windows-powershell) or newer (this is pre-installed with Windows 10)
  *   [Git for Windows](https://git-scm.com/download/win) 2.x, with the **Use Git from the Windows Command Prompt** option.

      If Git for Windows is already installed, make sure you can run `git` commands from the command prompt or PowerShell.

## Get the Flutter SDK <a href="#get-the-flutter-sdk" id="get-the-flutter-sdk"></a>

1.  Download the following installation bundle to get the latest stable release of the Flutter SDK:

    [Download](https://storage.googleapis.com/flutter\_infra\_release/releases/stable/windows/flutter\_windows\_3.3.10-stable.zip)

    For other release channels, and older builds, see the [SDK releases](https://docs.flutter.dev/development/tools/sdk/releases) page.
2. Extract the zip file and place the contained `flutter` in the desired installation location for the Flutter SDK (for example, `C:\src\flutter`).

If you don’t want to install a fixed version of the installation bundle, you can skip steps 1 and 2. Instead, get the source code from the [Flutter repo](https://github.com/flutter/flutter) on GitHub, and change branches or tags as needed. For example:

_content\_copy_

```
C:\src>git clone https://github.com/flutter/flutter.git -b stable
```

You are now ready to run Flutter commands in the Flutter Console.

## Update your path <a href="#update-your-path" id="update-your-path"></a>

If you wish to run Flutter commands in the regular Windows console, take these steps to add Flutter to the `PATH` environment variable:

* From the Start search bar, enter ‘env’ and select **Edit environment variables for your account**.
* Under **User variables** check if there is an entry called **Path**:
  * If the entry exists, append the full path to `flutter\bin` using `;` as a separator from existing values.
  * If the entry doesn’t exist, create a new user variable named `Path` with the full path to `flutter\bin` as its value.

You have to close and reopen any existing console windows for these changes to take effect.

&#x20;**Note:** As of Flutter’s 1.19.0 dev release, the Flutter SDK contains the `dart` command alongside the `flutter` command so that you can more easily run Dart command-line programs. Downloading the Flutter SDK also downloads the compatible version of Dart, but if you’ve downloaded the Dart SDK separately, make sure that the Flutter version of `dart` is first in your path, as the two versions might not be compatible. The following command tells you whether the `flutter` and `dart` commands originate from the same `bin` directory and are therefore compatible.

_content\_copy_

```
  C:\>where flutter dart
  C:\path-to-flutter-sdk\bin\flutter
  C:\path-to-flutter-sdk\bin\flutter.bat
  C:\path-to-dart-sdk\bin\dart.exe        :: this should go after `C:\path-to-flutter-sdk\bin\` commands
  C:\path-to-flutter-sdk\bin\dart
  C:\path-to-flutter-sdk\bin\dart.bat
```

As shown above, the command `dart` from the Flutter SDK doesn’t come first. Update your path to use commands from `C:\path-to-flutter-sdk\bin\` before commands from `C:\path-to-dart-sdk\bin\` (in this case). After restarting your shell for the change to take effect, running the `where` command again should show that the `flutter` and `dart` commands from the same directory now come first.

_content\_copy_

```
  C:\>where flutter dart
  C:\dev\src\flutter\bin\flutter
  C:\dev\src\flutter\bin\flutter.bat
  C:\dev\src\flutter\bin\dart
  C:\dev\src\flutter\bin\dart.bat
  C:\dev\src\dart-sdk\bin\dart.exe
```

However, if you are using `PowerShell`, in it `where` is an alias of `Where-Object` command, so you need to use `where.exe` instead.

_content\_copy_

```
  PS C:\> where.exe flutter dart
```

To learn more about the `dart` command, run `dart -h` from the command line, or see the [dart tool](https://dart.dev/tools/dart-vm) page.

#### Run `flutter doctor` <a href="#run-flutter-doctor" id="run-flutter-doctor"></a>

From a console window that has the Flutter directory in the path (see above), run the following command to see if there are any platform dependencies you need to complete the setup:

_content\_copy_

```
C:\src\flutter>flutter doctor
```

\
