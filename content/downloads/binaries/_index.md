---
title: "Binary releases"
date: 2025-03-31
aliases:
  - 26 # old site url was /downloads/26
draft: false
---
Please select a setup package depending on your platform:

  * [Windows XP / Vista / 7 / 8.x / 10](#imagesoswindows48pnglogo-microsoft-windows)
  * [Linux 32 and 64-bit](#imagesoslinux48pnglogo-linux-32-and-64-bit)
  * [Mac OS X](#imagesosapple48pnglogo-mac-os-x)

**NOTE**: For older OS'es use older releases. There are releases for many OS version and platforms on the [Sourceforge.net](https://sourceforge.net/projects/codeblocks/files/Binaries) page.

**NOTE**: There are also more recent nightly builds available in the [forums](https://forums.codeblocks.org/index.php/board,20.0.html) or (for Ubuntu users) in the [Ubuntu PPA repository](https://launchpad.net/~x-psoud/+archive/ubuntu/cbreleases/). Please note that we consider nightly builds to be stable, usually.

**NOTE**: We have a [Changelog for 25.03](/changelogs/25.03), that gives you an overview over the enhancements and fixes we have put in the new release.

**NOTE**: The default builds are 64 bit (starting with release 20.03). We also provide 32bit builds only for convenience.

---

## ![](/images/os/windows48.png#logo) Microsoft Windows (64 bit, default)
| File 	                                     | Download from
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| codeblocks-25.03-setup.exe                 | [Sourceforge.net](https://sourceforge.net/projects/codeblocks/files/Binaries/25.03/Windows/codeblocks-25.03-setup.exe) |
| codeblocks-25.03-setup-nonadmin.exe        | [Sourceforge.net](https://sourceforge.net/projects/codeblocks/files/Binaries/25.03/Windows/codeblocks-25.03-setup-nonadmin.exe) |
| codeblocks-25.03-nosetup.zip               | [Sourceforge.net](https://sourceforge.net/projects/codeblocks/files/Binaries/25.03/Windows/codeblocks-25.03-nosetup.zip) |
| codeblocks-25.03mingw-setup.exe            | [Sourceforge.net](https://sourceforge.net/projects/codeblocks/files/Binaries/25.03/Windows/codeblocks-25.03mingw-setup.exe) |
| codeblocks-25.03mingw-nosetup.zip          | [Sourceforge.net](https://sourceforge.net/projects/codeblocks/files/Binaries/25.03/Windows/codeblocks-25.03mingw-nosetup.zip) |

**NOTE**: The codeblocks-25.03-setup.exe file includes Code::Blocks with all plugins. The codeblocks-25.03-setup-nonadmin.exe file is provided for convenience to users that do not have administrator rights on their machine(s).

**NOTE**: The codeblocks-25.03mingw-setup.exe file includes additionally the GCC/G++/GFortran/Clang compiler and GDB debugger from [WinLibs project](https://winlibs.com/) (version 14.2.0, 32/64 bit).

**NOTE**: The codeblocks-25.03(mingw)-nosetup.zip files are provided for convenience to users that are allergic against installers. However, it will not allow to select plugins / features to install (it includes everything) and not create any menu shortcuts. For the "installation" you are on your own.

*If unsure, please use codeblocks-25.03mingw-setup.exe!*

## ![](/images/os/windows48.png#logo) Microsoft Windows (32 bit, special)
| File 	                                     | Download from
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| codeblocks-25.03-setup.exe           | [Sourceforge.net](https://sourceforge.net/projects/codeblocks/files/Binaries/25.03/Windows/32bit/codeblocks-25.03-32bit-setup.exe) |
| codeblocks-25.03-setup-nonadmin.exe  | [Sourceforge.net](https://sourceforge.net/projects/codeblocks/files/Binaries/25.03/Windows/32bit/codeblocks-25.03-32bit-setup-nonadmin.exe) |
| codeblocks-25.03-nosetup.zip         | [Sourceforge.net](https://sourceforge.net/projects/codeblocks/files/Binaries/25.03/Windows/32bit/codeblocks-25.03-32bit-nosetup.zip) |
| codeblocks-25.03mingw-setup.exe      | [Sourceforge.net](https://sourceforge.net/projects/codeblocks/files/Binaries/25.03/Windows/32bit/codeblocks-25.03mingw-32bit-setup.exe) |
| codeblocks-25.03mingw-nosetup.zip    | [Sourceforge.net](https://sourceforge.net/projects/codeblocks/files/Binaries/25.03/Windows/32bit/codeblocks-25.03mingw-32bit-nosetup.zip) |

---

## ![](/images/os/linux48.png#logo) Linux 32 and 64-bit
| Distro | File | Download from
|--------|------|---------------|
| ![](/images/os/debian48.png#logo) | codeblocks_25.03_amd64_debian11.tar.xz | [Sourceforge.net](https://sourceforge.net/projects/codeblocks/files/Binaries/25.03/Linux/codeblocks_25.03_amd64_debian11.tar.xz) |
| ![](/images/os/debian48.png#logo) | codeblocks_25.03_amd64_debian12.tar.xz | [Sourceforge.net](https://sourceforge.net/projects/codeblocks/files/Binaries/25.03/Linux/codeblocks_25.03_amd64_debian12.tar.xz) |
| ![](/images/os/debian48.png#logo) | codeblocks_25.03_i386_debian11.tar.xz | [Sourceforge.net](https://sourceforge.net/projects/codeblocks/files/Binaries/25.03/Linux/codeblocks_25.03_i386_debian11.tar.xz) |
| ![](/images/os/debian48.png#logo) | codeblocks_25.03_i386_debian12.tar.xz | [Sourceforge.net](https://sourceforge.net/projects/codeblocks/files/Binaries/25.03/Linux/codeblocks_25.03_i386_debian12.tar.xz) |

**Note**: The Linux packages above are compressed archives (tar, tar.xz or tar.bz2). When you decompress the package you downloaded on your system, you will find all the .rpm or .deb packages required to install Code::Blocks.

**Note**: Redhat/CentOS probably also needs an installed hunspell-package, if you want to install the contrib-plugins.

---

## ![](/images/os/apple48.png#logo) Mac
| File | Download from |
|------|---------------|
| CodeBlocks-25.03_macOS-11.7_x64-wx3.2.6.dmg | [Sourceforge.net](https://sourceforge.net/projects/codeblocks/files/Binaries/13.12/Mac/CodeBlocks-25.03_macOS-11.7_x64-wx3.2.6.dmg) |

**NOTES**:

 * Code::Blocks 25.03 for Mac is currently unsable due to a lack of Mac developers. We could use an extra Mac developer to work on these issues!

--- 

## See also
