# GH-FZF

Collection of powerful aliases to speed up interactions with GitHub

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

Usage:
# [ghpr] search for open pull requests created by user, usage: ghpr [AUTHOR] - if AUTHOR is empty, @me is used
# [ghi] search for open issues created by user, usage: ghi [AUTHOR] - if AUTHOR is empty, @me is used
# [ghrr] search for pull requests waiting for a review requested by user, usage: ghrr [AUTHOR] - if AUTHOR is empty, @me is used
# [ghspr] search for pull requests waiting for a review across all repositories owned by an owner, usage: ghspr [OWNER] - if OWNER is empty, @me is used
# [ghsi] search for open issues created across all repos owned by an owner, usage: ghsi [OWNER] - if OWNER is empty, @me is used
# [ghhelp] show this help message
