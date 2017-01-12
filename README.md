# Greyatom IDE

This repo is fork of https://github.com/learn-co/learn-ide/ modified to used for https://greyatom.com.

[Greyatom IDE](https://greyatom.com/ide) is a fully featured text editor for [Greyatom](https://greyatom.com). It provides a remote development environment to allow users to get started coding using real tools without the pain of setting one up locally. It is built on top of Github's open source [Atom editor](https://atom.io/).

## Project Structure

The Greyatom IDE client is a modified Atom build with two packages injected to provide functionality with a remote backend that provides a ready to go development environment for [Greyatom](https://greyatom.com) users.

**Atom Packages:**

- **[Greyatom IDE](https://github.com/learn-co/learn-ide)** - The main extension
- **[Greyatom IDE Tree](https://github.com/learn-co/learn-ide-tree)** - Our fork of Atom's [tree view](https://github.com/atom/tree-view). Intercepts Atom's file system events and instead performs them on our remote backend.

**Related libraries:**

Those two packages include a couple important libraries:

- **[nsync-fs](https://github.com/learn-co/nsync-fs)** A virtual file system for keeping Atom synced with the remote server
- **[atom-socket](https://github.com/learn-co/atom-socket)** A library for sharing a single websocket connection in Atom packages.

## Getting Started

1. Download [Atom](https://atom.io/)
2. Clone this repo and [learn-ide-tree](https://github.com/learn-co/learn-ide-tree)
3. Run `npm install` in both repos
4. Run `apm link` inside both repos - This will create a sym link to your .atom directory, making the plugin available for use.
5. Open Atom

## Building the Greyatom IDE

`gulp build` - Builds the Atom application with our packages injected ready for distribution and swaps out icons and names to brand it the Greyatom IDE.

## License

Greyatom IDE is [MIT licensed](LICENSE.md)
