obj-m += dev_nr.o

all:
	make -C /lib/modules/$$(uname -r)/build M=$(PWD) modules
	sudo mknod /dev/mydevice c 64 0
	sudo insmod dev_nr.ko

run:
	./test

clean:
	sudo rmmod dev_nr.ko
	sudo rm /dev/mydevice
	make -C /lib/modules/$$(uname -r)/build M=$(PWD) clean
	rm -f test	
