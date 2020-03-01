# pwsh-diff

`pwsh-diff` aims to serve as a PowerShell-based alternative to
[diff-highlight](https://github.com/git/git/tree/master/contrib/diff-highlight)
(and, eventually,
[diff-so-fancy](https://github.com/so-fancy/diff-so-fancy)) on Windows, because Perl and Windows
[don't](https://github.com/so-fancy/diff-so-fancy/issues/361) seem to
[get along](https://github.com/microsoft/terminal/issues/4738) when it comes to ANSI coloring.

This project is still in early development.

## Acknowledgements

Much of the requisite logic has been adapted directly from the aforementioned
[diff-highlight](https://github.com/git/git/tree/master/contrib/diff-highlight)
and
[diff-so-fancy](https://github.com/so-fancy/diff-so-fancy).