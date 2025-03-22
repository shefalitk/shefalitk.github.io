---
title: "gridparse"
collection: software
permalink: /software/gridparse
excerpt: 'An ArgumentParser that supports your grid-search needs.'
date: 2025-03-18
codelink: https://github.com/gchochla/gridparse
---

<img src="https://gchochla.github.io/images/gridparse.svg" style="display: block; margin-left: auto; margin-right:auto; width: 50%; height: auto;">
<br>

`gridparse` is a lightweight (only dependency is `omegaconf` which also downloads yaml) `ArgumentParser` - aka `GridArgumentParser` - that supports your grid-search needs. Supports top-level parser and subparsers. Configuration files of any type (using `omegaconf`) are also supported through the argument `--gridparse-config` (also available with underscore `_`), where multiple configuration files can be passed and parsed.

To install: `pip install gridparse`
