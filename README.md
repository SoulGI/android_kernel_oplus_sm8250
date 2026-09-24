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

# 鸣谢 / Acknowledgements

本仓库是上游项目的 fork。内核源码、移植适配与整套自动化构建体系均来自原作者，
在此向上游作者与所有相关开源项目致谢。

## 上游项目

- **[xxtvrxx233/android_kernel_oplus_sm8250](https://github.com/xxtvrxx233/android_kernel_oplus_sm8250)**
  —— 本 fork 的直接上游，本仓库的全部内核源码与移植工作均出自此处。
- **[xxtvrxx233/AnyKernel3](https://github.com/xxtvrxx233/AnyKernel3)**
  —— 配套的刷机包方案（本仓库使用其 `realme-sm8250` 分支）。

特别感谢上游作者提供的以下基础设施，本 fork 直接沿用、未作改动：

- 基于 GitHub Actions 的全自动内核构建与打包流水线（`ci/build_ci.sh`、`.github/workflows/`）
- `zyc-clang-16` 工具链的选型与获取脚本
- 面向 realme SM8250 系列机型的 AnyKernel3 刷机包配置

## 其他上游依赖

- **[ZyCromerZ/Clang](https://github.com/ZyCromerZ/Clang)**
  —— 本项目构建所使用的 Clang 16 预编译工具链（`Clang-16.0.6-20250721`）。
- **[osm0sis/AnyKernel3](https://github.com/osm0sis/AnyKernel3)**
  —— AnyKernel3 框架的原始作者。
- **[ReSukiSU](https://github.com/ReSukiSU/ReSukiSU)**
  —— `build_ksu.sh` 所集成的内核级 root 方案。
- **Linux 内核社区 / [CIP 项目](https://git.kernel.org/pub/scm/linux/kernel/git/cip/linux-cip.git) / CAF（Code Aurora Forum）**
  —— 内核源码基线。

## 说明

本 fork 仅用于个人使用与问题排查。所有原始代码的版权、署名与许可，
均归上述各项目的作者所有；本仓库不对其主张任何权利。
