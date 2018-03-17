# shelltest
Test cases for shell project

Usage: testpipe

Configuration:
Edit config and set the path to your shell and the shell to compare against of
your choice. Optionally, disable or enable various sections to test depending
on how much you have completed.

Currently the plan is to have automated batch tests of all commands and
many command combinations to make sure they all work, then automatically
compare it to what happens when BASH is run. 

Sections will be organized something like the below:

1) single commands and builtins
2) commands/builtins with arguments and options
3) ;
4) \#
5) " and ' not intermixed
6) 2, 3, 4 and 5 combined
