# Makefile example to ensure environment variables are present.
#
# To run this:
#
#     make
#
# This file is intended to be customized for your own purposes.

.PHONY: vet-auth0
vet-auth0:
ifeq ($(AUTH0_CLIENT_ID),)
	$(warning AUTH0_CLIENT_ID is missing. To get it, visit https://www.auth0.com/)
endif
ifeq ($(AUTH0_CLIENT_SECRET),)
	$(warning AUTH0_CLIENT_SECRET is missing. To get it, visit https://www.auth0.com/)
endif
