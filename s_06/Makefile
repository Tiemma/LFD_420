### Automatic Makefile generation by 'genmake' script        ####
### Copyright, Jerry Cooperstein, coop@linuxfoundation.org 2/2003 - 1/2017 ####
### License: GPLv2 ###

obj-m +=  for_each_process.o linked_list_master.o module_master.o module_slave.o

export KROOT=/lib/modules/4.15.0-112-generic/build

allofit:  modules
modules:
	@$(MAKE) -C $(KROOT) M=$(shell pwd) modules
modules_install:
	@$(MAKE) -C $(KROOT) M=$(shell pwd) modules_install
kernel_clean:
	@$(MAKE) -C $(KROOT) M=$(shell pwd) clean

clean: kernel_clean
	rm -rf   Module.symvers modules.order
