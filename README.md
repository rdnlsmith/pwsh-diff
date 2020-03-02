# pwsh-diff

`pwsh-diff` aims to serve as a PowerShell-based alternative to
[diff-highlight](https://github.com/git/git/tree/master/contrib/diff-highlight)
(and, eventually,
[diff-so-fancy](https://github.com/so-fancy/diff-so-fancy)) on Windows, because Perl and Windows
[don't seem](https://github.com/so-fancy/diff-so-fancy/issues/361)
to
[get along](https://github.com/microsoft/terminal/issues/4738) when it comes to ANSI coloring.

This project is still in early development.

## Installation

Make sure you have PowerShell Core (`pwsh.exe`) in your `PATH` somewhere. Then, copy the `pwsh-diff`
script to a directory in your `PATH`. That's it!

## Usage

Configure Git to use `pwsh-git` for all diff/log output:

```ps
git config --global core.pager "pwsh-diff | less --tabs=4 -RFX"
```

### Improved colors

`pwsh-diff` will read the same color settings expected by `diff-highlight`, and it depends on Git
itself to colorize everything besides the lines with highlighted bits. The following options are
recommended:

```ps
git config --global color.ui true

git config --global color.diff-highlight.oldNormal    "red bold"
git config --global color.diff-highlight.oldHighlight "red bold 52"
git config --global color.diff-highlight.newNormal    "green bold"
git config --global color.diff-highlight.newHighlight "green bold 22"

git config --global color.diff.old "red bold"
git config --global color.diff.new "green bold"
```

## Acknowledgements

Much of the requisite logic has been adapted directly from the aforementioned
[diff-highlight](https://github.com/git/git/tree/master/contrib/diff-highlight)
and
[diff-so-fancy](https://github.com/so-fancy/diff-so-fancy).