# shelltest
Test cases for shell project

Usage: testscript pathtoshell

Currently the plan is to have automated batch tests of all commands and many command combinations
to make sure they all work, then automatically compare it to what happens when BASH is run. 
Currently that functionality is commented out since I assume at this time most people have
debug code in which makes diff less useful. 

Eventually, once there are dozens to hundreds of cases, I think it would be nice to
break them into individually selectable sections (cases in separate files) organized
something like the list below.

1) single commands and builtins
2) commands/builtins with arguments and options
3) ;
4) #
5) " and ' not intermixed
6) 2, 3, 4 and 5 combined
