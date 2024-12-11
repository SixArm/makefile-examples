## 
# mise: Use mise, which is is a polyglot tool version manager. 
#
# This task checks for the command `mise` on your system path.
# If the command is not found, then this task installs it by
# using the typical mise cross-platform install process.
#
# The mise website:
# https://mise.jdx.dev/
#
#   * mise enables you to install software in easy ways;
#     mise can replaces tools like asdf, nvm, pyenv, rbenv, etc.
#
#   * mise enables you to switch sets of env vars in different projects;
#     mise can replace direnv for many developer project needs.
#
#   * mise is cross-platform, and works on Linux, macOS, and Windows;
#     mise can supplement macOS brew for many developer project needs.
#
#   * mise is a task runner that can run linters, tests, builders, servers.
#     mise can replace make, or just, or npm scripts.
##
.PHONY: mise
mise: mise-install mise-zshrc

##
# mise-install: Install mise from the website using the typical process.
#
.PHONY: mise-install
mise-install:
	$(shell command -v "$$HOME/.local/bin/mise" >/dev/null 2>&1 || curl https://mise.run | sh)
	$$HOME/.local/bin/mise --version

##
# mise-zshrc: Activate mise in your shell file ~/.zshrc.
#
# The goal is to add this line:
#
#     eval "$($HOME/.local/bin/mise activate zsh)"
#
# The line activates mise whenever you launch your your shell,
# which makes mise run automatically as you work in projects.
##
.PHONY: mise-zshrc
mise-zshrc:
	$(shell grep -q "\$$HOME/.local/bin/mise activate zsh" "$$HOME/.zshrc" || echo "eval \"\$$(\$$HOME/.local/bin/mise activate zsh)\"" >> "$$HOME/.zshrc")
