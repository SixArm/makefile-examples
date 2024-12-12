##
# Makefile example: GitHub SSH setup using ssh-keygen and ~/.ssh/config.
#
# https://github.com/SixArm/makefile-examples/tree/main/ssh-keygen
##

EMAIL ?= $(shell read -p "Email: " x; echo $$x)

##
# github-ssh: create your SSH settings suitable for GitHub.
##
.PHONY: github-ssh
github-ssh: $(HOME)/.ssh/id_ed25519-example $(HOME)/.ssh/config-example

##
# $(HOME)/.ssh/id_ed25519-example: generate your SSH key suitable for GitHub.
##
$(HOME)/.ssh/id_ed25519-example:
	ssh-keygen -t ed25519 -C "$(EMAIL)" -f $@
	cat $@.pub

##
# $(HOME)/.ssh/config-example: append your GitHub host to your SSH config file.
##
$(HOME)/.ssh/config-example:
	@echo "Host github.com\n  AddKeysToAgent yes\n  UseKeychain yes\n  IdentityFile ~/.ssh/id_ed25519" >> $@
