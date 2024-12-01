# Makefile example to vet (i.e. verify) installed software versions.
#
#   * operating system e.g. macOS-based Darwin, Debian-based Linux, etc.
#   * python programming language
#   * pip runtime tool
#   * poetry dependency manager
#   * postgresql database and related tools psql and pg_config.
#
# To run this:
#
#     make vet
#
# This example is intended to demonstrate various kinds of tools,
# and how to get their version numbers, their paths, and more.
#
# This file is intended to be customized for your own purposes.

define newline


endef

.PHONY: vet
vet:: vet_development_group

.PHONY: vet_development_group
vet_development_group: vet_make vet_gcc vet_git vet_aws_cli

.PHONY: vet_make
vet_make:
	@echo "\n### make ###"
	make --version | head -1
	which make

.PHONY: vet_git
vet_git:
	@echo "\n### git ###"
	git --version
	which git

.PHONY: vet_gcc
vet_gcc:
	@echo "\n### gcc ###"
	gcc --version | head -1
	which gcc

.PHONY: vet_aws_cli
vet_aws_cli:
	@echo "\n### aws-cli ###"
	aws --version
	which aws
