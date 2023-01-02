# GH-FZF

Collection of powerful aliases to speed up interactions with GitHub. It's purpose is to be a CLI clone of [github.com/pulls](https://github.com/pulls) and [github.com/issues](https://github.com/issues).

## Prerequisites?
* [fzf](https://github.com/junegunn/fzf)
* [hub](https://github.com/cli/cli)
* [jq](https://stedolan.github.io/jq/)

## Installation

You can directly download the [`ghfzf.source`](https://rawgit.com/cbrgm/ghfzf/master/ghfzf.source)
and save it in some directory.

Download:
```bash
curl -LO https://rawgit.com/cbrgm/ghfzf/master/ghfzf.source
```

then add to your .bashrc/.zshrc file:
```bash
[ -f <path-to>/ghfzf.source ] && source <path-to>/ghfzf.source
```

Alternatively you can install `ghfzf` using the ZSH plugin manager of your
choice.

## Usage

Usage of `ghfzf` aliases

```
Usage:

# [ghpr] search for open pull requests created by user, usage: ghpr [AUTHOR] - if AUTHOR is empty, @me is used
# [ghpra] search for open pull requests assigned to user, usage: ghpra [ASSIGNEE] - if ASSIGNEE is empty, @me is used
# [ghprm] search for open pull requests with user mentions, usage: ghprm [USER] - if USER is empty, @me is used
# [ghi] search for open issues created by user, usage: ghi [AUTHOR] - if AUTHOR is empty, @me is used
# [ghia] search for open issues assigned to user, usage: ghia [ASSIGNEE] - if ASSIGNEE is empty, @me is used
# [ghim] search for open issues with user mentions, usage: ghim [USER] - if USER is empty, @me is used
# [ghrr] search for pull requests waiting for a review requested by user, usage: ghrr [AUTHOR] - if AUTHOR is empty, @me is used
# [ghspr] search for pull requests waiting for a review across all repositories owned by an owner, usage: ghspr [OWNER] - if OWNER is empty, @me is used
# [ghsi] search for open issues created across all repos owned by an owner, usage: ghsi [OWNER] - if OWNER is empty, @me is used
# [ghhelp] show this help message
```
