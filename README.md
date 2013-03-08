# go-errcheck

go-errcheck provides an easy way to invoke
[errcheck](https://github.com/kisielk/errcheck) from within Emacs.

It invokes errcheck with the current file's directory and optionally
options for ignoring certain functions or packages. The output gets
presented in a compilation buffer, allowing navigating errors.

## Basic usage

Basic usage is as simple as invoking the function `go-errcheck` in a
Go buffer. Calling `go-errcheck` with a prefix argument allows setting
the `ignorepkg` and `ignore` flags interactively.

## Customizations

go-errcheck offers two customizable options: `go-errcheck-ignorepkg`
and `go-errcheck-ignore`, which correspondent to errcheck's flags. You
can set their default values directly or via the customization menu.

You can also use
[file local variables](http://www.gnu.org/software/emacs/manual/html_node/emacs/File-Variables.html)
as well as
[per-directory local variables](http://www.gnu.org/software/emacs/manual/html_node/emacs/Directory-Variables.html).
Because errcheck always operates on whole directories/packages, using
per-directory variables might make more sense than using file local
variables. They allow setting the `ignorepkg` and `ignore` flags for
your packages so that errcheck will be invoked with them
automatically.

## Screenshot

![Screenshot of go-errcheck](http://stuff.fork-bomb.org/screenshots/go-errcheck.png "go-errcheck displaying the filtered output of errchecking the fmt package")
