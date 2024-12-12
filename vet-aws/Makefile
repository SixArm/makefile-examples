##
# Makefile example to ensure environment variables are present.
#
# https://github.com/SixArm/makefile-examples/tree/main/vet-aws
#
# To run this:
#
#     make
#
# This file is intended to be customized for your own purposes.
##

.PHONY: vet-aws
vet-aws: vet-aws-cli vet-aws-ses

.PHONY: vet-aws-cli
vet-aws-cli:
ifeq ($(AWS_ACCESS_KEY_ID),)
	$(warning AWS_ACCESS_KEY_ID is missing. To get it, visit https://aws.amazon.com/)
endif
ifeq ($(AWS_SECRET_ACCESS_KEY),)
	$(warning AWS_SECRET_ACCESS_KEY is missing. To get it, visit https://aws.amazon.com/)
endif
ifeq ($(AWS_SESSION_TOKEN),)
	$(warning AWS_SESSION_TOKEN is missing. To get it, visit https://aws.amazon.com/)
endif

.PHONY: vet-aws-ses
vet-aws-ses:
ifeq ($(SES_SMTP_USERNAME),)
	$(warning SES_SMTP_USERNAME is missing. To get it, visit https://aws.amazon.com/)
endif
ifeq ($(SES_SMTP_PASSWORD),)
	$(warning SES_SMTP_PASSWORD is missing. To get it, visit https://aws.amazon.com/)
endif
ifeq ($(SES_SMTP_SERVER),)
	$(warning SES_SMTP_SERVER is missing. To get it, visit https://aws.amazon.com/)
endif
