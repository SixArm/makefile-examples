##
# Makefile example to check installed software versions.
#
# https://github.com/SixArm/makefile-examples/tree/main/check-development
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

.PHONY: check-development-group
check-development-group: check-make check-gcc check-git check-aws-cli

.PHONY: check-make
check-make:
	@echo "\n### $@ ###"
	make --version || true
	which -a make || true

.PHONY: check-git
check-git:
	@echo "\n### $@ ###"
	git --version || true
	which -a git || true

.PHONY: check-gcc
check-gcc:
	@echo "\n### $@ ###"
	gcc --version || true
	which -a gcc || true

.PHONY: check-aws-cli
check-aws-cli:
	@echo "\n### $@ ###"
	aws --version || true
	which -a aws || true
