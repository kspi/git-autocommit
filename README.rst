git-autocommit
==============

Automatically commits each change in a git repository.


Usage
-----

::

    usage: git-autocommit [-h] [-w WATCH_BRANCH] {watch,merge} ...

    positional arguments:
      {watch,merge}         subcommands
        watch               watch repository for changes and commit them [default]
        merge               merge automatic commits back into normal branch

    optional arguments:
      -h, --help            show this help message and exit
      -w WATCH_BRANCH, --watch-branch WATCH_BRANCH
                            automatically commit to this branch [default:
                            autocommit]


Copy ``git-autocommit`` to some directory in your ``$PATH`` and run ``git
autocommit`` in the root of the git repository. It also automatically adds
files to the repository, so you should list everything you don't want
added in ``.gitignore``.

The commits are performed into a branch called ``autocommit``. They can be
merged back into master with ``git autocommit merge``.

Requirements
------------

It requires Python 3 and ``pyinotify``.
