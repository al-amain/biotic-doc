# Chrome OS

### &#x20;System requirements <a href="#system-requirements" id="system-requirements"></a>

To install and run Flutter, your development environment must meet these minimum requirements:

* **Operating Systems**: Chrome OS (64-bit) with [Linux (Beta)](https://support.google.com/chromebook/answer/9145439) turned on
* **Disk Space**: 600 MB (does not include disk space for IDE/tools).
* **Tools**: Flutter depends on these command-line tools being available in your environment.
  * `bash`
  * `curl`
  * `git` 2.x
  * `mkdir`
  * `rm`
  * `unzip`
  * `which`
  * `xz-utils`
* **Shared libraries**: Flutter `test` command depends on this library being available in your environment.
  * `libGLU.so.1` - provided by mesa packages such as `libglu1-mesa` on Ubuntu/Debian

### Get the Flutter SDK <a href="#get-sdk" id="get-sdk"></a>

1.  Download the following installation bundle to get the latest stable release of the Flutter SDK:

    [Download](https://storage.googleapis.com/flutter\_infra\_release/releases/stable/linux/flutter\_linux\_3.3.10-stable.tar.xz)

    For other release channels, and older builds, see the [SDK releases](https://docs.flutter.dev/development/tools/sdk/releases) page.
2. In the Files app, drag-and-drop the downloaded file from “Downloads” to “Linux Files” to access Flutter from your Linux container.
3.  Extract the file in the desired location, for example:

    _content\_copy_

    ```
    $ cd ~/development
    $ tar xf ~/Downloads/flutter_linux_3.3.10-stable.tar.xz
    ```

    If you don’t want to install a fixed version of the installation bundle, you can skip steps 1 and 2. Instead, get the source code from the [Flutter repo](https://github.com/flutter/flutter) on GitHub with the following command:

    _content\_copy_

    ```
    $ git clone https://github.com/flutter/flutter.git
    ```

    You can also change branches or tags as needed. For example, to get just the stable version:

    _content\_copy_

    ```
    $ git clone https://github.com/flutter/flutter.git -b stable
    ```
4.  Add the `flutter` tool to your path:

    _content\_copy_

    ```
    $ export PATH="$PATH:`pwd`/flutter/bin"
    ```

    This command sets your `PATH` variable for the _current_ terminal window only. To permanently add Flutter to your path, see [Update your path](https://docs.flutter.dev/get-started/install/chromeos#update-your-path).
5.  Optionally, pre-download development binaries:

    The `flutter` tool downloads platform-specific development binaries as needed. For scenarios where pre-downloading these artifacts is preferable (for example, in hermetic build environments, or with intermittent network availability), iOS and Android binaries can be downloaded ahead of time by running:

    _content\_copy_

    ```
    $ flutter precache
    ```

    For additional download options, see `flutter help precache`.

You are now ready to run Flutter commands!

&#x20;**Note:** To update an existing version of Flutter, see [Upgrading Flutter](https://docs.flutter.dev/development/tools/sdk/upgrading).

#### Run flutter doctor <a href="#run-flutter-doctor" id="run-flutter-doctor"></a>

Run the following command to see if there are any dependencies you need to install to complete the setup (for verbose output, add the `-v` flag):

_content\_copy_

```
$ flutter doctor
```

This command checks your environment and displays a report to the terminal window. The Dart SDK is bundled with Flutter; it is not necessary to install Dart separately. Check the output carefully for other software you might need to install or further tasks to perform (shown in **bold** text).
