# ATTW-Before-Publish

Run Are-The-Types-Wrong as a precheck for npm pack or npm publish

[![npm version](https://img.shields.io/npm/v/attw-before-publish.svg)](https://www.npmjs.com/package/attw-before-publish)
[![readme](https://img.shields.io/badge/-readme-informational)](https://github.com/spautz/attw-before-publish/blob/main/packages/attw-before-publish/README.md)
[![build status](https://github.com/spautz/attw-before-publish/workflows/CI/badge.svg)](https://github.com/spautz/attw-before-publish/actions)
[![test coverage](https://img.shields.io/coveralls/github/spautz/attw-before-publish/main.svg)](https://coveralls.io/github/spautz/attw-before-publish?branch=main)
[![repo vulnerabilities](https://snyk.io/test/github/spautz/attw-before-publish/badge.svg)](https://snyk.io/test/github/spautz/attw-before-publish)
[![gzip size](https://img.shields.io/bundlephobia/minzip/attw-before-publish.svg)](https://bundlephobia.com/package/attw-before-publish@latest)

## NOT YET READY

This package is under active development, as of February 2024.

## Overview

[AreTheTypesWrong](https://arethetypeswrong.github.io/) ([`@arethetypeswrong/cli`](https://www.npmjs.com/package/@arethetypeswrong/cli))
is an excellent tool for validating a npm package's typings, but it operates on a packed (gzipped) package. This makes
it difficult to run AreTheTypesWrong as part of `pack` or `publish`

`attw-before-publish` provides commands that validate the package while performing the `pack` or `publish` commands:

- `attw-pack` runs `npm pack` and validates the resulting `[package-name].tgz`
- `attw-publish` runs `npm pack`, validates the resulting `[package-name].tgz`, and then proceeds with the publish it if it is valid
