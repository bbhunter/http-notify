# `http-notify`

<br>

<p align="left">
  <a href="https://img.shields.io/badge/Branch-master-green.svg">
    <img src="https://img.shields.io/badge/Branch-master-green.svg"
        alt="Branch">
  </a>
  <a href="https://img.shields.io/badge/Version-v1.0.0-lightgrey.svg">
    <img src="https://img.shields.io/badge/Version-v1.0.0-lightgrey.svg"
        alt="Version">
  </a>
  <a href="https://github.com/trimstray/http-notify">
    <img src="https://github.com/trimstray/http-notify.svg?branch=master"
        alt="Travis-CI">
  </a>
  <a href="http://www.gnu.org/licenses/">
    <img src="https://img.shields.io/badge/license-GNU-blue.svg"
        alt="License">
  </a>
</p>

<br>

## Description

**http-notify** - keep track of all http activities.

  > Before use **http-notify** please see **[Requirements](#requirements)**.

## How To Use

It's simple:

```bash
# Clone this repository
git clone https://github.com/trimstray/http-notify

# Go into the repository
cd http-notify

# Install
./setup.sh install

# Run the app
http-notify <params>
```

> * symlink to `bin/http-notify` is placed in `/usr/local/bin`
> * man page is placed in `/usr/local/man/man8`

## External tools

**http-notify** support external tools for security scans:

## Requirements

This tool working with:

- **GNU/Linux** (testing on Debian and CentOS)
- **[Bash](https://www.gnu.org/software/bash/)** (testing on 4.4.19)

## Parameters

Provides the following options:

```bash
    http-notify v1.0.0

Usage:
    http-notify <option|long-option>

  Examples:
    http-notify --help

  Options:
        --help                                show this message
```

## Contributing

See **[this](CONTRIBUTING.md)**.

## License

GPLv3 : <http://www.gnu.org/licenses/>

**Free software, Yeah!**
