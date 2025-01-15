
PATH:= /usr/sbin:/usr/bin
export PATH

default: clean image
image:
	mkosi build

run:
	mkosi qemu -vga std -display default,show-cursor=on

clean:
	mkosi clean
