# begone

_A fully automatic spamming tool, created for the sole purpose of
obliterating conversation threads on
[Facebook Messenger](https://messenger.com)._

[![Github Release][release-img]][release]
[![Go Report Card][grp-img]][grp]

Works with individual conversations as well as group threads—a real versatile
beast. Uses a modified version of
[`unixpickle/fbmsgr`](https://github.com/unixpickle/fbmsgr) as the underlying
Messenger client. And, like all my CLI programs, written in
[Go](https://golang.org).

<br />
<p align="center">
  <img src="./.github/demo.gif" width=600>
</p>

## Features
* `begone emojify` – send streams of emojis, en masse
* `begone repeat` – keep repeating a message
* `begone file` – read a file line-by-line to someone
* `begone image` – continually send an image

## Usage

### Installation

#### Using Homebrew:

If you're on macOS and have [Homebrew](https://brew.sh), you're in luck! Just
run:

```bash
brew install stevenxie/tap/begone
```

This will install `begone` from the Homebrew tap
[`stevenxie/tap`](https://github.com/stevenxie/homebrew-tap).

#### Manually:

Grab the [latest release](https://github.com/stevenxie/begone/releases) compiled
for your system.

Ensure that the binary is executable, and place it somewhere in your `$PATH`.
For macOS users, this might look something like this:

```bash
$ mv ~/Downloads/begone-darwin-x64 /usr/local/bin/begone
$ chmod u+x /usr/local/bin/begone
```

### Running

```bash
## (Optional) save login credentials to ~/.begone.json.
$ begone login

## Launch an emoji attack on a conversation thread.
$ begone emojify
Enter the target conversation URL (https://messenger.com/t/...):
https://messenger.com/t/exampleid

## See all options.
$ begone help
$ begone help <command>  # i.e. begone help emojify
```

<br />

## Advanced Usage

### Making from source

> This requires the [Go](https://golang.org) language and associated toolchain
> to be installed. If you're on macOS, this may be as easy as
> `brew install go`!

```bash
## Clone this repository.
$ git clone git@github.com:stevenxie/begone.git
$ cd begone

## Install module dependencies.
$ make dl # (or go mod download)

## Compile and install a version for your machine.
$ make install  # (or go install)
```

## TODOs

- [x] (maybe) Implement attacks using local files (images)?
- [x] Add more emojis to the `Emojifier` generator.
- [x] Create different interaction implementations for Windows (the spinners
      and attack text look kinda funky).

[grp]: https://goreportcard.com/report/github.com/stevenxie/begone
[grp-img]: https://goreportcard.com/badge/github.com/stevenxie/begone
[release]: https://github.com/stevenxie/begone/releases
[release-img]: https://img.shields.io/github/release/stevenxie/begone.svg
