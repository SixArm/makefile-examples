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

.PHONY: vet_python_group
vet_python_group: vet_python vet_pip vet_pipx vet_poetry

.PHONY: vet_python
vet_python:
	@echo "\n### python ###"
	python --version
	which python

.PHONY: vet_pip
vet_pip:	
	@echo "\n### pip ###"
	pip --version
	which pip 

.PHONY: vet_pipx
vet_pipx:	
	@echo "\n### pipx ###"
	pipx --version
	which pipx

.PHONY: vet_poetry
vet_poetry:
	@echo "\n### poetry ###" 
	poetry --version
	which poetry 
