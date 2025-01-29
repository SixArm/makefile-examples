##
# Makefile example that shows the command `dscl` with a match.
#
# https://github.com/SixArm/makefile-examples/tree/main/dscl-list-users-match
#
# Example to check for a process that matches the string "foo":
#
#     make dscl-list-users-match-foo
#
# This matches anywhere in the macOS dscl list of users' short names.
##

##
# dscl-list-users-match: Run the command `dscl . -list /Users` and grep the output for a match.
##
.PHONY: dscl-list-users-match-%
dscl-list-users-match-%:
	@dscl . -list /Users | grep "$*"
