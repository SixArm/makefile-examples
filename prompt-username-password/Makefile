##
# Makefile example that shows how to prompt for a username and password.
#
# * The prompt for the username displays as the user types.
#
# * The prompt for the password does not display as the user types.
#
# The task prints the username and password, just so you can see it work.
# In a real project, never print the password, because it's a secret.
##

USERNAME ?= $(shell read -p "Username: " x; echo $$x)
PASSWORD ?= $(shell read -s -p "Password: " x; echo $$x)

example:
	$(info The username is $(USERNAME))
	$(info The password is $(PASSWORD))
