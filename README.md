# Shortest-Job-First-CPU-Scheduling-Algorithm
##Description:
This C++ code implements the Shortest Job First (SJF) scheduling algorithm. SJF is a non-preemptive scheduling algorithm that selects the process with the shortest burst time for execution next. This code calculates and prints the waiting time, turnaround time, and a Gantt chart for the given processes.

Code Breakdown:

1.Include Statements and Namespace:

#include <bits/stdc++.h>: This includes all standard library headers.
using namespace std; directive allows the use of standard library names without the std:: prefix.

2.Main Function:

The main function performs the SJF scheduling algorithm and outputs the relevant information.

3.Variable Initialization:

int p: Total number of processes.
int w, i, j, sum = 0, min, index: Various integer variables for loops and calculations.
float awt = 0, atat = 0: Average waiting time and average turnaround time.

4.Input Handling:

The user is prompted to enter the total number of processes.
Arrays are dynamically allocated for storing burst times (cbt), waiting times (wt), Gantt chart values (gc), turnaround times (tat), and a temporary array (tmp).

5.Burst Time Input:

The user is prompted to enter the CPU burst times for each process.
These burst times are stored in both cbt and tmp arrays for sorting and processing.

6.Sorting and Gantt Chart Generation:

The burst times are sorted in ascending order using sort(cbt, cbt + p).
The Gantt chart is generated by selecting the shortest job (burst time) from the remaining jobs in each iteration.
For each selected job, the start time (gc), waiting time (wt), and turnaround time (tat) are calculated.
The selected job is marked as processed by setting its burst time in tmp to -1.
The process index is stored in proc for later reference.

7.Output Gantt Chart:

The Gantt chart is printed with process IDs and start times.
The total turnaround time (atat) is calculated by summing up the start times and dividing by the number of processes.

8.Output Process Details:

The process details including process ID, burst time, waiting time, and turnaround time are printed.
The total waiting time (awt) is calculated by summing up the waiting times and dividing by the number of processes.

9.Final Output:

The average waiting time and average turnaround time are printed.

Example Execution:
User is prompted to enter the number of processes.
User enters the burst times for each process.
The program sorts the burst times and generates the Gantt chart based on the SJF algorithm.
The program outputs the Gantt chart, process details, average waiting time, and average turnaround time.

Output:

Enter The Total Number of Process: 3

Enter CBT of Process:
7
4
1

========================================================
		Shortest Job First Gantt. Chart
========================================================
P3  |  P2  |  P1  |  
--------------------------------------------------------
00    01    05    12    

--------------------------------------------------------
Process		CBT	Waiting Time	Turn Around Time
--------------------------------------------------------
P[3]		1	0		1
P[2]		4	1		5
P[1]		7	5		12


Total Waiting Time: 2
Total Turn Around Time: 4
