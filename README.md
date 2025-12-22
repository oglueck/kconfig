# Linux Kernel Default Config 
For x64 commodity hardware

I regularly publish default configuration of the Linux kernel for popular and modern x86_64 commodity hardware that is typically found in netbooks, laptops, desktops or off-the-shelf servers. I am not talking about embedded devices, development, big iron, other platforms, exotic hardware or peripherials. Just the standard stuff for running Linux. No discussion about modules vs. built-in. I do built-in. 

[Details](https://www.odi.ch/prog/kernel-config.php) on all current kernel options.


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
