obj-m += read_write.o

all:
	make -C /lib/modules/$$(uname -r)/build M=$(PWD) modules
	sudo insmod read_write.ko

clean:
	sudo rmmod read_write.ko
	make -C /lib/modules/$$(uname -r)/build M=$(PWD) clean
	
