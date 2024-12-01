# Makefile example to vet (i.e. verify) installed software versions.
#
# To run this:
#
#     make
#
# This example is intended to demonstrate various kinds of tools,
# and how to get their version numbers, their paths, and more.
#
# This file is intended to be customized for your own purposes.

.PHONY: vet_system_group
vet_system_group: vet_user vet_home vet_path vet_uname

.PHONY: vet_user
vet_user:
	@echo "\n### user ###"
	echo "$$USER"

.PHONY: vet_home
vet_home:
	@echo "\n### home ###"
	echo "$$HOME"

.PHONY: vet_path
vet_path:
	@echo "\n### path ###"
	echo "$$PATH"

.PHONY: vet_uname
vet_uname:
	@echo "\n### uname ###"
	uname -a
	which uname
