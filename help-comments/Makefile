##
# Makefile example to show how to write help comments.
#
# https://github.com/SixArm/makefile-examples/tree/main/help-comments
#
# Each help comment starts with two hash marks, and ends the same way.
# Our hope is this makes it easy for developers to add help information.
#
# Compared to other kinds of well-known make self-documentation tools,
# this implementation is simpler and is also much more flexible.
##

## 
# help: display this help message.
##
.PHONY: help
help:
	@awk '/^##/{a=1-a}a' $(MAKEFILE_LIST) | cut -c3-

##
# You can write help comments anywhere you want,
# such as between tasks, like this help comment.
##

##
# alfa: echo the word alfa.
##
.PHONY: alfa
alfa: 
	@echo "alfa"

##
# You can write anything you want in a help comment,
# such as ASCII art, and whatever you write is displayed.
#
#          ^__^
#          (oo)\_______
#          (__)\       )\/\
#              ||----w |
#              ||     ||
##

## 
# bravo: echo the word bravo.
##
.PHONY: bravo
bravo: 
	@echo "bravo"

# This line is a normal comment.
# This line is another normal comment.
# These normal comments are not printed by the help task.

## 
# charlie: echo the word charlie.
##
.PHONY: charlie
charlie: 
	@echo "charlie"

##
# If you wish, you can end with a footer comment with more information.
# To contact the author, email joel@joelparkerhenderson.com.
##
