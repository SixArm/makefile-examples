##
# Makefile example that shows how to check processes for a match.
#
# https://github.com/SixArm/makefile-examples/tree/main/process-match
#
# Example to check for a process that matches the string "foo":
#
#     make process-match-foo
#
# This matches anywhere in the process listing, including the user name, command
# name, arguments, and anything else that the command `ps` shows.
##

##
# process-match: Run the command `ps` and grep the output for a match.
##
.PHONY: process-match-%
process-match-%:
	@ps aux | grep "$*"
