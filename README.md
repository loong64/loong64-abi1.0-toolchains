# cross-tools for ABI1.0

LoongArch64 cross-compile toolchain, supports both i686 Windows (MinGW-w64) and x86_64 Linux architectures.

# New! 

There are some newly compiled toolchains (i.e. using GCC 14) in [this repo](https://github.com/loong64/cross-tools/tree/canadian). 

## Toolchains

| Name                       | Version | Supported Host                                                                                                                                                                                                                                                                                                                             | Target                | Kernel | Binutils | GCC   | Libc(glibc) | Note                                                        |
| -------------------------- | ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------- | ------ | -------- | ----- | ----------- | ----------------------------------------------------------- |
| GCC 8.3 with LSX / LASX    | rc1.5   | [i686 Windows](https://github.com/loong64/loong64-abi1.0-toolchains/releases/download/20250722/loongson-gnu-toolchain-8.3-i686-mingw-loongarch64-linux-gnu-rc1.6.zip)/[x86_64 Linux](https://github.com/loong64/loong64-abi1.0-toolchains/releases/download/20250722/loongson-gnu-toolchain-8.3-x86_64-loongarch64-linux-gnu-rc1.6.tar.xz) | loongarch64-linux-gnu | 4.15.0 | 2.31     | 8.3.0 | 2.28        | Only support `lp64d` glibc ABI                              |
| GCC 8.3 without LSX / LASX | rc1.1   | [x86_64 Linux](https://github.com/loong64/loong64-abi1.0-toolchains/releases/download/20250722/loongson-gnu-toolchain-8.3.novec-x86_64-loongarch64-linux-gnu-rc1.1.tar.xz)                                                                                                                                                                 | loongarch64-linux-gnu | 4.15.0 | 2.31     | 8.3.0 | 2.28        | Only support `lp64d` glibc ABI, no vector extension support |
| go | 1.24.0 1.24.3 | x86_64 Linux | linux/loong64 |  N/A | N/A     | N/A | N/A        | Share the same target with office go, which only support ABI2.0. Always clear the build cache before building for another ABI target!|

## How to use

Download the tarball from the [release page](https://github.com/loong64/cross-tools/releases) and extract it to `/opt/x-tools`:

```sh
sudo mkdir -p /opt/x-tools
sudo tar -xf ${Target}.tar.xz -C /opt/x-tools
```

## How to build

Currently，the toolchains are provided on loongson's official website, and the build process is not open sourced. You can find the release page of toolchains on [the official website](https://www.loongnix.cn/zh/toolchain/GNU/).

## License

There are currently no licenses information for the toolchains on the official website. The copyright information under the official website is `© 龙芯开源社区`.

## Acknowledgements

We would like to express our gratitude to the following organizations, individuals and projects:

- [龙芯开源社区](https://www.loongnix.cn/)
