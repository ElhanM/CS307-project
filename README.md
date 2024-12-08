# CS307 Operating Systems Project: Minimal Operating System in C++

linux mint 17

sudo apt-get install g++ binutils libc6-dev-i386

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