## Intro

![](https://img.shields.io/github/go-mod/go-version/iyear/tdl?style=flat-square)
![](https://img.shields.io/github/license/iyear/tdl?style=flat-square)
![](https://img.shields.io/github/workflow/status/iyear/tdl/master%20builder?style=flat-square)
![](https://img.shields.io/github/v/release/iyear/tdl?color=red&style=flat-square)
![](https://img.shields.io/github/last-commit/iyear/tdl?style=flat-square)

📥 Telegram Downloader, but more than a downloader 🚀

> ⚠ Note: Command compatibility is not guaranteed in the early stages of development

## Features

- Single file start-up
- Low resource usage
- Take up all your bandwidth
- Faster than official clients
- Download files from (protected) chats
- Upload files to Telegram

## Preview

It reaches my proxy's speed limit, and the **speed depends on whether you are a premium**

![](img/preview.gif)

## Install

Go to [GitHub Releases](https://github.com/iyear/tdl/releases) to download the latest version

## Usage

```shell
# check the version
tdl version

# use proxy, only support socks now
tdl --proxy socks5://localhost:1080

# specify the account namespace
tdl -n my-tdl

# login your account
tdl login -n iyear

# list your chat
tdl chat ls -n iyear

# download files in url mode, url is the message link
tdl dl url -n iyear -u https://t.me/tdl/1 -u https://t.me/tdl/2

# full examples in download url mode
tdl dl url -n iyear --proxy socks5://localhost:1080 -u https://t.me/tdl/1 -u https://t.me/tdl/2 -s 262144 -t 16 -l 3

# upload files to 'Saved Messages', exclude the specified file extensions
tdl up -n iyear -p /path/to/file -p /path -e .so -e .tmp

# full examples in upload mode
tdl up -n iyear --proxy socks5://localhost:1080 -p /path/to/file -p /path -e .so -e .tmp -s 262144 -t 16 -l 3
```

## Data

Your account information will be stored in the `~/.tdl` directory.

## Commands

Go to [command documentation](docs/command/tdl.md) for full command docs.

## Contribute

- Better command input
- Better interaction
- Better mode support
- ......

Please provide better suggestions or feedback for the project in the form of [SUBMIT ISSUE](https://github.com/iyear/tdl/issues/new)

## LICENSE

AGPL-3.0 License
