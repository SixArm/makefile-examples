##
# Makefile example: Coach a user how to onboard onto a project, team, etc.
#
# https://github.com/SixArm/makefile-examples/tree/main/onboard
#
# These tasks simply print items for the user to read.
#
# These tasks don't have any other effects, such as creating accounts.
#
# A real-world project would make each of these tasks have real effects.
##

.PHONY: onboard
onboard: onboard-header onboard-email onboard-discord onboard-linear onboard-figma onboard-system onboard-github onboard-aws

.PHONY: onboard-header
onboard-header:
	$(info Onboard tasks for you to do before you continue:)

.PHONY: onboard-email
onboard-email:
	$(info - [ ] Get your organization email address, then read your email messages.)

.PHONY: onboard-discord
onboard-discord:
	$(info - [ ] Join our Discord for chat, then visit the channel #onboard and say hi.)

.PHONY: onboard-linear
onboard-linear:
	$(info - [ ] Join our Linear for tasks, then create any task that helps us improve.)

.PHONY: onboard-figma
onboard-figma:
	$(info - [ ] Join our Figma for UI/UX, then see project name "onboard" and learn it.)

.PHONY: onboard-system
onboard-system:
	$(info - [ ] Create a fresh computer system user account, then do any system updates.)

.PHONY: onboard-github
onboard-github:
	$(info - [ ] Get your GitHub account, then view our GitHub organization page.)

.PHONY: onboard-aws
onboard-aws:
	$(info - [ ] Get your Amazon Web Services account, then sign in with AWS IAM SSO.)
