# gh-fused

Collection of powerful aliases combining `gh` and `fzf` to speed up interactions with GitHub. It's purpose is to be a CLI clone of [github.com/pulls](https://github.com/pulls) and [github.com/issues](https://github.com/issues) and it can be so much more!.

Try them out and you won't live without them anymore 🚀

## Prerequisites?

* [fzf](https://github.com/junegunn/fzf)
* [gh](https://github.com/cli/cli)
* [gnu core utils](https://www.gnu.org/software/coreutils/)
* [jq](https://stedolan.github.io/jq/)

## Installation

You can directly download the [`ghfused.source`](https://raw.githubusercontent.com/cbrgm/gh-fused/main/ghfused.source)
and save it in some directory.

Download:
```bash
curl -LO https://raw.githubusercontent.com/cbrgm/gh-fused/main/ghfused.source
```

then add to your .bashrc/.zshrc file:
```bash
[ -f <path-to>/ghfused.source ] && source <path-to>/ghfused.source
```

Alternatively you can install `ghfused` using the ZSH plugin manager of your
choice.

## Usage

Usage of `ghfused` aliases (you can check them by running `ghhelp` once installed)

```
Usage of ghfused aliases

Collection of powerful aliases to speed up interactions with GitHub
Find more information at https://github.com/cbrgm/ghfused

Usage:
# [ghspr] Fuzzy searches for pull requests and allows the user to open them in a web browser.
# [ghpr] Search for open pull requests created by the current user.
# [ghpra] Search for open pull requests assigned to the current user.
# [ghprm] Search for open pull requests with mentions of the current user.
# [ghrr] Search for open pull requests with review requests wanted from the current user.
# [gshi] Fuzzy searches for issues and allows the user to open them in a browser
# [ghi] Search for open issues created by the current user.
# [ghia] Search for open issues assigned to the current user.
# [ghim] Search for open issues with mentions of the current user.
# [ghsr] Fuzzy searches for repositories and allows the user to open them in a browser
# [ghhelp] show this help message
```

## Explanations

### Github Search enchanced!

The three aliases

* `ghspr` ([gh]ithub [s]earch [p]ull [r]equest)
* `ghsi` ([gh]ithub [s]earch [i]ssue)
* `ghsr` ([gh]ithub [s]earch [r]epository)

are equal to the default search subcommands provided by the `gh` command, but combines them with fuzzy searching with `fzf`.

### Fine-tuned defaults for PRs!

* `ghpr` Search for open pull requests created by the current user.
* `ghpra` Search for open pull requests assigned to the current user.
* `ghprm` Search for open pull requests with mentions of the current user.
* `ghrr` Search for open pull requests with review requests wanted from the current user.

### Fine-tuned defaults for issues!

* `ghi` Search for open issues created by the current user.
* `ghia` Search for open issues assigned to the current user.
* `ghim` Search for open issues with mentions of the current user.

## Some handy examples

Fuzzy search open PRs which requested a review from you, approve.

```bash
 ghspr --sort=updated --limit 100 --review-requested=@me --archived=false --state=open | xargs -I{} sh -c 'gh pr review --approve {}'
```

Fuzzy search open PRs which requested a review from you, approve and merge.

```bash
 ghspr --sort=updated --limit 100 --review-requested=@me --archived=false --state=open | xargs -I{} sh -c 'gh pr review --approve {} && gh pr merge --squash {}'
```

## Flags

Supports all options that `gh search repos/issues/prs` supports, except for `--json` and `--template` which are being utilized by this extension.

## Contributing & License

Feel free to submit changes! See
the [Contributing Guide](https://github.com/cbrgm/contributing/blob/master/CONTRIBUTING.md). This project is open-source
and is developed under the terms of the [Apache 2.0 License](https://github.com/cbrgm/gh-fused/blob/master/LICENSE).
