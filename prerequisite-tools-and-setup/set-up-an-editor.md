# Set up an editor

You can build apps with Flutter using any text editor combined with Flutter’s command-line tools. However, we recommend using one of our editor plugins for an even better experience. These plugins provide you with code completion, syntax highlighting, widget editing assists, run & debug support, and more.

Use the following steps to add an editor plugin for VS Code, Android Studio, IntelliJ, or Emacs. If you want to use a different editor, that’s OK, skip ahead to the [next step: Test drive](https://docs.flutter.dev/get-started/test-drive).

{% tabs %}
{% tab title="Visual Studio Code" %}
## Install VS Code <a href="#install-vs-code" id="install-vs-code"></a>

VS Code is a lightweight editor with complete Flutter app execution and debug support.

* [VS Code](https://code.visualstudio.com/), latest stable version

## Install the Flutter and Dart plugins <a href="#install-the-flutter-and-dart-plugins" id="install-the-flutter-and-dart-plugins"></a>

1. Start VS Code.
2. Invoke **View > Command Palette…**.
3. Type “install”, and select **Extensions: Install Extensions**.
4. Type “flutter” in the extensions search field, select **Flutter** in the list, and click **Install**. This also installs the required Dart plugin.

## Validate your setup with the Flutter Doctor <a href="#validate-your-setup-with-the-flutter-doctor" id="validate-your-setup-with-the-flutter-doctor"></a>

1. Invoke **View > Command Palette…**.
2. Type “doctor”, and select the **Flutter: Run Flutter Doctor**.
3. Review the output in the **OUTPUT** pane for any issues. Make sure to select Flutter from the dropdown in the different Output Options.
{% endtab %}

{% tab title="Android Studio and IntelliJ" %}
### Install Android Studio <a href="#install-android-studio" id="install-android-studio"></a>

Android Studio offers a complete, integrated IDE experience for Flutter.

* [Android Studio](https://developer.android.com/studio), version 2020.3.1 (Arctic Fox) or later

Alternatively, you can also use IntelliJ:

* [IntelliJ IDEA Community](https://www.jetbrains.com/idea/download/), version 2021.2 or later
* [IntelliJ IDEA Ultimate](https://www.jetbrains.com/idea/download/), version 2021.2 or later

### Install the Flutter and Dart plugins <a href="#install-the-flutter-and-dart-plugins-1" id="install-the-flutter-and-dart-plugins-1"></a>

The installation instructions vary by platform.

#### Mac <a href="#mac" id="mac"></a>

Use the following instructions for macos:

1. Start Android Studio.
2. Open plugin preferences (**Preferences > Plugins** as of v3.6.3.0 or later).
3. Select the Flutter plugin and click **Install**.
4. Click **Yes** when prompted to install the Dart plugin.
5. Click **Restart** when prompted.

#### Linux or Windows <a href="#linux-or-windows" id="linux-or-windows"></a>

Use the following instructions for Linux or Windows:

1. Open plugin preferences (**File > Settings > Plugins**).
2. Select **Marketplace**, select the Flutter plugin and click **Install**.
{% endtab %}

{% tab title="Emacs" %}
## Install Emacs <a href="#install-emacs" id="install-emacs"></a>

Emacs is a lightweight editor with support for Flutter and Dart.

* [Emacs](https://www.gnu.org/software/emacs/download.html), latest stable version

## Install the lsp-dart package <a href="#install-the-lsp-dart-package" id="install-the-lsp-dart-package"></a>

For information on how to install and use the package, see the [lsp-dart documentation](https://emacs-lsp.github.io/lsp-dart/).
{% endtab %}
{% endtabs %}
