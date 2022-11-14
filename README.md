#Branch utilization for lab 2
Lab 2 Q1 and P2 are included in this repository and branch. 
Lab 2 Q2 and Q3 are included as branches in a separate repository https://github.com/StephenJogie/Lab2_Q2_816022581 
The reason for branches only being utilized from the second question was because I was familiarizing myself with how to navigate between branches after Q1 was completed and the repository for Q2 was already made and being utilized, so it was decided that I would utilize branches going forward in the Q2 repository. 
The branches for the Q2 repository will be explained in the readme in the repository for Q2.

#P2
First, to allow freertos to collect statistics. 
  1. make menuconfig
  2. In menuconfig, -> component config -> FreeRTOS
  3. Select the option to enable FreeRTOS to collect run time stats

# Lab2_Q1_816022581
Included output files are:
  1. output.txt. This is an output for when the task delay of task3 is set to 100ms. This was done for debugging purposes to see task3 try to take the mutex while it was unavailable. 
  2. outputNormal1secTask3.txt. This is the correct output file for normal operation of the system for Q1 of lab 2. This is what is renamed to output.out. 
  

# Q1 brief description (with task3 having a 1000ms delay):
Task1 is created first, then Task2 is created, then Task3 is created. 
When task1 and task2 take the mutex and use the gpio pin (shared resource), they have an active delay of 500ms WHILE HOLDING THE MUTEX, they then give back the mutex for another task to use, then they have a TASK DELAY of 1000ms. 

See the below screenshot of the oscilloscope verifying correct operation of the system. 
![lab2q1ScopePicForGithub](https://user-images.githubusercontent.com/91706020/201450949-7711ae90-96ae-40ff-afae-be2fc2757359.png)
