---
title: "Source code"
date: 2025-08-24
draft: false
aliases:
  - 25
---

If you want to download the source code of Code::Blocks 25.03, here are the links:
| File                     | Download from                                                                                            |
|--------------------------|----------------------------------------------------------------------------------------------------------|
| codeblocks_25.03.tar.xz  | [Sourceforge.net](https://sourceforge.net/projects/codeblocks/files/Sources/25.03/codeblocks_25.03.tar.xz) or [dAppCDN.com](https://dappcdn.com/download/devtools/code-blocks?get=codeblocks_25.03.tar.xz) |
| codeblocks_25.03.tar.bz2 | [Sourceforge.net](https://sourceforge.net/projects/codeblocks/files/Sources/25.03/codeblocks_25.03.tar.bz2) or [dAppCDN.com](https://dappcdn.com/download/devtools/code-blocks?get=codeblocks_25.03.tar.bz2) |

For older versions please check [here](/downloads/source/older).

Alternatively, you could [retrieve the code from SVN](/downloads/svn). Either way, if it turns out you need to patch the source code in order to create packages for your favourite Linux distribution, we would be interested to know about the needed changes so we can include them in our next release.

## Documentation

We provide a (Doxygen based) documentation of the Code::Blocks SDK to developers for developing their own plugins. It consists of the following documents:

 * the main document: The Code::Blocks SDK itself (sdk.chm)
 * the SDK for developing add-ons for wxSmith, the GUI design tool in Code::Blocks (wxSmith.chm) and
 * the documentation for the CodeCompletion plugin in case you want to extend it:

| File               | Download from                                                                              |
|--------------------|--------------------------------------------------------------------------------------------|
| sdk.chm            | [Sourceforge.net](https://sourceforge.net/projects/codeblocks/files/Sources/25.03/sdk.chm) |
| wxSmith.chm        | [Sourceforge.net](https://sourceforge.net/projects/codeblocks/files/Sources/25.03/wxSmith.chm) |
| codecompletion.chm | [Sourceforge.net](https://sourceforge.net/projects/codeblocks/files/Sources/25.03/codecompletion.chm) |

---

> Note to Windows users: If you download (any) CHM file, Windows will usually block the file content by default to protect you from embedded HTML viruses. The result is an empty CHM file if you open it. If that is the case, mark the CHM file as safe after download in the file properties (right click in the Explorer on the file, select "Properties" and tick the "Allow" checkbox at the bottom, next to the "Security" note.)

## Miscellaneous

Note that wxWidgets for Windows comes compiled in a shared, monolithic, release, unicode flavour, compiled like that:

    mingw32-make -f makefile.gcc SHARED=1 MONOLITHIC=1 BUILD=release UNICODE=1

---

## See also
