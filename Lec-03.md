# Operating Systems Lecture 2: OS Introduction (Part 2): CPU, I/O and Interrupts


### I/O Devices
- It has 2 things:
    - **controller**
    - **local buffer**
- **driver** is the software (between OS and device controller) and **controller** is the hardware(electronic circult and interface)
- Data is witten to local buffer by device itself 
- Data transfer form local buffer to main memory is done by CPU


### Timing Diagram
```
CPU
                         running   copy
                                   data
                                   to MM
------------------------------------------------
| kernel | P1 | kernel | P2       | kenel   
------------------------------------------------

I/O
                    waiting
------------------------------------------------
                 | P1             |
------------------------------------------------
```
- I/O devices has a queue and service one at a time whenever it completes them its gonna generate an interrupt
- kenel invokes the CPU schedular 
- Process reqests I/O trough a **system call** (most common service of system call for I/O)
- **system call** is implemented using a **interrupt**
- Whenever an interrupts is generated control is given to kernel. Read about Interrupt Service Routine.
- When a process competes it I/O request (**waiting** state) it uses an **interrupt** to inform OS that it is done
- The kernal takes over after this **interrupt** and copies the the data from local buffer to main memory and marks the process as **ready**


### Special Interrupt exc
- It is called Exceptions
- Examples:
    - Divide by zero
    - Stack overflow
    - Floating Point overflow
    - Out of Bound memory access
- It transfers control to the kernel
- kernel terminates the process


### Computer-System Operation
- I/O devices and the CPU can execute concurrently
- Each device controller is in charge of a particular device type
- Each device controller has a local buffer
- CPU moves data from/to main memeory to/from local buffer
- I/O is form the device to local buffer of controller
- Device controller informs CPI that is has finished its operations by causing an **interrupt**


### Common Functions of Interrupts
- Interrupts transfers control to the interrupt service routine generally, through the **interrupt vector**, which contains the address of all the service routines
- Interrupts architecture must save the address of the interrupted instruction
- A **trap** or **exception** is a software-generated interrupt caused either by an error ot a user request
- An OS is **interrupt driven**
