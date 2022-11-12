# Lab2_Q1_816022581

Q1 brief description (with task3 having a 1000ms delay):
Task1 is created first, then Task2 is created, then Task3 is created. 
When task1 and task2 take the mutex and use the gpio pin (shared resource), they have an active delay of 500ms WHILE HOLDING THE MUTEX, they then give back the mutex for another task to use, then they have a TASK DELAY of 1000ms. 

See the below screenshot of the oscilloscope verifying correct operation of the system. 
![lab2q1ScopePicForGithub](https://user-images.githubusercontent.com/91706020/201450949-7711ae90-96ae-40ff-afae-be2fc2757359.png)
