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

.PHONY: vet_postgresql_group
vet_postgresql_group: vet_pg_config vet_psql vet_psql_connection

.PHONY: vet_pg_config
vet_pg_config:
	@echo "\n### pg_config ###"
	pg_config --version
	which pg_config

.PHONY: vet_psql
vet_psql:
	@echo "\n### psql ###"
	psql --version
	which psql

.PHONY: vet_psql_connection
vet_psql_connection:
	@echo "\n### psql connection ###"
	psql --username postgres --tuples-only --no-align --command='select version();'
