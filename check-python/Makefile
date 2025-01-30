##
# Makefile example to check installed software versions.
#
# https://github.com/SixArm/makefile-examples/tree/main/check-python
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

.PHONY: check-python-group
check-python-group: check-python check-python-import check-pip check-pipx check-poetry

.PHONY: check-python
check-python:
	@echo "\n### $@ ###"
	python --version || true
	which -a python || true

.PHONY: check-python-import
check-python-import:
	@echo "\n### $@ ###"
	python -c "import numpy; print(numpy.__version__)"
	python -c "import pandas; print(pandas.__version__)"

.PHONY: check-pip
check-pip:	
	@echo "\n### $@ ###"
	pip --version || true
	which -a pip || true

.PHONY: check-pipx
check-pipx:	
	@echo "\n### $@ ###"
	pipx --version || true
	which -a pipx || true

.PHONY: check-poetry
check-poetry:
	@echo "\n### $@ ###"
	poetry --version || true
	which -a poetry || true
