##
# Makefile example: clone hosted repositories to local directories.
#
# https://github.com/SixArm/makefile-examples/tree/main/github-clone
#
# This implementation demonstrates how to pattern match
# a string such as "github.com/sixarm/checkline" then
# use the pattern match to clone the remote repository.
#
# To use this, specify what you want to clone, such as
# this GitHub SixArm repository named "checkline":
#
#     make github.com/sixarm/checkline
#
# The default local directory is:
#
#     $HOME/opt/github.com
#
# You can override this with the GITHUB_CLONE_TARGET_DIR environment variable.
##

GITHUB_CLONE_TARGET_DIR = $(HOME)/opt/github.com

##
# github.com/%: Match a generic GitHub URL-like repository string,
# such as "github.com/sixarm/checkline", then clone it locally.
##
.PHONY: github.com/%
github.com/%: 
	test -d "$(GITHUB_CLONE_TARGET_DIR)/$*" || git clone "git@github.com:$*.git" "$(GITHUB_CLONE_TARGET_DIR)/$*"
