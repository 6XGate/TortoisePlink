---
title: Build TortoisePlink
permalink: /build/
---

## Requirements

To build this version of TortoisePlink, you will need the following tools:

- Visual Studio 2017 or better, the Community Edition should work.
    - Must include the Visual C++ components required for building Windows desktop applications.
	- Must include the Windows 8.1 SDK.
- WiX, at least 3.10 or better.

## Building

It is best to build from the _Developer Command Prompt_. From command prompt, change into the
directory where the installation project resides.

`cd <working-directory>\TortoisePlink-setup`

Then, using MSBuild; build the platform agnostic installer.

- **For _Release_**;
  > `msbuild TortoisePlink-setp.wixproj /p:Configuration=Release`.
- **For _Debug_**;
  > `msbuild TortoisePlink-setp.wixproj /p:Configuration=Debug`.
- **For the default configuration, using _Debug_**;
  > `msbuild TortoisePlink-setp.wixproj`

Though the project for _TortoisePlink_ and the platform specific installer,
_TortoisePlink.Setup.Base_, may be build via VisualStudio; the platform agnostic installer must be
built from the command-line using MSBuild as shown above.

## Troubleshooting

- If your images and icons disappear in VisualStudio after installing WiX, please see [this page for
  a workaround](https://developercommunity.visualstudio.com/content/problem/94502/visual-studio-2017-153-toolbar-icons-are-missing.html).
