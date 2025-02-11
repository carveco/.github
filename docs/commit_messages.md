<!-- omit in toc -->
# Writing commit messages

- [Introduction](#introduction)
- [Overall Style](#overall-style)
- [🙂 Emoji](#-emoji)
  - [Examples](#examples)
- [🔨 Refactoring](#-refactoring)
  - [Examples](#examples-1)

## Introduction

This page provides guidance for composing commit messages across the
organisation.

## Overall Style

* [How to Write a Git Commit Message](https://cbea.ms/git-commit/)

## 🙂 Emoji

Commit message titles may begin with an emoji. If they do, the meaning should
be roughly consistent with other commits by following the chart below.

Emoji may compress extra information in a limited space (50 characters) and set
expectations about what the commit contains. For example, a refactoring or
performance improvement shouldn't change functionality.


| Commit type                | Emoji | Equivalent Markdown tag           |
| :------------------------- | :---- | :-------------------------------- |
| New feature                | ✨     | `:sparkles:`                      |
| Bugfix                     | 🐛     | `:bug:`                           |
| Documentation              | 📃     | `:page_with_curl:`                |
| Performance                | 🏇     | `:horse_racing:`                  |
| Cosmetic (UI)              | 💄     | `:lipstick:`                      |
| Tests                      | 🚨     | `:rotating_light:`                |
| Adding a test              | 🧪     | `:test_tube:`                     |
| Make a test pass           | ✅     | `:white_check_mark:`              |
| General update             | ⚡     | `:zap:`                           |
| Improve code formatting    | 🎨     | `:art:`                           |
| Lint                       | 👕     | `:shirt:`                         |
| Refactor code              | 🔨     | `:hammer:`                        |
| Tidy/improve readability   | 🧹     | `:broom:`                         |
| Removing code/files        | 🔥     | `:fire:`                          |
| Continuous Integration     | 👷     | `:construction_worker:`           |
| Security                   | 🔒     | `:lock:`                          |
| Translation                | 🌐     | `:globe_with_meridians:`          |
| Text (UI)                  | 📝     | `:pencil:`                        |
| Critical hotfix            | 🚑     | `:ambulance:`                     |
| Publish release            | 🚀     | `:rocket:`                        |
| Fixing on Linux            | 🐧     | `:penguin:`                       |
| Add feature flag           | 🏁     | `:checkered_flag:`                |
| Work in progress           | 🚧     | `:construction:`                  |
| Analytics or tracking code | 📈     | `:chart_with_upwards_trend:`      |
| Removing a dependency      | ➖     | `:heavy_minus_sign:`              |
| Adding a dependency        | ➕     | `:heavy_plus_sign:`               |
| Upgrading dependencies     | ⬆️     | `:arrow_up:`                      |
| Downgrading dependencies   | ⬇️     | `:arrow_down:`                    |
| Docker                     | 🐳     | `:whale:`                         |
| Configuration files        | 🔧     | `:wrench:`                        |
| Bad code / need improv.    | 💩     | `:hankey:`                        |
| Reverting changes          | ⏪     | `:rewind:`                        |
| Accessibility              | ♿     | `:wheelchair:`                    |
| Move/rename                | 🚚     | `:truck:`                         |
| Other                      |       | Create a PR to suggest something! |

Based on
[`parmentf/GitCommitEmoji.md`](https://gist.github.com/parmentf/035de27d6ed1dce0b36a),
with inspiration from
[`dannyfritz/commit-message-emoji`](https://github.com/dannyfritz/commit-message-emoji),
[`gitmoji`](https://gitmoji.carloscuesta.me/) and [`Git-Emoji`](https://babakks.github.io/article/2020/07/03/emojis-in-git-commit-messages.html).

Use the key combination 🪟+. (windows key and dot) to show the Windows emoji picker
(works in the major web browsers, code editors, and terminal).

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
