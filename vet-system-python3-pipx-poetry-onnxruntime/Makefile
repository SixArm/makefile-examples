# Makefile example to vet (i.e. verify) installed software versions.
#
#   * operating system e.g. macOS-based Darwin or Debian-based Linux.
#   * python3 programming language
#   * pipx runtime tool
#   * poetry dependency manager
#   * onnxruntime open neural network exchange
#
# To run this:
#
#     make vet
#
# This example is intended to demonstrate various kinds of tools,
# and how to get their version numbers, and how to show error help.
#
# This file is intended to be customized and changed,
# such as by adjusting each tool's version number,
# and by adding/removing tools that you want to vet.

# Change this section to set the versions that you expect.
.PHONY: vet
vet::
darwin_version_must_equal := 24.1.0
debian_version_must_equal := 6.1.0-13-arm64
python3_version_must_equal := 3.13.0
pipx_version_must_equal := 1.7.1
poetry_version_must_equal := 1.8.4
onnxruntime_version_must_equal := 1.20.1

# Customize this line to call whichever tools you wish.
#
# Be aware that the order matters, so be sure to vet the
# lower-level dependencies before higher-level dependencies.
#
vet:: vet_system vet_python3 vet_pipx vet_poetry vet_onnxruntime

# Vet the operating system release version.
#
# Currently this task expects macOS 15 Darwin or Debian 12 Linux,
# and otherwise skips the vet. We welcome help to add more systems.
#
.PHONY: vet_system
vet_system:
uname_S := $(shell sh -c 'uname -s 2>/dev/null || echo not')
uname_R := $(shell sh -c 'uname -r 2>/dev/null || echo not')
ifeq ($(uname_S),Darwin)
ifneq ($(uname_R),$(darwin_version_must_equal))
$(error Darwin release version mismatch: actual: ${uname_R}, expect: ${darwin_version_must_equal}. Try running: "uname -r")
endif
endif
ifeq ($(uname_S),Linux)
ifneq ($(debian_version),$(debian_version_must_eq))
$(error Debian release version mismatch: actual: ${uname_R}, expect: ${debian_version_must_equal}. Try running: "uname -r")
endif
endif
$(info Found ${uname_S} ${uname_R})

# Vet python3 programming language.
#
# Be aware that some systems call this "python" not "python3".
# If so, you'll want to rename this task and its variables.
#
.PHONY: vet_python3
vet_python3:
ifeq (, $(shell which python3))
$(error Missing program: python3. To install, try via https://www.python.org/ or Nix or macOS "brew install python3" or Debian "apt-get install python3")
endif
python3_version := $(shell sh -c 'python3 -c "import platform; print(platform.python_version())" 2>/dev/null || echo error')
ifneq ($(python3_version),$(python3_version_must_equal))
$(error python3 version mismatch: actual: ${python3_version}, expect: ${python3_version_must_equal}. Try running: "python3 --version")
endif
$(info Found python3 ${python3_version})

# Vet pipx runtime tool.
#
# This tool has various ways to install it, and versions might vary.
# If you need multiple ways, then you'll want to enhance this task.
#
.PHONY: vet_pipx
vet_pipx:
ifeq (, $(shell which pipx))
$(error Missing program: pipx. To install, try https://pipx.pypa.io/ or Nix or macOS "brew install pipx" or Debian "apt-get install pipx")
endif
pipx_version := $(shell sh -c 'pipx --version 2>/dev/null || echo error')
ifneq ($(pipx_version),$(pipx_version_must_equal))
$(error pipx version mismatch: actual: ${pipx_version}, expect: ${pipx_version_must_equal}. Try running: pipx --version")
endif
$(info Found pipx ${pipx_version})

# Vet poetry dependency manager.
#
# This tool has various ways to install it, and versions might vary.
# If you need multiple ways, then you'll want to enhance this task.
#
# Be aware we've previously hit glitches with poetry when using macOS
# and brew for poetry. Currently we prefer installing poetry via pipx.
#
.PHONY: vet_poetry
vet_poetry:
ifeq (, $(shell which poetry))
$(error Missing program: poetry. To install, try https://python-poetry.org/ or Nix or "pipx install poetry" or or macOS "brew install poetry" or Debian "apt-get install poetry")
endif
poetry_version := $(shell sh -c 'poetry --version | sed "s/.*(version //; s/).*//;" 2>/dev/null || echo error')
ifneq ($(poetry_version),$(poetry_version_must_equal))
$(error poetry version mismatch: actual: ${poetry_version}, expect: $(poetry_version_must_equal). Try running: poetry --version)
endif
$(info Found poetry ${poetry_version})

# Vet onnxruntime open neural network exchange.
#
# This tool has various ways to install it, and is notably different
# depending on the operating system, CPU architecture, and programming
# language. 
#
# This task example is implemented to vet that onnxruntime is installed
# via python3 pipx, and is available for python3 scripts to import.
#
.PHONY: vet_onnxruntime
vet_onnxruntime:
ifeq (, $(shell python3 -c "import onnxruntime" 2>/dev/null))
$(error Missing library: onnxruntime. To install, try https://onnxruntime.ai/ or Nix or macOS "brew install onnxruntime" or Debian "apt-get install onnxruntime")
endif
onnxruntime_version := $(shell sh -c 'python3 -c "import onnxruntime; print(onnxruntime.__version__)" 2>/dev/null || echo error')
ifneq ($(onnxruntime_version),$(onnxruntime_version_must_equal))
$(error onnxruntime version mismatch: actual: ${onnxruntime_version}, expect: ${onnxruntime_version_must_equal}. Try running: python3 -c "import onnxruntime; print(onnxruntime.__version__))
endif
$(info Found onnxruntime ${onnxruntime_version})
