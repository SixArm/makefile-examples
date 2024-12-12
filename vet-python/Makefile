##
# Makefile example to vet (i.e. verify) installed software versions.
#
# https://github.com/SixArm/makefile-examples/tree/main/vet-python
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

.PHONY: vet-python-group
vet-python-group: vet-python vet-python-import vet-pip vet-pipx vet-poetry

.PHONY: vet-python
vet-python:
	@echo "\n### $@ ###"
	python --version
	which python

.PHONY: vet-python-import
vet-python-import:
	@echo "\n### $@ ###"
	python -c "import numpy; print(numpy.__version__)"
	python -c "import pandas; print(pandas.__version__)"

.PHONY: vet-pip
vet-pip:	
	@echo "\n### $@ ###"
	pip --version
	which pip

.PHONY: vet-pipx
vet-pipx:	
	@echo "\n### $@ ###"
	pipx --version
	which pipx

.PHONY: vet-poetry
vet-poetry:
	@echo "\n### $@ ###"
	poetry --version
	which poetry
