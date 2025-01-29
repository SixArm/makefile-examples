##
# Makefile example to ensure environment variables are present.
#
# https://github.com/SixArm/makefile-examples/tree/main/vet-stripe
#
# To run this:
#
#     make
#
# This file is intended to be customized for your own purposes.
##

.PHONY: vet-stripe
vet-stripe:
ifeq ($(STRIPE_API_KEY),)
	$(warning STRIPE_API_KEY is missing. To get it, visit https://stripe.com/)
endif
ifeq ($(STRIPE_WEBHOOK_SECRET),)
	$(warning STRIPE_WEBHOOK_SECRET is missing. To get it, visit https://stripe.com/)
endif
