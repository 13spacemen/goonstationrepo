# goonstationrepo

goonstationrepo is the 2009 Space Station 13 code used on the Goon community's servers: a [BYOND](https://www.byond.com/)
game of life on a space station, written in DreamMaker. It was developed on Google Code
([code.google.com/archive/p/goonstationrepo](https://code.google.com/archive/p/goonstationrepo/)).

This repository holds the project's complete history, converted from its Google Code SVN repository
(89 revisions, March 9 to March 21, 2009).

## Building and running

1. Install BYOND, which includes Dream Maker (the compiler) and Dream Daemon (the server).
2. Open `Public.dme` in Dream Maker and compile it. The map is `maps/Space Station 13-new atmos.dmp`.
3. Host the compiled `Public.dmb` with Dream Daemon.

The server's settings are in `config/`, and `data/mode.txt` holds the default game mode.

This code was written for the BYOND of early 2009 and does not compile unchanged on current BYOND. BYOND 516 reports
6 errors: four `color` variables that now clash with a built-in variable, and procs named `sign` and `throw`, which
are now reserved words.

## Repository layout

`master` is the main line of development. New work goes here.

| Branch | Contents |
|---|---|
| `master` | SVN's `branches/Latest Revision`, continued. All of the project's development happened on this branch. |
| `svn-final-import` | `branches/Latest Revision` exactly as it was at the last SVN revision (r89). Kept unchanged as an archive. |
| `svn-trunk` | SVN's trunk (r1 to r7). The first upload of the code went here, was moved to `branches/Latest Revision`, and trunk was left empty. |
| `svn-mirror` | The whole SVN repository at every revision, including the project's wiki page |

Git branch names cannot contain spaces, so SVN's `Latest Revision` branch is not kept under its own name. Its
history is `master` up to r89.

### SVN details

Each converted commit ends with a `git-svn-id:` line giving its SVN path and revision. Further SVN information, such
as exact timestamps, changed paths and properties, is stored in git notes. After cloning, fetch and show them with:

```bash
git fetch origin refs/notes/svn:refs/notes/svn
```

```bash
git log --notes=svn
```

Commit authors are Google Code usernames. SVN stored no email addresses, so each author has the address
`username@e4a2f0c6-0cc0-11de-a490-4563d82dadc6`, the SVN repository's ID, as `git svn` does. Google Code created the
first revision itself, so it has no author.

## License

The Google Code project was published under the GNU General Public License, version 3. See `LICENSE`.
