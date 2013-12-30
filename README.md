## Useful scripts

This is a collection of scripts that I find useful but are not worthy of having
their own repository each.

### 256colors

Prints out the xterm 256 color chart.

### git-alias

Prints git aliases.  The name argument can be used to filter the results.

<pre>
$ git alias
co      checkout
diffc   diff --cached
diffw   diff --color-words
k       !sh -c 'gitk "$@" &' git-k
</pre>
<pre>
$ git alias k
k       !sh -c 'gitk "$@" &' git-k
</pre>

### git-recent-branches

Lists branches and their ages, sorted by last commit timestamp.

<pre>
$ git recent-branches
  feature                        3 weeks ago
  other-branch                   4 days ago
* <span style="color: #00cd00">master                         8 minutes ago</span>
</pre>

### git-reparent

This is a symlink to [git-reparent](https://github.com/MarkLodato/git-reparent),
assuming it is contained in the same parent directory.

### git-zmv / git-mmv

Uses zsh's [zmv](http://zshwiki.org/home/builtin/functions/zmv) module with
`git mv`.  For example, to rename all ".markdown" extensions to ".md", use one
of the following:

    $ git zmv '(*).markdown' '$1.md'
    $ git mmv '*.markdown' '*.md'

### pithos-control

A script to control Pithos.  This is easier to use than raw `dbus-send`, and it
also includes discrete play and pause commands, which are not available
directly via dbus.  Examples:

    $ pithos-control play
    $ pithos-control skip

I originally wrote this for use with LIRC, as described in
[my blog post](http://marklodato.github.io/2013/10/24/how-to-use-lirc.html).

### risk

Prints the number of armies needed to perform a march in the game of [Risk][].
For example, to compute the number of armies to safely attack three countries,
one occupied by two defenders and two occupied by one each:

    $ risk 2 1 1
    Total armies expected needed: 11.5781570709 + extra for safety

    Defender      Loss  Inc. Loss  (not counting 2 army to occupy)
    ========  ========  =========
           2  1.546578   1.030789
           1  0.515789   0.515789
           1  0.515789   0.515789

[Risk]: http://en.wikipedia.org/wiki/Risk_(game)

### COPYRIGHT

All files are copyright 2013 Mark Lodato <lodatom@gmail.com> and released under
the MIT license.  See LICENSE for terms.
