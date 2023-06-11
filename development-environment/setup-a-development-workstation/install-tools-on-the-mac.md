# Install Tools on the Mac

## iTerm2

A terminal application is used both for command-line access to macOS and to log in on the Linux Virtual Machine. The recommended terminal application for is [_**iTerm2**_](https://iterm2.com), although the macOS built-in _**Terminal**_ application can also be used.

1. Download iTerm2 at [https://iterm2.com/downloads.html](https://iterm2.com/downloads.html)
2. Double-click on the downloaded file and follow installation instructions
3. Optionally, you can create a dock shortcut&#x20;
   1. Launch _**iTerm2**_
   2. Right-click the _**iTerm2**_ icon in the dock
   3. Select **`Options->Keep in Dock`**&#x20;

## Homebrew

[_**Homebrew**_](https://brew.sh) is a package manager for macOS that allows users to easily install, manage, and update software packages and utilities from the command line, making it simpler to set up and maintain software on a Mac.

1. Launch _**iTerm2**_
2. At the command prompt, type:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Make sure the follow the installation instructions to ensure that _**Homebrew**_ is added the to the _PATH_.

## Visual Studio Code&#x20;

A code editor is used to edit the source code for all programming languages and text-based structured data files (e.g., json). The code editor is used to edit files both on macOS itself as well as the files on the Virtual Linux Machine.

The recommended code editor is [_**Visual Studio Code**_](https://code.visualstudio.com)_**,**_ a free and open-source code editor developed by [Microsoft](https://www.microsoft.com), widely used by developers for its versatility, extensibility, and powerful features that enhance coding productivity across various programming languages.

1. Download Visual Studio Code at [https://code.visualstudio.com/Download](https://code.visualstudio.com/Download)
2. Move the downloaded file to the _**Applications**_ folder
3. Optionally, you can create a dock shortcut&#x20;
   1. Launch _**Visual Studio Code**_
   2. Right-click the _**Visual Studio Code**_ icon in the dock
   3. Select `Options->Keep in Dock`

## Git

[_**Git**_](https://git-scm.com) is a distributed version control system that enables developers to track changes, collaborate on projects, and efficiently manage code repositories, facilitating seamless code management and team collaboration.

1. Launch _**iTerm2**_
2. At the command prompt, type:

```bash
brew install git
```

## **GitLab Workflow Extension for Visual Studo Code**

The _**GitLab Workflow Extension for Visual Studio Code**_ is a tool that integrates GitLab's features into the code editor, providing developers with convenient access to GitLab repositories, issue tracking, CI/CD pipelines, and other collaborative functionalities directly within the development environment.

1. From within _**Visual Studio Code**_, go to `Settings -> Extensions`
2. Search for "Gitlab Workflow" and click on "Install".
3. In the _**Gitlab Workflow Extension**_ details page, follow the instructions to set up your access token(s)

## **Directories for Projects and Tools**&#x20;

The development directory is used to store project files as well as some development tools installed at the user level (e.g., _**Flutter**_).&#x20;

1. Launch _**iTerm2**_
2. At the command prompt, type:

```bash
mkdir ~/dev
mkdir ~/dev/tools
```

## Flutter

Install minimal or full Xcode

* Download the latest version of flutter at [https://docs.flutter.dev/get-started/install/macos](https://docs.flutter.dev/get-started/install/macos)

```bash
xcode-select --install
```

Install Flutter

```bash
cd ~/dev
unzip ~/Downloads/<flutter-filename>.zip
```

Add Flutter executables to the PATH by adding the following lines to `~/.bash_profile`

```bash
PATH="$PATH:/Users/<username>/dev/flutter/bin"
export PATH
```

To verify that the installation was successful, log out, re-log in and type

```bash
flutter doctor
```

## Flutter Extension for Visual Studio Code&#x20;

1. Start VS Code.
2. Invoke **View > Command Palette…**.
3. Type “install”, and select **Extensions: Install Extensions**.
4. Type “flutter” in the extensions search field, select **Flutter** in the list, and click **Install**. This also installs the required Dart plugin.
