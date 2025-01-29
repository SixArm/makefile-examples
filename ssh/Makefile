##
# Makefile example: set up secure shell.
#
# https://github.com/SixArm/makefile-examples/tree/main/ssh
#
# Currently this Makefile just creates placeholder files:
#
#   $HOME/.ssh/config
#   $HOME/.ssh/known_hosts
##

##
# ssh: Use ssh which is secure shell access.
##
.PHONY: ssh
ssh: $(HOME)/.ssh/config $(HOME)/.ssh/known_hosts

##
# $(HOME)/.ssh/config: Create a placeholder blank file
##
$(HOME)/.ssh/config:
	mkdir -p "$(HOME)/.ssh"
	touch $@

##
# $(HOME)/.ssh/known_hosts: Create a placeholder blank file
##
$(HOME)/.ssh/known_hosts:
	mkdir -p "$(HOME)/.ssh"
	touch $@
