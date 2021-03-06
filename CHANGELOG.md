`0.0.19` Friday Nov 15, 2019

The `cd` method now has a default `dest`, as it should've all along. Use
`os.path.expanduser` to allow `~` at the start of the given path.

`0.0.18` Friday Nov 15, 2019

Fixed too-simplistic handling of control-c. Now install a signal handler
that sends a SIGINT to the pseudotty subprocess. A similar thing should be
done for subprocesses not run in pseudottys.

`0.0.17` Thursday Nov 14, 2019

Ignore control-c. Ignore non UTF-8 output from UNIX commands (e.g., the
output from running vi). The `UnicodeDecodeError` exception raised in this
case can still be seen when debugging is on (use the `%d` command to toggle
debug output and `%t` to see the traceback).

`0.0.16` Saturday Oct 19, 2019

Added non-interactive processing allowing scripts to be written for
`daudin` (with support for `#!/usr/bin/env daudin` hashbang lines). Add
reading from standard in via a regular shell pipe. Added some tests for
the new non-interactive processing.  Added `--noPtys` command-line option
to prevent pseudo-ttys from ever being used. Added to README.md.

`0.0.15` Saturday Oct 19, 2019

Added example function for setting a colored prompt showing the current
working directory and git branch. This is extremely simplistic!

`0.0.14` Saturday Oct 19, 2019

Added `--shell` command line option to control the underlying shell used
for UNIX commands.

`0.0.13` Thursday Oct 17, 2019

Added readline completion of Python symbols following
[suggestion from @reckoner](https://github.com/terrycojones/daudin/issues/7).
Documented this in `README.md`.

`0.0.12` Monday Oct 13, 2019

Improved `README.md`. Use `shlex.split` to extract argument in `%cd`
command, to allow quoting, spaces in dir names, etc.

`0.0.11` Sunday Oct 13, 2019

Improved `README.md`.

`0.0.10` Sunday Oct 13, 2019

Improved `README.md`.

`0.0.9` Sunday Oct 13, 2019

Improved `README.md`.

`0.0.8` Sunday Oct 13, 2019

Improved `README.md`.

`0.0.7` Sunday Oct 13, 2019

Improved `README.md`.

`0.0.6` Sunday Oct 13, 2019

Improved `README.md`.

`0.0.5` Sunday Oct 13, 2019

Improved `README.md`.

`0.0.4` Sunday Oct 13, 2019

Updated `README.md`.

`0.0.3` Sunday Oct 13, 2019

Added this `CHANGELOG`. Updated `README.md` with install instructions and a
bit more about reptile taxonomy.

`0.0.2` Sunday Oct 13, 2019 

Many changes, including filename completion, start-up options, README, a
new name, many bug fixes, traceback display, tests, code refactoring,
adjusted pipeline model, dropped support for Python 2, pseudo-tty support.

`0.0.1` Friday Oct 4, 2019 

Initial proof of concept.
