# Makefile example to vet (i.e. verify) the system environment.
#
# To run this:
#
#     make
#
# This file is intended to be customized for your own purposes.

.PHONY: vet_env
vet_env: vet_aws vet_auth0 vet_stripe

.PHONY: vet_aws
vet_aws:
ifeq ($(origin AWS_ACCESS_KEY_ID),undefined)
	$(error AWS_ACCESS_KEY_ID undefined. To get it, visit https://aws.amazon.com/)
endif
ifeq ($(origin AWS_SECRET_ACCESS_KEY),undefined)
	$(error AWS_SECRET_ACCESS_KEY is undefined. To get it, visit https://aws.amazon.com/)
endif

.PHONY: vet_auth0
vet_auth0:
ifeq ($(origin AUTH0_CLIENT_ID),undefined)
	$(error AUTH0_CLIENT_ID undefined. To get it, visit https://auth0.com/)
endif
ifeq ($(origin AUTH0_CLIENT_SECRET),undefined)
	$(error AUTH0_CLIENT_SECRET undefined. To get it, visit https://auth0.com/)
endif

.PHONY: vet_stripe
vet_stripe:
ifeq ($(origin STRIPE_API_KEY),undefined)
	$(error STRIPE_API_KEY undefined. To get it, visit https://stripe.com/)
endif
ifeq ($(origin STRIPE_WEBHOOK_SECRET),undefined)
	$(error STRIPE_WEBHOOK_SECRET undefined. To get it, visit https://stripe.com/)
endif

