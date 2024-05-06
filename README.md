# static-php-cli-hosted
Self-Hosted [static-php-cli](https://github.com/crazywhalecc/static-php-cli) build action.

## Introduction

This repository is used to automatically compile static-php-cli related content for different architectures and operating systems.

Because GitHub's official runners (free) do not support the ARM architecture for Linux, 
they are required to release production-ready binaries such as spc, 
php-cli containing common extensions, etc. 
So the repository is a mix of GitHub Actions' official runner and my local runner to build 
different architecture and OS versions of the same content at the same time.

Because it relies on my local ARM linux vm for build, and the local environment is not a stable cloud server, 
all workflows are currently triggered manually.

## List of Actions

- [Archive download sources weekly](https://github.com/crazywhalecc/static-php-cli-hosted/blob/master/.github/workflows/download-cache.yml)
- [Build PHP - common](https://github.com/crazywhalecc/static-php-cli-hosted/blob/master/.github/workflows/build-php-common.yml)
- [Build PHP - minimal](https://github.com/crazywhalecc/static-php-cli-hosted/blob/master/.github/workflows/build-php-minimal.yml)
- [Build PHP - bulk](https://github.com/crazywhalecc/static-php-cli-hosted/blob/master/.github/workflows/build-php-bulk.yml)
- [Build PHP (Windows) - spc-min](https://github.com/static-php/static-php-cli-hosted/blob/master/.github/workflows/build-php-windows.yml)
- [Extension matrix tests](https://github.com/static-php/static-php-cli-hosted/blob/master/.github/workflows/ext-matrix-tests.yml)
