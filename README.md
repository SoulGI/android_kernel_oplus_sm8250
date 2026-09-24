# Build it yourself?

Build Kernel
```bash
  sh ./build.sh
```
Build Kernel with ReSukiSU
```bash
  sh ./build_ksu.sh
```


# Kernel CI Build System
This repository is equipped with a fully automated kernel build system powered by GitHub Actions.
Once code is pushed to the repository, the kernel will be built and packaged automatically in the cloud, eliminating the need for local builds

You can download artifacts [here](https://github.com/xxtvrxx233/android_kernel_oplus_sm8250/actions)


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

This repository is a fork. All kernel source code, device porting work and the entire automated
build system originate from the upstream author. Thanks are due to the upstream project and to
every open-source project this build depends on.

## Upstream projects

- **[xxtvrxx233/android_kernel_oplus_sm8250](https://github.com/xxtvrxx233/android_kernel_oplus_sm8250)**:
  the direct upstream of this fork. All kernel source and porting work in this repository
  originates there.
- **[xxtvrxx233/AnyKernel3](https://github.com/xxtvrxx233/AnyKernel3)**:
  the accompanying flashable-package setup (this repository uses its `realme-sm8250` branch).

The following infrastructure is used here unchanged, and is gratefully credited to the upstream
author:

- The fully automated kernel build and packaging pipeline built on GitHub Actions
  (`ci/build_ci.sh`, `.github/workflows/`).
- The selection and fetch script for the `zyc-clang-16` toolchain.
- The AnyKernel3 flashable-package configuration for realme SM8250 devices.

## Other upstream dependencies

- **[ZyCromerZ/Clang](https://github.com/ZyCromerZ/Clang)**:
  the prebuilt Clang 16 toolchain used to build this kernel (`Clang-16.0.6-20250721`).
- **[osm0sis/AnyKernel3](https://github.com/osm0sis/AnyKernel3)**:
  original author of the AnyKernel3 framework.
- **[ReSukiSU](https://github.com/ReSukiSU/ReSukiSU)**:
  the kernel-level root solution integrated by `build_ksu.sh`.
- **The Linux kernel community / [the CIP project](https://git.kernel.org/pub/scm/linux/kernel/git/cip/linux-cip.git) / CAF (Code Aurora Forum)**:
  the kernel source baseline.

## Note

This fork is maintained for personal use and troubleshooting only. All copyright, attribution and
licensing of the original code remain with the authors of the projects listed above; no claim is
made here.
