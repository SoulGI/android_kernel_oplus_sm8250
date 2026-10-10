# Difference between this repository and upstream repository

This repository directly applies several fixes generated after analysis by a Large Language Model (LLM). **I have zero experience with Linux kernel development or custom modding**, so I cannot verify whether these fixes are legitimately correct or merely LLM hallucinations.

Therefore, I forked the upstream repository, applied a few LLM-generated fixes, built the flashable package with the help of the LLM, and finally flashed it onto my own device.

Based on my hands-on testing so far, the fixes provided by the LLM seem visually and functionally correct in daily use. However, I cannot guarantee that issues won't gradually surface tomorrow, the day after, or further down the line.

**Use at your own risk. I hold myself to the exact same standard. So if you do not understand what "use at your own risk" means, please do not use builds from this repository.**

If something goes wrong when you flash it, whether you hurl abuse at me, beg humbly for help, or offer me money directly, I will not be able to assist you. As mentioned earlier, I am just an amateur doing my best to look out for myself.

In most cases, please consider using upstream only:
https://github.com/xxtvrxx233/android_kernel_oplus_sm8250

___________________________________________________________________________________________________

# Build it yourself?

Build Kernel
```bash
  sh ./build.sh
```
Build Kernel with ReSukiSU
```bash
  sh ./build_ksu.sh
```
___________________________________________________________________________________________________

Linux kernel
============

There are several guides for kernel developers and users. These guides can
be rendered in a number of formats, like HTML and PDF. Please read
Documentation/admin-guide/README.rst first.

In order to build the documentation, use ``make htmldocs`` or
``make pdfdocs``.  The formatted documentation can also be read online at:

    https://www.kernel.org/doc/html/latest/

There are various text files in the Documentation/ subdirectory,
several of them using the Restructured Text markup notation.
See Documentation/00-INDEX for a list of what is contained in each file.

Please read the Documentation/process/changes.rst file, as it contains the
requirements for building and running the kernel, and information about
the problems which may result by upgrading your kernel.


___________________________________________________________________________________________________

# Acknowledgements
- **[xxtvrxx233/android_kernel_oplus_sm8250](https://github.com/xxtvrxx233/android_kernel_oplus_sm8250)**:
  the direct upstream of this fork. All kernel source and porting work in this repository
  originates there.
- **[xxtvrxx233/AnyKernel3](https://github.com/xxtvrxx233/AnyKernel3)**:
  the accompanying flashable-package setup (this repository uses its `realme-sm8250` branch).
- **[ZyCromerZ/Clang](https://github.com/ZyCromerZ/Clang)**:
  the prebuilt Clang 16 toolchain used to build this kernel (`Clang-16.0.6-20250721`).
- **[osm0sis/AnyKernel3](https://github.com/osm0sis/AnyKernel3)**:
  original author of the AnyKernel3 framework.
- **[ReSukiSU](https://github.com/ReSukiSU/ReSukiSU)**:
  the kernel-level root solution integrated by `build_ksu.sh`.
- **The Linux kernel community / [the CIP project](https://git.kernel.org/pub/scm/linux/kernel/git/cip/linux-cip.git) / CAF (Code Aurora Forum)**:
  the kernel source baseline.
