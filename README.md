# shelltest
Test cases for shell project

NOTE: Excess whitespace at the start of a line in a command file will break
the PATHless version for the moment.

NOTE2: If you have a prompt output with piped input, the diff will see every
line with your prompt as different from the shell you're mimicing since
they do not output a prompt. Use isatty() to make your shell not output
the prompt for better results.

Usage: ./testpipe

This will create a folder for test results indicated by the RESULTSDIR path,
as well as subdirectories to store the individual output from all the test
files as they are run.

Configuration:
Edit config and set the path to your shell and the shell to compare against of
your choice. Optionally, disable or enable various sections to test depending
on how much you have completed or want to focus on. Notably, you will want
to disable PATHENABLED if you are not currently handling the PATH
environmental variable.

How to add cases to shell input checks:
Just make a file with the list of input lines you want and stick it in an
appropriate directory. There are three directories hooked up currently,
basiccmds, argcmds and comments. More will be forthcoming.

Command file format:
Just a list of commands as if they were each a terminal input line. If you add
any, make sure it has at least a semi-descriptive filename for the case. If the
description is too complicated for a filename, then any lines beginning with a
comment (#) should output before the diff is taken. Directories that are not
comment testing will filter out lines that begin with comments before they are
input to the shell.

Currently the plan is to have automated batch tests of all commands and
many command combinations to make sure they all work, then automatically
compare it to what happens when the selected shell is run. 

Sections will be organized something like the below:

1) single commands
2) commands with arguments and options
3) ;
4) \#
5) " and ' not intermixed
6) 2, 3, 4 and 5 combined
N) Extensive testing of builtins individually, one for each

Additionally, there will likely be tests for individual library style
functions added here as well at some point.
