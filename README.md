# CS307 Operating Systems Project: Minimal Operating System in C++

linux mint 17

sudo apt-get install g++ binutils libc6-dev-i386

make clean

make loader.o
make kernel.o
make mykernel.bin

make install
sudo vim /boot/grub/grub.cfg

...
### END /etc/grub.d/30 os-prober ###


### BEGIN MYKERNEL ###

menuentry 'My Operating System' {
  multiboot /boot/mykernel.bin
  boot
}

### END MYKERNEL ###


### BEGIN /etc/grub.d/30 uefi-firmware ###
...

VirtualBox:
https://www.linuxquestions.org/questions/linux-software-2/how-install-virtualbox-7-0-20-on-linux-mint-22-a-4175739823/

sudo apt-get install grub-common xorriso

make mykernel.iso

Open VirtualBox -> New
Name: My Operating System
ISO Image: mykernel.iso
Type: Other
Version: Other/Unknown

Do Not Add a Virtual Hard Disk

https://superuser.com/questions/579156/how-to-release-mouse-from-virtualbox


