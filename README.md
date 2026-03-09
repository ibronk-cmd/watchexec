[![CI status on main branch](https://github.com/watchexec/watchexec/actions/workflows/tests.yml/badge.svg)](https://github.com/watchexec/watchexec/actions/workflows/tests.yml)

# Watchexec

Software development often involves running the same commands over and over. Boring!

`watchexec` is a simple, standalone tool that watches a path and runs a command whenever it detects modifications.

Example use cases:

* Automatically run unit tests
* Run linters/syntax checkers
* Rebuild artifacts


## Features

* Simple invocation and use, does not require a cryptic command line involving `xargs`
* Runs on OS X, Linux, and Windows
* Monitors current directory and all subdirectories for changes
* Coalesces multiple filesystem events into one, for editors that use swap/backup files 

## Quick start

Watch all JavaScript, CSS and HTML files in the current directory and all subdirectories for changes, running `npm run build` when a change is detected:

    $ watchexec -e js,css,html npm run build

Call/restart `python server.py` when any Python file in the current directory (and all subdirectories) changes:

    $ watchexec -r -e py -- python server.py

More usage examples: [in the CLI README](./crates/cli/#usage-examples)!

## Install

<a href="https://repology.org/project/watchexec/versions"><img align="right" src="https://repology.org/badge/vertical-allrepos/watchexec.svg" alt="Packaging 

Watchexec pairs well with:

- [checkexec](https://github.com/kurtbuilds/checkexec): to run only when source files are newer than a target file
- [just](https://github.com/casey/just): a modern alternative to `make`
- [systemfd](https://github.com/mitsuhiko/systemfd): socket-passing in development

## Extend

- [watchexec library](./crates/lib/): to create more specialised watchexec-powered tools.
  - [watchexec-events](./crates/events/): event types for watchexec.
  - [watchexec-signals](./crates/signals/): 
### Downstreams

Selected downstreams of watchexec and associated crates:

