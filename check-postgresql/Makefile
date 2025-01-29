##
# Makefile example to check PostgreSQL and related tools.
#
# https://github.com/SixArm/makefile-examples/tree/main/check-postgresql
#
# To run this:
#
#     make
#
# This file is intended to be customized for your own purposes.
##

##
# check-postgresql-group: Check all the PostgreSQL aspects.
##
.PHONY: check-postgresql-group
check-postgresql-group: check-ps-postgres check-pg-config check-psql check-psql-connection

##
# check-ps-postgres: Use the command `ps` to list PostgreSQL-related processes.
##
.PHONY: check-ps-postgres
check-ps-postgres:
	@echo "\n### $@ ###"
	ps aux | grep postgres

##
# check-pg-config: Print the version and path of the command `pg_config`.
##
.PHONY: check-pg-config
check-pg-config:
	@echo "\n### $@ ###"
	pg_config --version || true
	which pg_config || true

##
# check-pg-psql: Print the version and path of the command `psql`.
##
.PHONY: check-psql
check-psql:
	@echo "\n### $@ ###"
	psql --version || true
	which psql || true

##
# check-psql-connection: Check that it's possible to connect to PostgreSQL via the command `psql`.
##
.PHONY: check-psql-connection
check-psql-connection:
	@echo "\n### $@ ###"
	$(shell command -v "psql" >/dev/null 2>&1 && psql --username postgres --tuples-only --no-align --command='select version();')
