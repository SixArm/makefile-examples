##
# Makefile example to vet (i.e. verify) installed software versions.
#
# https://github.com/SixArm/makefile-examples/tree/main/vet-postgresql
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

.PHONY: vet-postgresql-group
vet-postgresql-group: vet-pg-config vet-psql vet-psql-connection

.PHONY: vet-pg-config
vet-pg-config:
	@echo "\n### $@ ###"
	pg_config --version
	which pg_config

.PHONY: vet-psql
vet-psql:
	@echo "\n### $@ ###"
	psql --version
	which psql

.PHONY: vet-psql-connection
vet-psql-connection:
	@echo "\n### $@ ###"
	psql --username postgres --tuples-only --no-align --command='select version();'
