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
`awk -f mutexruns.awk &` Executes the awk file, which tests the mutex code up to the designated # of trials: [Default mutexruns.awk from Canvas](/mutexruns.awk)

`grep 1 out.mutex` prints all occurrences of 1 in the data

`grep -n 1 out.mutex` prints all occurences of 1 including the line (trial) number

`wc out.mutex` The leftmost number gives the number of lines in the output file, AKA the number of trials that have been completed.

`mv out.mutex destination_file` moves the data from the output file to a specified location, e.g. to out.mutex.sleep0.5.run1
## Running Instructions
*Use instructions below for running one file at a time*<br>
<br>
#1 copy the code from the variation you wish to test to your clipboard<br>
#2 create a a vim file called mutex.c and post the code into this file<br>
#3 compile mutex.c<br>
#4 create another vim file called mutexruns.awk<br>
#5 paste the awk code (with the appropriate number of trials) into mutexruns.awk<br>
<br>
#6 check with `ls` to make sure that a.out, mutex.c, and mutexruns.awk are present<br>
#7 run `awk -f mutexruns.awk &` to run the program in the background<br>
#8 check on how the program is doing:<br>check for synchronization mechanism failures using `grep 1 out.mutex` or `grep -n 1 out.mutex`<br>use `wc out.mutex` and check leftmost number to see how many trials have completed<br>
#9 move the data from out.mutex to a new file using the mv command in the format `mv out.mutex destination_file` e.g. `mv out.mutex out.mutex.sleep0.5.run1`<br>
#10 post new code in mutex.c, compile, and repeat steps 6-9.<br>

## Concurrent Running Tips
*These are the altered steps I took when running multiple different variations in order to avoid any possible errors with files overwriting other files. Some of this may be superfluous and maybe I didn't need to make new files for everything but I did so out of fear and lack of sufficient knowledge of C.* <br>
<br>
#2 I created a new vim file for each variation and called it something other than mutex.c<br>
#3 I used the command `gcc -o output_filename source_file.c` to create a different output (a.out replacement) for my new c file, giving the output_filename any name I want<br>
#4 I created this file with a different name and altered the code so that line 2 would read `system("cc current_variation_file.c -lpthread")` and line 3 would read `for (i=1; i<=100000000; i++) system("./output_file_from_step_3 >> out.file_name_for_destination_of_data")` I also would reduce 100 million to a smaller figure, maybe around 10 million.<br>
<br>
#6 check again with `ls` to ensure that we have <br>
<br>
1) the c file variant we are currently using <br>
2) the output file we named in step #3 <br>
3) The [awk file](/mutexruns.awk) that mentions 3 named variables, in order: the file names from #2, #3, and a unique `out.filename` where the data will be sent.<br>
<br>
#7 run the command using the new awk file<br>
#8 check the program making sure to use the `out.filename` that was created earlier<br>
#9-10 I did not complete these steps as I never reused mutex.c, mutexruns.awk, or out.mutex. (again, maybe that was very unnecessary 😅)<br>
<br>
**I also used `htop` to figure out which awk process running belonged to which variation, and obtain their PIDs in order to kill them (because I was running for 100 million trials)**
