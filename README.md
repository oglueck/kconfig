# Linux Kernel Default Config 
For x64 commodity hardware

I regularly publish default configuration of the Linux kernel for popular and modern x86_64 commodity hardware that is typically found in netbooks, laptops, desktops or off-the-shelf servers. I am not talking about embedded devices, development, big iron, other platforms, exotic hardware or peripherials. Just the standard stuff for running Linux. No discussion about modules vs. built-in. I do built-in. 

[Details](https://www.odi.ch/prog/kernel-config.php) on all current kernel options.

## Assumptions
For these ready-made kernels the following assumptions were made:
* VHOST: KVM is enabled to host virtual machines with QEmu
* VGUEST: no VM guest support
* SEC: most security relevant options have been enabled, except CPU vulnerability mitigations since they are not relevant in practice IMHO and only kill performance
* OLD: deprecated and obsolete options are mostly disabled
* COMPAT: options are mostly enabled
* DEV: development and debugging options are disabled
* Intel, nNvidia and AMD graphic are all enabled
* Intel sound is enabled
* Compiled for the _local_ CPU (X86_NATIVE_CPU) (not generic x86!)
* The kernel can be used as a crash-kernel as well


## Archive By Kernel Version
The archive contains each a `defconfig` file and a `config` file. 

How to use them:
```
S=/usr/src/linux
cp config $S/.config

# or
cp defconfig $S/arch/x86/configs/x86_64_defconfig
cd $S
make defconfig
```

after that customize your config as usual: `make menuconfig`

## Versions
* [6.18](x86_64/v6.18/)
* [6.19](x86_64/v6.19/)
* [7.0](x86_64/v7.0/)
* [7.1](x86_64/v7.1/)
