##
# Makefile example to ensure environment variables are present.
#
# https://github.com/SixArm/makefile-examples/tree/main/check-auth0
#
# To run this:
#
#     make
#
# This file is intended to be customized for your own purposes.
##

.PHONY: check-auth0
check-auth0:
ifeq ($(AUTH0_CLIENT_ID),)
	$(warning AUTH0_CLIENT_ID is missing. To get it, visit https://www.auth0.com/)
endif
ifeq ($(AUTH0_CLIENT_SECRET),)
	$(warning AUTH0_CLIENT_SECRET is missing. To get it, visit https://www.auth0.com/)
endif
