ECE382Lab8
==========
Austin Bolinger
Dr. York
ECE 382
05 Nov 14

Description: Lab 5 is IR signals. Taking lab 3's pong game and making it react to the buttons pressed on a remote control.
**InLab5**

**Firmware**

Project built around [test5.c](http://ecse.bd.psu.edu/cmpen352/lab/lab5/test5.c)

1. How long will it take the timer to roll over?
2. How long does each timer count last?
3. The while(1) loop in main reads in the ir pules in the for loop. Annotate the picture below to describe the which lines of the for loop the program is executed at which part of the pulse. You should show a total of 6 lines of code (lines 32-34 and lines 36-38).

**IR data packets**

1. List the lengths of the pulses generated by the remote control in absolute time using the O'scope (3 significant figures) and in timer A counts.

| Pulse | Duration (ms) | timer A counts |
| --- | --- | --- |
| Start logic 0 half-pulse | 1.11 |  8950 |
| Start logic 1 half-pulse | 0.553  | 4420 |
| Data 1 logic 0 half-pulse | 0.0770 | 616  |
| Data 1 logic 1 half-pulse | 0.206 | 1650  |
| Data 0 logic 0 half-pulse | 0.0770 | 616 |
| Data 0 logic 1 half-pulse | 0.0678 | 542 |
| Stop logic 0 half-pulse | 0.0771 | 620 |
| Stop logic 1 half-pulse | 5.369 | 42952 |

1. Collect 8 samples of timer A counts for each of the following pulse types. Compute the average and standard deviation of each pulse type. I would suggest just grabbing it from the CCS variables tab.

| Data | Logic half-pulse | Average Count | Avg. Time(ms) | St. Dev. Count | St. Dev. Time(ms) |
| --- | --- | --- | --- | --- | --- |
| 1 | 0 | 507.6 | 0.00635 | 25.3 | 0.00316 |
| 1 | 1 | 1621.9 | 0.203 | 28.99 | 0.00362 |
| 0 | 0 | 617 | 0.0771 | 3.13 | 0.000392 |
| 0 | 1 | 617 | 0.0771 | 3.13 | 0.000392 |

Tabulate this information in Excel, label the rows and columns of your table so that I will know what the information in each cell means.

1. For each pulse type list the range of timer A counts that would correctly classify 99.9999426697% of the pulses. This number has something to do with thestandard deviation(hint look at the table in this section).
2. Let the codes (in hex) for several remote control buttons.

| Button | code (not including start and stop bits) |
| --- | --- |
| 0 | 0	1	1	0	0	0	0	1	1	0	1	0	0	0	0	0	1	0	0	1	0	0	0	0	0	1	1	0	1	1	1	1	1
 |
| 1 | 0	1	1	0	0	0	0	1	1	0	1	0	0	0	0	0	0	0	0	0	0	0	0	0	1	1	1	1	1	1	1	1	1
 |
| 2 | 0	1	1	0	0	0	0	1	1	0	1	0	0	0	0	0	1	0	0	0	0	0	0	0	0	1	1	1	1	1	1	1	1
 |
| 3 | 0	1	1	0	0	0	0	1	1	0	1	0	0	0	0	0	0	1	0	0	0	0	0	0	1	0	1	1	1	1	1	1	1
 |
| Power | 0	1	1	0	0	0	0	1	1	0	1	0	0	0	0	0	1	1	1	1	0	0	0	0	0	0	0	0	1	1	1	1	1
 |
| VOL + | 0	1	1	0	0	0	0	1	1	0	1	0	0	0	0	0	0	0	1	1	0	0	0	0	1	1	0	0	1	1	1	1	1
 |
| VOL - | 0	1	1	0	0	0	0	1	1	0	1	0	0	0	0	0	1	0	1	1	0	0	0	0	0	1	0	0	1	1	1	1	1
 |
| CH + | 0	1	1	0	0	0	0	1	1	0	1	0	0	0	0	0	0	1	0	1	0	0	0	0	1	0	1	0	1	1	1	1	1
 |
| CH - | 0	1	1	0	0	0	0	1	1	0	1	0	0	0	0	0	1	1	0	1	0	0	0	0	0	0	1	0	1	1	1	1	1
  |
