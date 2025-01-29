##
# Makefile example to check installed software versions.
#
# https://github.com/SixArm/makefile-examples/tree/main/check-postgresql
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

.PHONY: check-postgresql-group
check-postgresql-group: check-pg-config check-psql check-psql-connection

.PHONY: check-pg-config
check-pg-config:
	@echo "\n### $@ ###"
	pg_config --version
	which pg_config

.PHONY: check-psql
check-psql:
	@echo "\n### $@ ###"
	psql --version
	which psql

.PHONY: check-psql-connection
check-psql-connection:
	@echo "\n### $@ ###"
	psql --username postgres --tuples-only --no-align --command='select version();'
