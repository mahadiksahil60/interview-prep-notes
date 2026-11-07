**Kernel vs user mode**

- User mode is for running normal applications. It has limited access to system resources.
- Kernel mode runs the core os and has all the control over hardware.
- This seperation ensures security, stability and efficient resource management

**User Mode**
- When a program starts, the OS creates a seperate process and assigns its own memory space 
- Program in user mode cannot access hardware or kernel memory directly it has to request 
  access through system calls to kernel

**Key features**
- Isolated environment : Each process has its own memory space.
- No direct hardware access : Only accessible to kernel services.
- Safe Excecution : Errors or crashes dont affect entire system.

**Advantages :**
- Easier debugging : Since each process is isolated debugging is easier
- Crash control : One crash cannot affect other applications or os 
- Security : Since application cannot access other application memory and system hardware its secure 

**Disadvantage :**
Overheaad : Since all the communication happens through system calls to the kernel it introduces a significant overhead. 
Low control : Developers have low control over the hardware might result in lesser control over the memory.


**Kernel mode**
Kernel mode is a privileged mode where kernel operates, it has unlimited access to all machine resources, storage, cpu and gpu.
When it receives a request from user mode it executes the operations and then the control returns to user mode 

**Key features :**
Direct hardware access : Has access to all the hardware components 
Complete system control : has control over the entire hardware

**Advantages :**
- Full hardware access
- Low overhead
- Advance scheduling : multitasking, thread syncnorization, context switches 

**Disadvantages :**
- High risk of system crash : errors can affect entire os 
- Harder to debug : mistakes in kernel are harder to identify and fix.
- Security issues : Exposes a security risks

**Interview-ready answer:**

"User mode and kernel mode are CPU execution privilege levels. An application running in user mode invokes a system call,
 which triggers a controlled CPU privilege transition into kernel mode.
The kernel executes the requested operation and returns control to user mode."


**System Calls : Execution flow**
- When user program want to access any system resources, it invokes a system call.
- Then the mode switching happens and cpu changes the privililedges to kernel mode. Executes the command in 
  safe environment and returns the flow to user mode again. 
- *NOTE* : Mode switching is different from context switching where the calling program is blocked.

**Types of system calls**

![Types of system calls](https://media.geeksforgeeks.org/wp-content/uploads/20251202114956548681/frame_11.webp)

- File System : Used to create, open, close, save a file in the system. Ex. open(), close(), read(), write(), seek()
- Memory Management : Used to allocate, deallocate, terminate and block memory. brk(), sbrk(), mnap(), mlock()
- Process Control : Used to create, execute, terminate process. Ex fork(), exec(), wait(), exit(), kill()
- Interprocess Communication (IPC) : Used to transfer data between different processes. Ex socket(), semget().
- Device Management : Used to request and release devices Ex. open(), close(), WriteConsole(), ReadConsole()


