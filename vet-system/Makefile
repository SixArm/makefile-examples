##
# Makefile example to vet (i.e. verify) installed software versions.
#
# https://github.com/SixArm/makefile-examples/tree/main/vet-system
#
# To run this:
#
#     make
#
# This example is intended to demonstrate various kinds of tools,
# and how to get their version numbers, their paths, and more.
#
# This file is intended to be customized for your own purposes.
##

.PHONY: vet-system-group
vet-system-group: vet-uname vet-user vet-home vet-path

.PHONY: vet-uname
vet-uname:
	@echo "\n### $@ ###"
	uname -a
	which uname

.PHONY: vet-user
vet-user:
	@echo "\n### $@ ###"
	echo "$$USER"

.PHONY: vet-home
vet-home:
	@echo "\n### $@ ###"
	echo "$$HOME"

.PHONY: vet-path
vet-path:
	@echo "\n### $@ ###"
	echo "$$PATH"
