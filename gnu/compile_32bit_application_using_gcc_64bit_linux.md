# 64bit环境GCC编译32bit程序

ubuntu环境下 `gcc` 是64bit：

```bash
$ gcc -v
Using built-in specs.
COLLECT_GCC=gcc
COLLECT_LTO_WRAPPER=/usr/lib/gcc/x86_64-linux-gnu/5/lto-wrapper
Target: x86_64-linux-gnu
```

需要编译32位程序，需要安装`gcc-multilib，libc6-dev-i386`，然后加上 `-m32`选项 修改 `Makefile`：

```bash
CFLAGS += -m32
```

For 32 bit version:
```bash
$ gcc -m32 -o output32 hello.c
```

For 64 bit version :
```bash
$ gcc -m64 -o output64 hello.c
```
> [How to create a 32-bit shared-library on a 64-bit platform with autotools](http://stackoverflow.com/questions/5383325/how-to-create-a-32-bit-shared-library-on-a-64-bit-platform-with-autotools)
