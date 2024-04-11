# OS Assignment 4 
## Table of Variants
The following table outlines the multiple code variants included in this repository. We may not use all of them, and if there are any combinations missing that would be good to test please let me know so I can create that variant! :relaxed: <br>
2Threads = Original Assignment 4 File
| Variation   | inc() | dec() | thread count |
| ------------- | ------------- | ------------- | ------------- |
| 2Threads | sleep(.1)  | sleep(.2) | 2 | 
| 2ThreadsLoops | loop to 100,000  |loop to 200,000 | 2 |
| 2Threads2and2Sleep | sleep(.2) | sleep(.2) | 2 |
| 2Threads1and3Sleep | sleep(.1) | sleep(.3) | 2 |
| 2Threads1and5Sleep | sleep(.1) | sleep(.5) | 2 |
| 3Threads | sleep(.1) | sleep(.2) | 3 |
| 3ThreadsLoops | loop to 100,000 | loop to 200,000 | 3 |
| 3Threads2and2Sleep | sleep(.2) | sleep(.2) | 3 |
| 3Threads1and3Sleep| sleep(.1) | sleep(.3) | 3 |
| 3Threads1and5Sleep| sleep(.1) | sleep(.5) | 3 |
| 4Threads| sleep(.1) | sleep(.2) | 4 |
| 4ThreadsLoops | loop to 100,000 | loop to 200,000 | 4 |
| 4Threads2and2Sleep | sleep(.2) | sleep(.2) | 4 |
| 4Threads1and3Sleep| sleep(.1) | sleep(.3) | 4 |
| 4Threads1and5Sleep| sleep(.1) | sleep(.5) | 4 |
| 5Threads| sleep(.1) | sleep(.2) | 5 |
| 5ThreadsLoops| loop to 100,000 | loop to 200,000 | 5 |
| 5Threads2and2Sleep| sleep(.2) | sleep(.2) | 5 |
| 5Threads1and3Sleep| sleep(.1) | sleep(.3) | 5 |
| 5Threads1and5Sleep| sleep(.1) | sleep(.5) | 5 |

## Helpful Commands
`awk -f mutexruns.awk &` Executes the awk file, which tests the mutex code up to the designated # of trials: [Default mutexruns.awk from Canvas]

`grep 1 out.mutex`

`grep -n 1 out.mutex`

`wc out.mutex` The leftmost number gives the number of lines in the output file, AKA the number of trials that have been completed.

`mv out.mutex destination_file`
## Running Instructions

#1 

## Concurrent Running Tips
