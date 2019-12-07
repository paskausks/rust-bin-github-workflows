# Github Actions for Rust binaries

A Sample Rust binary project for matrix-testing, building and packaging Rust binary projects.

## Workflows

This project contains two workflows - CI and release.

### CI

This workflow is meant for pushes to the master branch and for pull requests.

It will:

* Cache dependencies
* Build and test the debug binary on Ubuntu, MacOS and Windows Server.
* Run clippy and rustfmt
