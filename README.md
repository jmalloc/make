# Icecave Makefiles

This repository contains common Makefile configurations used by Icecave projects.

**The contents is not intended to be used by third-parties and may change at any
time without notice.**

# Setup

- Include `artifacts/make/<lang>.mk` in the top of your project's `Makefile`.
- Add a target that fetches the `Makefile` from GitHub.

The example below fetches the Makefile for the Go language.

```Makefile
SHELL := /bin/bash
-include artifacts/make/go.mk

artifacts/make/%.mk:
	bash <(curl -s https://icecave.github.io/make/install) $*
```
