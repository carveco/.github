<!-- omit in toc -->
# Writing commit messages

- [Introduction](#introduction)
- [Overall Style](#overall-style)
- [Format](#format)
  - [Default](#default)
  - [PR/Merge Commit](#prmerge-commit)
  - [Revert Commit](#revert-commit)
- [🙂 Emoji](#-emoji)
  - [Examples](#examples)
- [🔨 Refactoring](#-refactoring)
  - [Examples](#examples-1)
  - [Attributions](#attributions)

## Introduction

This page provides guidance for composing commit messages across the
organisation.

## Overall Style

* [How to Write a Git Commit Message](https://cbea.ms/git-commit/)

## Format

### Default

```
<emoji> <The description>
```

### PR/Merge Commit

```
<emoji> <task id>: <The description>
```

### Revert Commit

```
⏪ Revert "<reverted commit subject line>"
```

## 🙂 Emoji

All commits should start with a single emoji signifying the type of change. Use
the key combination 🪟+. (windows key and dot) to show the Windows emoji picker.

The following chart outlines the most common types of emojis used. Try to use
the emojis on the list where possible. Each type roughly corresponds the
[conventional commit
types](https://gist.github.com/qoomon/5dfcdf8eec66a051ecd85625518cfd13#types),
but with emojis.

| Commit type | Emoji | Emoji picker description |
| :---------- | :---: | :----------------------- |
| `feat`      |   ✨   | sparkles                 |
| `fix`       |   🐛   | bug                      |
| `refactor`  |   🔨   | hammer                   |
| `perf`      |   🚤   | speed boat               |
| `style`     |   👕   | t-shirt                  |
| `test`      |   🧪   | test tube                |
| `docs`      |   📃   | page with curl           |
| `build`     |   🛠️   | hammer and wrench        |
| `ops`       |   👷   | construction worker      |
| `chore`     |   🧹   | broom                    |

Aside from the common list of emojis above we also have these specific emojis
for other types of commits:

| Commit type  | Emoji | Emoji picker description |
| :----------- | :---: | :----------------------- |
| `remove`     |   🔥   | fire                     |
| `move`       |   🚚   | delivery truck           |
| `translate`  |   🌐   | globe with meridians     |
| `hotfix`     |   🚑   | ambulance                |
| `release`    |   🚀   | rocket                   |
| `revert`     |   ⏪   | rewind                   |
| `wip`        |   🚧   | construction             |
| do not merge |   💀   | skull                    |

### Examples

* 🔨 Inline typedef: d2rReaderInfoList [3277c7a](https://github.com/carveco/carveco/commit/3277c7a6f368102e393d01fefc87b3914d063e9a)
* 🐛 Fix Rope Creator [beb4cfe](https://github.com/carveco/carveco/commit/beb4cfe3f3f6ccc87731438dfcc5fe0523cb0efe)
* 🌐 Update localizations [503bddd](https://github.com/carveco/carveco/commit/503bddd9e795b1a18a1fd49cea0dabef40dda38f)

## 🔨 Refactoring

The [Refactoring Catalog](https://refactoring.com/catalog/) is an excellent
basis for describing refactorings because of its foundation in software
engineeering literature. The patterns help decompose complex refactorings into
smaller, more manageable steps. The changes are easier to verify and require a
less in-depth understanding of the code being modified.

Here are some particularly common or helpful refactorings:
* Extract function
* Inline function
* Remove dead code
* Rename variable
* Slide statements
* Parameterize function
* Move statements to callers

The current way we use the catalog is to follow the appropriate emoji (usually
🔨 or 🔥) with the pattern name, followed by the location in code (to make it
easier to distinguish what was being changed).

### Examples

* 🔨 Inline function: check_dog_beagle_collar()
* 🔨 Rename variable: better_name
* 🔥 Remove dead code: GetWorkplaneManagerObject()

### Attributions

* [Conventional Commits](https://www.conventionalcommits.org/)
* [Conventional Commits Cheatsheet ](https://gist.github.com/qoomon/5dfcdf8eec66a051ecd85625518cfd13)
* [`parmentf/GitCommitEmoji.md`](https://gist.github.com/parmentf/035de27d6ed1dce0b36a)
* [`dannyfritz/commit-message-emoji`](https://github.com/dannyfritz/commit-message-emoji)
* [`gitmoji`](https://gitmoji.carloscuesta.me/)
* [`Git-Emoji`](https://babakks.github.io/article/2020/07/03/emojis-in-git-commit-messages.html)
