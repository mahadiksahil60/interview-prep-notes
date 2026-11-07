**Program**
A program is nothing but a blueprint on how the program should be executed. Programs are usually stored on the disk as passive files. 

**Process**
A process is a running instance of that program. A process is stored in RAM. A process provides isolation of resources, memory and other things. so a crash of one process does not bring the entire process down. 

**Threads**
Threads are independent execution paths inside a process they are responsible for carrying out different tasks inside a process. Each thread has its own stack, execution traceer and heap memory. A thread shares the memory space with other threads inside that process. Can achive concurrency thorugh threads. 


Ex Browser running. A process is created for running browser. now inside the process there are multiple tasks like handling user input, updating ui etc which is handled independently. 

