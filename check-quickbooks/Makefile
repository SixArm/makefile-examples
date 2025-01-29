##
# Makefile example to ensure environment variables are present.
#
# https://github.com/SixArm/makefile-examples/tree/main/check-quickbooks
#
# To run this:
#
#     make
#
# This file is intended to be customized for your own purposes.
##

.PHONY: check-quickbooks
check-quickbooks: check-quickbooks-client check-quickbooks-target

check-quickbooks-client:
ifeq ($(QUICKBOOKS_CLIENT_ID),)
	$(warning QUICKBOOKS_CLIENT_ID is missing. To get it, visit https://developer.intuit.com/)
endif
ifeq ($(QUICKBOOKS_CLIENT_SECRET),)
	$(warning QUICKBOOKS_CLIENT_SECRET is missing. To get it, visit https://developer.intuit.com/)
endif

.PHONY: check-quickbooks-target
check-quickbooks-target:
ifeq ($(QUICKBOOKS_ENVIRONMENT),)
	$(warning QUICKBOOKS_ENVIRONMENT is missing. To get it, visit https://developer.intuit.com/)
endif
ifeq ($(QUICKBOOKS_BASE_URL),)
	$(warning QUICKBOOKS_BASE_URL is missing. To get it, visit https://developer.intuit.com/)
endif
ifeq ($(QUICKBOOKS_REDIRECT_URI),)
	$(warning QUICKBOOKS_REDIRECT_URI is missing. To get it, visit https://developer.intuit.com/)
endif
