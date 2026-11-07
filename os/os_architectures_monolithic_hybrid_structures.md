**Operating System Structures**

An Operating system can be built by different structures. There are mainly 8 types. 
- Simple structure
- Layered structure
- Modular structure
- Virtual Machines
- Monolithic structure
- Micro kernel structure
- Hybrid Kernel structure
- Exo kernel structure

**Simple Structure**
Simple structures have no seperation between the interface and the system internals. It acts a simple program.
Applications have direct access of system resources. User program crashes can bring down the entire OS. 
Ex MS DOS

**Layered Structure**
Layered structure divides the layer into multiple layers where each layer uses functions of the below layer. 
Debugging is easier since each bug is associated with its layer 
Causes overhead because data has to passed through multiple layers.

**Modular Structure**
In Modular structure, uses a kernel which has core functionalities and the rest of the services are added on boot or runtime as loadable modules. 
It similar to layered structure as it abstracts the core functionalities but makes communication with other modules a lot simpler
Ex Solaris

**Virtual Machines**
VM abstracts the hardware and network and cpu into isolated environments. Each vm acts like a independent machine despite running on same hardware
Ex Virtualbox

**Monolithic Structure**
In monololithic architecture the OS is a entire big kernel containing all the functionalities. Any change in the user based program need to alter the kernel code. Its faster since there is no overhead of system calls. 
Ex SunOS, BSD

**Micro Kernel Structure**
In Micro, the kernel contains only the essential services. Rest of the services run in user space. 
This allows new services to be added without modifying the kernel code.
Ex MINIX, Mach

**Hybrid Kernel structures**
Hybrid kernel uses the concepts of both monolithic and micro kernel. It blends the speed and control of monolithic kernel and moularity of micro kernels .
Ex Mac OS

**Exo kernel structure**
Exo kernel structure gives direct access to applcations to modify system level resources. It seperates resource protection with resource management.
Offers great freedom to users.
Ex Aegis, ExOS

