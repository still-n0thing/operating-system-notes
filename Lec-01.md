# Operating Systems Lecture 1: OS Introduction (Part 1)


### What is an OS?
- A program that acts as an intermediary betweene a user of a computer and the computer hardware
- OS goals:
    - Execute use programs and make solving user problems easier
    - Make the computer system convenient to use
    - Use the computer hardware in an efficient manner (resource management)
    - It provides system calls and APIs


### What are 4 components of a computer system?
![4 components of a computer system](/images/01-01.png)


### What OS do?
- Depends on thr type of system
- Users want convenience, **ease of use** and **good performance**
    - Don't care about **resouce utilization**
- But shared computers such as **mainframes** must keep all users
- User of dedicated systems such as **workstationss** have dedicated resources but frequentlly use shared resources from **servers**
- Handheld computers are resources poor, optimized for usability and battery life
- Some computers have little or no user interface, such as embedded computers in devices and automobiles (computers that control different hardwares)


### Operating System definition
- OS is a **resouce allocator**
    - Manages all the resouces
    - Decides betweeen conflicting requests for efficient and fair resource use
- OS is a **control program**
    - Controls execution of programs to prevent errors and improper use of the computer (protection, ex- memory protection and DOS did not have it)
- No universally accepted defination
- "Everything a vendor ships when you order as OS" is a good approximation
    - But varies widely
- "The one program running at all times on the computer" is the **kernal** .
- Everthing else is either
    - a system program (ships with OS), or
    - an application program


### Computer Startup
- **bootstrap program** is loaded at power-up or reboot
    - Typically stored in ROM or EPROM, generally known as **firmware**
    - Initializes all aspects of system
    - Loads OS kernel and starts execution
