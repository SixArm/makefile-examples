##
# Makefile example to ensure environment variables are present.
#
# https://github.com/SixArm/makefile-examples/tree/main/check-openai
#
# To run this:
#
#     make
#
# This file is intended to be customized for your own purposes.
##

.PHONY: check-openai
check-openai:
ifeq ($(OPENAI_API_TOKEN),)
	$(warning OPENAI_API_TOKEN is missing. To get it, visit https://www.openai.com/)
endif
