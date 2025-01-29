##
# Makefile example to check installed software versions.
#
# https://github.com/SixArm/makefile-examples/tree/main/check-system
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

.PHONY: check-system-group
check-system-group: check-uname check-user check-home check-path

.PHONY: check-uname
check-uname:
	@echo "\n### $@ ###"
	uname -a
	which uname

.PHONY: check-user
check-user:
	@echo "\n### $@ ###"
	echo "$$USER"

.PHONY: check-home
check-home:
	@echo "\n### $@ ###"
	echo "$$HOME"

.PHONY: check-path
check-path:
	@echo "\n### $@ ###"
	echo "$$PATH"
