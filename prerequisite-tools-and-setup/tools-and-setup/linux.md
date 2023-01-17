# Linux

## System requirements <a href="#system-requirements" id="system-requirements"></a>

To install and run Flutter, your development environment must meet these minimum requirements:

* **Operating Systems**: Linux (64-bit)
* **Disk Space**: 600 MB (does not include disk space for IDE/tools).
* **Tools**: Flutter depends on these command-line tools being available in your environment.
  * `bash`
  * `curl`
  * `file`
  * `git` 2.x
  * `mkdir`
  * `rm`
  * `unzip`
  * `which`
  * `xz-utils`
  * `zip`
* **Shared libraries**: Flutter `test` command depends on this library being available in your environment.
  * `libGLU.so.1` - provided by mesa packages such as `libglu1-mesa` on Ubuntu/Debian and `mesa-libGLU` on Fedora.

## Get the Flutter SDK <a href="#get-sdk" id="get-sdk"></a>

On Linux, you have two ways you can install Flutter.

#### Install Flutter using snapd <a href="#install-flutter-using-snapd" id="install-flutter-using-snapd"></a>

The easiest way to install Flutter on Linux is by using snapd. For more information, see [Installing snapd](https://snapcraft.io/docs/installing-snapd).

Once you have snapd, you can [install Flutter using the Snap Store](https://snapcraft.io/flutter), or at the command line:

_content\_copy_

```
$ sudo snap install flutter --classic
```

&#x20;**Note:** Once the snap is installed, you can use the following command to display your Flutter SDK path:

_content\_copy_

```
  $ flutter sdk-path
```

## Install Flutter manually <a href="#install-flutter-manually" id="install-flutter-manually"></a>

If you don’t have `snapd`, or can’t use it, you can install Flutter using the following steps.

1.  Download the following installation bundle to get the latest stable release of the Flutter SDK:

    [Download](https://storage.googleapis.com/flutter\_infra\_release/releases/stable/linux/flutter\_linux\_3.3.10-stable.tar.xz)

    For other release channels, and older builds, see the [SDK releases](https://docs.flutter.dev/development/tools/sdk/releases) page.
2.  Extract the file in the desired location, for example:

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
3.  Add the `flutter` tool to your path:

    _content\_copy_

    ```
    $ export PATH="$PATH:`pwd`/flutter/bin"
    ```

    This command sets your `PATH` variable for the _current_ terminal window only. To permanently add Flutter to your path, see [Update your path](https://docs.flutter.dev/get-started/install/linux#update-your-path).
4.  Optionally, pre-download development binaries:

    The `flutter` tool downloads platform-specific development binaries as needed. For scenarios where pre-downloading these artifacts is preferable (for example, in hermetic build environments, or with intermittent network availability), iOS and Android binaries can be downloaded ahead of time by running:

    _content\_copy_

    ```
    $ flutter precache
    ```

    For additional download options, see `flutter help precache`.

You are now ready to run Flutter commands!

&#x20;**Note:** To update an existing version of Flutter, see [Upgrading Flutter](https://docs.flutter.dev/development/tools/sdk/upgrading).

## Run flutter doctor <a href="#run-flutter-doctor" id="run-flutter-doctor"></a>

Run the following command to see if there are any dependencies you need to install to complete the setup (for verbose output, add the `-v` flag):

_content\_copy_

```
$ flutter doctor
```

This command checks your environment and displays a report to the terminal window. The Dart SDK is bundled with Flutter; it is not necessary to install Dart separately. Check the output carefully for other software you might need to install or further tasks to perform (shown in **bold** text).
