# TortoisePlink

A standalone packaging of PuTTY's Plink from the Tortoise line of Windows Explorer add-ons.

## Introduction

To provide an improved experience to any Git GUI using the command-line tools, this packaging of
TortoiseGit's customized _plink_ provides a simple way to install TortoisePlink without the full
TortoiseGit package.

## Building

To build this version of TortoisePlink, you will need the following tools:

- Visual Studio 2017 or better, the Community Edition should work.
    - Must include the Visual C++ components required for build Windows desktop applications.
	- Must include the Windows 8.1 SDK.
- WiX, at least 2.9 or better.

Though the project for the EXE and each part of the installer may be build via VisualStudio, the
final part of the installer must be built from the command-line using MSBuild. Simply open a
_Developer Command Prompt_, change to the installation project directory, and call one of the
following:

- `msbuild TortoisePlink-setp.wixproj /p:Configuration=Release` for a release build.
- `msbuild TortoisePlink-setp.wixproj /p:Configuration=Debug` for a debug build.
- `msbuild TortoisePlink-setp.wixproj` for the default configuration, usually _Debug_.

## Troubleshooting

- If your images and icons disappear in VisualStudio after installing WiX, please see [this page for
  a workaround](https://developercommunity.visualstudio.com/content/problem/94502/visual-studio-2017-153-toolbar-icons-are-missing.html).
