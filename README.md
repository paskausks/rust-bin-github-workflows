# Github Actions for Rust binaries

A Sample Rust binary project for matrix-testing, building and packaging Rust binary projects.

## Workflows

This project contains two workflows - CI and release.

### CI

This workflow is meant for pushes to the master branch and for pull requests.

It will:

* Cache dependencies
* Build and test the debug binary on Ubuntu, MacOS and Windows Server using the current stable version of Rust.
* Run clippy and rustfmt

### Create release

This workflow will be triggered when a pushed tag matches v*, i.e. v1.0, v20.15.10

It will:

* Cache dependencies
* Build the release binary on Ubuntu, MacOS and Windows Server using the current stable version of Rust.
* Create archives for the built release artifacts (_tar.gz_ for Linux and _zip_ for Windows and MacOS.)
* Uploads the created archives as artifacts.

## Setup

Set the `env.RELEASE_BIN` name in _.github/workflows/release.yml_ (excluding any extension) and verify that the additional paths in `env.RELEASE_ADDS` are correct.
