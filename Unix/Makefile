ifeq ($(origin SOLUTION_DIR), undefined)
	SOLUTION_DIR := $(shell pwd)/
endif
PROJECT_DIR_DISTORM:=$(dir $(lastword $(MAKEFILE_LIST)))

clean::
	rm -f libdistorm64.so*
	rm -f libdistorm

libdistorm:
	cd $(PROJECT_DIR_DISTORM)/../build/linux && make clib
	cp $(PROJECT_DIR_DISTORM)/../build/linux/libdistorm64.so* .
	cd $(PROJECT_DIR_DISTORM)/../build/linux && make -i clean
	touch libdistorm


