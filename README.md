# shelltest
Test cases for shell project

NOTE: EXCESS WHITESPACE IN COMMANDS HAS NOT YET BEEN WELL TESTED WITH
THE PATHLESS VERSION. CONVERSION WITH WITCH AND CUT MAY EAT THE WHITESPACE
OR BREAK THE COMMAND.

Usage: ./testpipe

This will create a folder for test results indicated by the RESULTSDIR path,
as well as subdirectories to store the individual output from all the test
files as they are run.

Configuration:
Edit config and set the path to your shell and the shell to compare against of
your choice. Optionally, disable or enable various sections to test depending
on how much you have completed. Notably, you will want to disable PATHENABLED
if you are not currently handling the PATH environmental variable.

Command file format:
Just a list of commands as if they were each a terminal input line. If you add
any, make sure it has at least a semi-descriptive filename for the case. If
it's not clear what the case is, add a comment to the top of the case's file.

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