1. git clone https://github.com/dodyirawan85/android_kernel_realme_sdm660 rmx && cd rmx
2. git clone https://github.com/kdrag0n/proton-clang --depth=1
3. #!/bin/bash

# Main environtment
KERNEL_DIR=$PWD
KERN_IMG=$KERNEL_DIR/out/arch/arm64/boot/Image.gz-dtb
CONFIG=RMX1801_defconfig
CROSS_COMPILE="aarch64-linux-gnu-"
CROSS_COMPILE_ARM32="arm-linux-gnueabi-" 
PATH=:"${KERNEL_DIR}/proton-clang/bin:${PATH}"

#user-host
export KBUILD_BUILD_USER=kontol
export KBUILD_BUILD_HOST=ngaceng
# Compile plox
function compile() {
    make -j$(nproc) O=out ARCH=arm64 RMX1801_defconfig
    make -j$(nproc) O=out ARCH=arm64  CC=clang \
                               CROSS_COMPILE=aarch64-linux-gnu- \
                               CROSS_COMPILE_ARM32=arm-linux-gnueabi-
}
compile


=========================>


1.    ls

2.     cd out && cd arch && cd arm64 && cd boot


3.     rm -rf .git


4.      git init

5.      git add Image.gz-dtb

6.       git commit -m "terserah isi apa"

7.      git branch -M dono

8.        git remote add origin https://github.com/Dono5/dono.git

9.       git push -u origin dono











