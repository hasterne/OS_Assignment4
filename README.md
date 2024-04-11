# OS Assignment 4 
## Table of Variants
The following table outlines the multiple code variants included in this repository. We may not use all of them, and if there are any combinations missing that would be good to test please let me know so I can create that variant! :relaxed: <br>
2Threads = Original Assignment 4 File
| Variation   | inc() | dec() | thread count |
| ------------- | ------------- | ------------- | ------------- |
| 2Threads | sleep(.1)  | sleep(.2) | 2 | 
| Loops2Threads | loop to 100,000  |loop to 200,000 | 2 |
| 2and2Sleep2Threads | sleep(.2) | sleep(.2) | 2 |
| 1and3Sleep2Threads | sleep(.1) | sleep(.3) | 2 |
| 1and5Sleep2Threads | sleep(.1) | sleep(.5) | 2 |
| 3Threads | sleep(.1) | sleep(.2) | 3 |
| Loops3Threads | loop to 100,000 | loop to 200,000 | 3 |
| 2and2Sleep3Threads | sleep(.2) | sleep(.2) | 3 |
| 1and3Sleep3Threads| sleep(.1) | sleep(.3) | 3 |
| 1and5Sleep3Threads| sleep(.1) | sleep(.5) | 3 |
| 4Threads| sleep(.1) | sleep(.2) | 4 |
| Loops4Threads | loop to 100,000 | loop to 200,000 | 4 |
| 2and2Sleep4Threads | sleep(.2) | sleep(.2) | 4 |
| 1and3Sleep4Threads| sleep(.1) | sleep(.3) | 4 |
| 1and5Sleep4Threads| sleep(.1) | sleep(.5) | 4 |
| 5Threads| sleep(.1) | sleep(.2) | 5 |
| Loops5Threads| loop to 100,000 | loop to 200,000 | 5 |
| 2and2Sleep5Threads| sleep(.2) | sleep(.2) | 5 |
| 1and3Sleep5Threads| sleep(.1) | sleep(.3) | 5 |
| 1and5Sleep5Threads| sleep(.1) | sleep(.5) | 5 |

## Helpful Commands
`awk -f mutexruns.awk &` Executes the awk file, which tests the mutex code up to the designated # of trials: [Default mutexruns.awk from Canvas]

`grep 1 out.mutex`

`grep -n 1 out.mutex`

`wc out.mutex` The leftmost number gives the number of lines in the output file, AKA the number of trials that have been completed.

`mv out.mutex destination_file`
## Running Instructions

#1 

## Concurrent Running Tips
