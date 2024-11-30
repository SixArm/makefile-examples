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
vet::
	@echo "Vet this system, such as printing some of its important tools, their versions, and paths. This task is intended to help with installation, debugging, and maintenance."

vet:: vet_system_group vet_development_group vet_python_group vet_postgresql_group

vet_system_group: vet_user vet_home vet_path vet_uname

vet_user:
	@echo "\n### user ###"
	echo $USER

vet_home:
	@echo "\n### home ###"
	echo $HOME

vet_path:
	@echo "\n### path ###"
	echo $PATH

vet_uname:
	@echo "\n### uname ###"
	uname -a
	which uname

vet_development_group: vet_make vet_gcc vet_git

vet_make:
	@echo "\n### make ###"
	make --version | head -1
	which make

vet_git:
	@echo "\n### git ###"
	git --version
	which git

vet_gcc:
	@echo "\n### gcc ###"
	gcc --version | head -1
	which gcc

vet_python_group: vet_python vet_pip vet_pipx vet_poetry

vet_python:
	@echo "\n### python ###"
	python --version
	which python

vet_pip:	
	@echo "\n### pip ###"
	pip --version
	which pip 

vet_pipx:	
	@echo "\n### pipx ###"
	pipx --version
	which pipx

vet_poetry:
	@echo "\n### poetry ###" 
	poetry --version
	which poetry 

vet_postgresql_group: vet_pg_config vet_psql vet_psql_connection

vet_pg_config:
	@echo "\n### pg_config ###"
	pg_config --version
	which pg_config

vet_psql:
	@echo "\n### psql ###"
	psql --version
	which psql

vet_psql_connection:
	@echo "\n### psql connection ###"
	psql --username postgres --tuples-only --no-align --command='select version();'
