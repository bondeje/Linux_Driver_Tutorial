obj-m += mymodule.o

all:
	make -C /lib/modules/$$(uname -r)/build M=$(PWD) modules
	sudo insmod mymodule.ko

clean:
	sudo rmmod mymodule.ko
	make -C /lib/modules/$$(uname -r)/build M=$(PWD) clean
	
