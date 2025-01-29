##
# Makefile example that shows how to check processes for a match.
#
# https://github.com/SixArm/makefile-examples/tree/main/ps-match
#
# Example to check for a process that matches the string "foo":
#
#     make ps-match-foo
#
# This matches anywhere in the process listing, including the user name, command
# name, arguments, and anything else that the command `ps` shows.
##

##
# ps-match: Run the command `ps` and grep the output for a match.
##
.PHONY: ps-match-%
ps-match-%:
	@ps aux | grep "$*"
