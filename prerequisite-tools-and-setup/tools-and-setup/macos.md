# macOS

## System requirements <a href="#system-requirements" id="system-requirements"></a>

To install and run Flutter, your development environment must meet these minimum requirements:

* **Operating Systems**: macOS
* **Disk Space**: 2.8 GB (does not include disk space for IDE/tools).
* **Tools**: Flutter uses `git` for installation and upgrade. We recommend installing [Xcode](https://developer.apple.com/xcode/), which includes `git`, but you can also [install `git` separately](https://git-scm.com/download/mac).

&#x20;**Important:** If you’re installing on an [Apple Silicon Mac](https://support.apple.com/en-us/HT211814), you must have the Rosetta translation environment available for [some ancillary tools](https://github.com/flutter/website/pull/7119#issuecomment-1124537969). You can install this manually by running:

_content\_copy_

```
$ sudo softwareupdate --install-rosetta --agree-to-license
```

## Get the Flutter SDK <a href="#get-sdk" id="get-sdk"></a>

1.  Download the following installation bundle to get the latest stable release of the Flutter SDK:

    | Intel                                                                                                                      | Apple Silicon |
    | -------------------------------------------------------------------------------------------------------------------------- | ------------- |
    | [Download](https://storage.googleapis.com/flutter\_infra\_release/releases/stable/macos/flutter\_macos\_3.3.10-stable.zip) | Download      |

    \
    For other release channels, and older builds, see the [SDK releases](https://docs.flutter.dev/development/tools/sdk/releases) page.

    &#x20;**Tip:** To determine whether your Mac uses an Apple silicon processor, refer to [Mac computers with Apple silicon](https://support.apple.com/en-us/HT211814) on apple.com
2.  Extract the file in the desired location, for example:

    _content\_copy_

    ```
    $ cd ~/development
    $ unzip ~/Downloads/flutter_macos_3.3.10-stable.zip
    ```
3.  Add the `flutter` tool to your path:

    _content\_copy_

    ```
    $ export PATH="$PATH:`pwd`/flutter/bin"
    ```

    This command sets your `PATH` variable for the _current_ terminal window only. To permanently add Flutter to your path, see [Update your path](https://docs.flutter.dev/get-started/install/macos#update-your-path).

You are now ready to run Flutter commands!

&#x20;**Note:** To update an existing version of Flutter, see [Upgrading Flutter](https://docs.flutter.dev/development/tools/sdk/upgrading).

## Run flutter doctor <a href="#run-flutter-doctor" id="run-flutter-doctor"></a>

Run the following command to see if there are any dependencies you need to install to complete the setup (for verbose output, add the `-v` flag):

_content\_copy_

```
$ flutter doctor
```

This command checks your environment and displays a report to the terminal window. The Dart SDK is bundled with Flutter; it is not necessary to install Dart separately. Check the output carefully for other software you might need to install or further tasks to perform (shown in **bold** text).

\
