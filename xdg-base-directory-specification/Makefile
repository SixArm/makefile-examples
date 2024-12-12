## 
# Makefile example: XDG Base Directory Specification
#
# https://github.com/SixArm/makefile-examples/tree/main/xdg-base-directory-specification
#
# $XDG_CONFIG_HOME defines the base directory relative to which user-specific configuration files should be stored. 
# If $XDG_CONFIG_HOME is either not set or empty, a default equal to $HOME/.config should be used.
#
# $XDG_DATA_HOME defines the base directory relative to which user-specific data files should be stored. 
# If $XDG_DATA_HOME is either not set or empty, a default equal to $HOME/.local/share should be used.
#
# $XDG_STATE_HOME defines the base directory relative to which user-specific state files should be stored. If 
# $XDG_STATE_HOME is either not set or empty, a default equal to $HOME/.local/state should be used. 
##

XDG_CONFIG_HOME ?= $(HOME)/.config
XDG_DATA_HOME ?= $(HOME)/.local/share
XDG_STATE_HOME ?= $(HOME)/.local/state

##
# xdg: Make the XDG base directories.
##
xdg: $(XDG_CONFIG_HOME) $(XDG_DATA_HOME) $(XDG_STATE_HOME)
	$(info XDG_CONFIG_HOME: $(XDG_CONFIG_HOME))
	$(info XDG_DATA_HOME: $(XDG_DATA_HOME))
	$(info XDG_STATE_HOME: $(XDG_STATE_HOME))

##
# $(XDG_CONFIG_HOME): make the directory.
##
$(XDG_CONFIG_HOME):
	mkdir -p "$(XDG_CONFIG_HOME)"

##
# $(XDG_DATA_HOME): make the directory.
##
$(XDG_DATA_HOME):
	mkdir -p "$(XDG_DATA_HOME)"

##
# $(XDG_STATE_HOME): make the directory.
##
$(XDG_STATE_HOME):
	mkdir -p "$(XDG_STATE_HOME)"
