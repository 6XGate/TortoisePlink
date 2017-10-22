# Porting TortoisePlink from TortoiseGit

## Porting Instructions

Porting to this project from TortoiseGit is done by:

- Removing all source files from _/src_ and the Visual C++ project.
- In the _Project Common_ property sheet, reset the _Warning Level_ and
  _Disable Specific Warnings_ to the default values.
- Copying the files in TortoiseGit's source at _/src/TortoisePlink_ to the _/src_ of this project.
- Adding the files back to the Visual C++ project.
- Usually repeating most of the steps from the prior port.
- Building and correcting any issues.
- Logging the necessary changes to make a successful build.

## Porting Log from TortoiseGit

### 2017-10-22

- Removed _/src/Windows/MSVC_ directory.
- Set the warning level to zero (all warnings off).
- Disabled 4703 and 4996 warnings.
- Did not include _/src/sshnogss.c_ in the Visual C++ project.
- Resaved _/src/Windows/TortoisePlink.rc_ as UTF-16.
