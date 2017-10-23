---
title: TortoisePlink
---

## Introduction

To provide an improved experience to any Git GUI using the command-line tools, this packaging of
TortoiseGit's customized _plink_ provides a simple way to install TortoisePlink without the full
TortoiseGit package.

## Setup

Improved SSH interaction is as simple as downloading and installing TortoisePlink. But a few
things should be checked.

- Ensure that the `SSH`, `GIT_SSH`, `SVN_SSH`, and `CVS_RSH` [environment variables](https://www.digitalcitizen.life/simple-questions-what-are-environment-variables)
  are **not set** for the user or system.
- Ensure that you are running the build of PuTTY that matches that of TortoisePlink if you want to
  use Peagent for you SSH keys.
- Ensure the VCS clients you are using, such as Git, do not have a specific SSH client specified.

## Why Use TortoisePlink

1. **It uses _modal dialogs_ to communicate with the user.** The version of _plink_ provided with
   PuTTY uses text prompts when user interaction is required. Many GUI tools will not function
   correctly when such a prompt is presented.
2. **PuTTY and Plink are the defacto standard for SSH on Windows.** Most VCS tools on Windows will
   work with them out of the box, commerical and open-source.
3. **Supports the Peagent key agent, just like the original.** Since you are probably use to
   loading you keys up into Peagent, using TortoisePlink is just like using PuTTY or the original
   _plink_.
