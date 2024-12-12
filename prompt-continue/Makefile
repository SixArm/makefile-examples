##
# Makefile example of a prompt that asks if the user wants to continue.
#
# https://github.com/SixArm/makefile-examples/tree/main/prompt-continue
#
# To run this:
#
#     make example
#
# This file is intended to be customized for your own purposes.
##

.PHONY: example
example:
	@printf %s "Continue? [y/n] " && read x && [ $$x = y ]
	@echo "Answer is yes."
