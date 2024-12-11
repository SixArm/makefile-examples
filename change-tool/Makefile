##
# Makefile example that shows how to coach a user to change tools.
#
# This example checks for the tool 'asdf' (which we want to phase out),
# and if found, recommends the tool 'mise' (which we want to phase in).
##

.PHONY: example
example:
    @which -a asdf && printf %s\\n "Please consider changing from the tool 'asdf' to the tool 'mise'."
