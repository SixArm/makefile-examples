# Makefile examples

Makefile examples repo. Each subdirectory demonstrates a make-related topic with an example.

Here's the example Makefile:

```make
##
# This is the Makefile for demonstrating some of our practices.
#
# The purpose of this Makefile is to provide a single entry point
# that new developers can use to set up their local computer, and
# install the relevant software tools and versions, and build Heron.
#
# This Makefile is a work in progress. We improve it as we go.
#
# Ideally this Makefile can mostly delegate to better tools,
# meaning our goal is to make this file just bootstrap glue.
#
# To build everything using our defaults:
#
#    make
#
# To check everything using our defaults:
#
#    make check
#
# To get help:
#
#    make help
#
##

.PHONY: default
default: hello

# Makefile example: use the command 'uname' to get system information.
#
# https://github.com/SixArm/makefile-examples/tree/main/uname
#
# This code is taken directly from the git Makefile.

uname_S := $(shell sh -c 'uname -s 2>/dev/null || echo not')
uname_M := $(shell sh -c 'uname -m 2>/dev/null || echo not')
uname_O := $(shell sh -c 'uname -o 2>/dev/null || echo not')
uname_R := $(shell sh -c 'uname -r 2>/dev/null || echo not')
uname_P := $(shell sh -c 'uname -p 2>/dev/null || echo not')
uname_V := $(shell sh -c 'uname -v 2>/dev/null || echo not')

# Makefile example to show how to write help comments.
#
# https://github.com/SixArm/makefile-examples/tree/main/help-comments
#
# Each help comment starts with two hash marks, and ends the same way.
# Our hope is this makes it easy for developers to add help information.
#
# Compared to other kinds of well-known make self-documentation tools,
# this implementation is simpler and is also much more flexible.

##
# help: Display this help message.
##
.PHONY: help
help:
	@awk '/^##/{a=1-a}a' $(MAKEFILE_LIST) | cut -c3-

# newline: This is a print helper when you want to embed a newline in a message.
define newline


endef

##
# hello: print "hello world"
##
.PHONY: hello
hello:
	$(info hello world)

# Makefile example to vet (i.e. verify) installed software versions.
#
#   * operating system e.g. macOS-based Darwin or Debian-based Linux.
#   * python programming language
#   * postgresql database
#   * pipx runtime tool
#
# To run this:
#
#     make check
#
# This example is intended to demonstrate various kinds of tools,
# and how to get their version numbers, and how to show error help.
#
# This file is intended to be customized and changed,
# such as by adjusting each tool's version number,
# and by adding/removing tools that you want to vet.

##
# check: Check this project, such as printing some of its important tools, their versions, and paths. This task is intended to help with installation, debugging, and maintenance.
##
.PHONY: check
check::
	@echo "Check this project, such as printing some of its important tools, their versions, and paths. This task is intended to help with installation, debugging, and maintenance."

check:: check-uname check-python

##
# check-uname: Print the uname information of the system.
##
.PHONY: check-uname
check-uname:
	@echo "\n### uname ###"
	uname -a

##
# check-python: Print the version and path of the command `python`.
##
.PHONY: check-python
check-python:
	@echo "\n### python ###"
	python --version || true
	which -a python || true
```
