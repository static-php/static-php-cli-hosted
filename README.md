# static-php-cli-hosted
Self-Hosted static-php-cli build action.

## Introduction

This repository is used to automatically compile static-php-cli related content for different architectures and operating systems.

Because GitHub's official runners (free) do not support the ARM architecture, 
they are required to release production-ready binaries such as spc, 
php-cli containing common extensions, etc. 
So the repository is a mix of GitHub Actions' official runner and my local runner to build 
different architecture and OS versions of the same content at the same time.

Because it relies on my local ARM device for build, and the local environment is not a stable cloud server, 
all workflows are currently triggered manually.

## List of Actions

- [Build spc binary files](https://github.com/crazywhalecc/static-php-cli-hosted/blob/master/.github/workflows/build-spc-release.yml)
- [Build PHP with common extensions](https://github.com/crazywhalecc/static-php-cli-hosted/blob/master/.github/workflows/build-php-common.yml)
