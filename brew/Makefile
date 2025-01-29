##
# Makefile example: get macOS brew package manager then install packages.
#
# https://github.com/SixArm/makefile-examples/tree/main/brew
##

##
# brew: do all our brew-* tasks.
##
.PHONY: brew
brew: brew-command brew-path-in-zshrc brew-update brew-install-favorites brew-install-postgresql-build-dependencies

##
# brew-command: if the brew command is available, then OK, else install it.
##
.PHONY: brew-command  brew-update brew-install-favorites brew-install-postgresql-build-dependencies
brew-command:
	command -v brew >/dev/null 2>&1 || /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

##
# brew-path-in-zshrc: Ensure that the typical brew path env var export for /usr/local/bin is in ~/.zshrc
##
.PHONY: brew-path-in-zshrc
brew-path-in-zshrc: brew-command
	$(shell test -e "$$HOME/.zshrc" && grep -q "/usr/local/bin:" "$$HOME/.zshrc" || echo 'export PATH="/usr/local/bin:$$PATH"' >> "$$HOME/.zshrc" && . "$$HOME/.zshrc")

##
# brew-upgrade: run the brew upgrade commands, to upgrade everything.
##
.PHONY: brew-upgrade
brew-upgrade:
	brew upgrade --greedy
	brew upgrade --greedy --cask

##
# brew-install: do all our brew-install-* tasks.
##
.PHONY: brew-install
brew-install: brew-install-favorites brew-install-postgresql-build-dependencies

##
# brew-install-favorites: install our favorite packages.
##
.PHONY: brew-install-favorites
brew-install-favorites:
	brew install bat moreutils tmux vim

##
# brew-install-postgresql-build-dependencies: install packages that are
# needed by PostgreSQL when we building it from scratch or via mise/asdf.
##
.PHONY: brew-install-postgresql-build-dependencies
brew-install-postgresql-build-dependencies:
	brew install gcc readline zlib curl openssl ossp-uuid icu4c pkg-config
