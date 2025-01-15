<!-- omit in toc -->
# Code Review Etiquette

- [Introduction](#introduction)
- [Review Status](#review-status)
- [Giving Reviews](#giving-reviews)
  - [Label Comment Severity](#label-comment-severity)
- [Responding to Reviews](#responding-to-reviews)
- [Recommended Tools](#recommended-tools)
  - [GitHub CLI](#github-cli)
  - [VS Code Extension](#vs-code-extension)
  - [Browser Extension](#browser-extension)


## Introduction

This document outlines shared practices we use for creating and giving feedback
for pull requests. Much inspiration has been taken from two excellent sources,
which are recommended reading.

[Google's Code Review Guidelines](https://google.github.io/eng-practices/)
provides very practical advice towards making changes and giving reviews, whilst
[Chapter 14: Code Review from "Software Engineering at
Google"](https://abseil.io/resources/swe-book/html/ch09.html) dives into the
theoretical and philosophical motivations.

## Review Status

If a pull request is in draft, typically feedback will only be given if
explicitly requested. 

[Assignees](https://docs.github.com/en/issues/tracking-your-work-with-issues/using-issues/assigning-issues-and-pull-requests-to-other-github-users)
are used to communicate who is actively looking at a pull request. This should
flip between the author and reviewer as changes are requested.

If you have someone specific who you'd like to review your change then [request
their
review](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/requesting-a-pull-request-review).

## Giving Reviews

Check for unassigned open PRs during [break
points](https://google.github.io/eng-practices/review/reviewer/speed.html#interruption).
This could be when your current coding task is completed, after lunch, returning
from a meeting, coming back from the breakroom, etc.

A code review should [start by considering the broad implications of the
change](https://google.github.io/eng-practices/review/reviewer/navigate.html#step_one).
Does the approach make sense? Is the change too large for a single review, or
are there prior refactoring or cleanup steps that would make the change easier
to understand? Is there context behind the change that has not been provided in
the PR description?  
Under these circumstances, a "request changes" should be left and the author
given an opportunity to rectify before any further review.

Once a review has been deemed as appropriate, then a more detailed review can be
given with an "approve" or "request changes" outcome. Reviewers should avoid
responding in piecemeal fashion, as the author may consider all comments to
decide how best to tackle the feedback. When changes are requested the
assignment should flip to the PR author and it is best practice to `@mention`
them in the review comment so they are alerted on Slack.

A review should only be approved if the reviewer is happy for the change to be
merged without any comments being addressed. For approved PRs with no pending
requests, it is the onus of the reviewer to merge the PR. Otherwise it is the
author's choice to address any comments before merging the PR.

### Label Comment Severity

[Label the severity of your comments, differentiating required changes from
guidelines or
suggestions](https://google.github.io/eng-practices/review/reviewer/comments.html#label-comment-severity).
Here are some examples:

> Praise: [Appreciation for good practices, or interesting
> techniques.](https://google.github.io/eng-practices/review/reviewer/looking-for.html#good-things)

> Nit: This is a minor thing. Technically you should do it, but it won’t hugely
> impact things.

> Consider: I think this may be a good idea, but it’s not strictly required.

> FYI: I don’t expect you to do this in this PR, but you may find this
> interesting to think about for the future.

Any comments without a severity label are assumed to be necessary to address.

## Responding to Reviews

When responding to review comments, the author should react or reply **but leave
the comment unresolved**. This gives the reviewer an opportunity to verify all
changes have been addressed before resolving the comment.

If you are only addressing minor changes, then it is better to add follow-up
commits _without rebasing_. This makes it easier for the review to follow what
has changed. If substantial changes are required, it is best to rebase your
entire PR or even create a new one.

In the rarer cases that one of your commits contains substantial issues and
should not belong in the commit history, it is recommended to _rebase onto the
common ancestor_ instead of master. Once again this makes it easier for the
reviewer to follow what has changed.

## Recommended Tools

### GitHub CLI

The GitHub CLI [`gh pr`](https://cli.github.com/manual/gh_pr) command allows you
to manage PRs from within the terminal. 

Especially useful commands are `gh pr create [--web]` and `gh pr status
[--conflict-status]`.

### VS Code Extension

The [Github Pull Requests
extension](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github)
allows you to view and create pull requests from within VS Code. Alongside
[`github.dev`](https://github.com/github/dev) this makes it easier to navigate
surrounding code during reviews.

### Browser Extension

The [Refined
GitHub](https://github.com/refined-github/refined-github#highlights-) browser
extension augments the GitHub interface with useful additions and features.

[Highlights](https://github.com/refined-github/refined-github#highlights-)
include visible whitespace, showing only unresolved comments in PRs and adding
`sort:updated-desc` to the default search. 
