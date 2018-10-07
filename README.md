# Real Time Kernel
### File
rt-kernel_4.14.66-rt40.tgz
### Version
4.14.66-rt40 (PREEMPT_RT)
### Description
Cross compiled RT-Kernel on Ubuntu 16.04
### How to use
1. Unzip file: `~$ tar xzf rt-kernel_4.14.66-rt40.tgz`
  * contents: bcm* boot/ lib/ overlays/
2. Copy and Paste files
 - copy boot/
    - `~$ sudo cp -dr ./boot/* /boot/``
 - copy lib/
    - `~$ sudo cp -dr ./lib/* /lib/`
 - copy overlays/
    - `~$ sudo cp -d ./overlays/* /boot/overlays`
 - copy files
    - `~$ sudo cp -d bcm* /boot/`
3. Change [/boot/config.txt]: `~$ sudo nano /boot/config.txt`
 - Add option: `kernel=vmlinuz-4.14.66-rt40-v7+`


##### Comments
 copy option -d: 원본파일이 소프트링크 파일이면, 소프트링크 원본을 복사한다.   
 copy option -r: 디렉토리 안의 모든 하위디렉토리, 파일들이 복사된다.

 [/boot/config.txt]:https://www.raspberrypi.org/documentation/configuration/config-txt/

##### Reference
[lemariva blog / Raspberry pi RT patching tutorial](https://lemariva.com/blog/2018/07/raspberry-pi-preempt-rt-patching-tutorial-for-kernel-4-14-y)
