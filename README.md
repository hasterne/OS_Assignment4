# OS Assignment 4 
## Table of Variants
The following table outlines the multiple code variants included in this repository. We may not use all of them, and if there are any combinations missing that would be good to test please let me know so I can create that variant! :relaxed: <br>
2Threads = Original Assignment 4 File
| Variation   | inc() | dec() | thread count |
| ------------- | ------------- | ------------- | ------------- |
| [2Threads](/2Threads.c) | sleep(.1)  | sleep(.2) | 2 | 
| [2ThreadsLoops](/2ThreadsLoops.c)| loop to 100,000  |loop to 200,000 | 2 |
| [2Threads2and2Sleep](/2Threads2and2Sleep.c)| sleep(.2) | sleep(.2) | 2 |
| [2Threads1and3Sleep](/2Threads1and3Sleep.c) | sleep(.1) | sleep(.3) | 2 |
| [2Threads1and5Sleep](/2Threads1and5Sleep.c) | sleep(.1) | sleep(.5) | 2 |
| [3Threads](/3Threads.c) | sleep(.1) | sleep(.2) | 3 |
| [3ThreadsLoops](/3ThreadsLoops.c) | loop to 100,000 | loop to 200,000 | 3 |
| [3Threads2and2Sleep](/3Threads2and2Sleep.c) | sleep(.2) | sleep(.2) | 3 |
| [3Threads1and3Sleep](/3Threads1and3Sleep.c)| sleep(.1) | sleep(.3) | 3 |
| [3Threads1and5Sleep](/3Threads1and5Sleep.c)| sleep(.1) | sleep(.5) | 3 |
| [4Threads](/4Threads.c)| sleep(.1) | sleep(.2) | 4 |
| [4ThreadsLoops](/4ThreadsLoops.c) | loop to 100,000 | loop to 200,000 | 4 |
| [4Threads2and2Sleep](/4Threads2and2Sleep.c) | sleep(.2) | sleep(.2) | 4 |
| [4Threads1and3Sleep](/4Threads1and3Sleep.c)| sleep(.1) | sleep(.3) | 4 |
| [4Threads1and5Sleep](/4Threads1and5Sleep.c)| sleep(.1) | sleep(.5) | 4 |
| [5Threads](/5Threads.c)| sleep(.1) | sleep(.2) | 5 |
| [5ThreadsLoops](/5ThreadsLoops.c)| loop to 100,000 | loop to 200,000 | 5 |
| [5Threads2and2Sleep](/5Threads2and2Sleep.c)| sleep(.2) | sleep(.2) | 5 |
| [5Threads1and3Sleep](/5Threads1and3Sleep.c)| sleep(.1) | sleep(.3) | 5 |
| [5Threads1and5Sleep](/5Threads1and5Sleep.c)| sleep(.1) | sleep(.5) | 5 |

## Helpful Commands
`awk -f mutexruns.awk &` Executes the awk file, which tests the mutex code up to the designated # of trials: [Default mutexruns.awk from Canvas]

`grep 1 out.mutex`

`grep -n 1 out.mutex`

`wc out.mutex` The leftmost number gives the number of lines in the output file, AKA the number of trials that have been completed.

`mv out.mutex destination_file`
## Running Instructions

#1 

## Concurrent Running Tips
