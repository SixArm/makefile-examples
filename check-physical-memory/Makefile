##
# Makefile example to check physical memory by using top.
#
# https://github.com/SixArm/makefile-examples/tree/main/check-physical-memory
#
# To run this:
#
#     make
#
# This file is intended to be customized for your own purposes.
##

.PHONY: check-physical-memory
check-physical-memory:
	top -l 1 -s 0 | grep PhysMem
