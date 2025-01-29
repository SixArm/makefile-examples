##
# Makefile example to vet (i.e. verify) installed software versions.
#
# https://github.com/SixArm/makefile-examples/tree/main/vet-development
#
# This example checks for:
#
#   * operating system e.g. macOS-based Darwin, Debian-based Linux, etc.
#   * python programming language
#   * pip runtime tool
#   * poetry dependency manager
#   * postgresql database and related tools psql and pg_config.
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

.PHONY: vet-development-group
vet-development-group: vet-make vet-gcc vet-git vet-aws-cli

.PHONY: vet-make
vet-make:
	@echo "\n### $@ ###"
	make --version | head -1
	which make

.PHONY: vet-git
vet-git:
	@echo "\n### $@ ###"
	git --version
	which git

.PHONY: vet-gcc
vet-gcc:
	@echo "\n### $@ ###"
	gcc --version | head -1
	which gcc

.PHONY: vet-aws-cli
vet-aws-cli:
	@echo "\n### $@ ###"
	aws --version
	which aws
