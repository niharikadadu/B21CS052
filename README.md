# XV Quiz (CSL 3030)

Welcome to the XV Quiz for CSL 3030 - Operating Systems!



## Instructions
- Answer the multiple-choice questions by selecting the correct option.
- For theoretical questions, provide concise and accurate explanations.
- Feel free to use this quiz for self-assessment or educational purposes.

## Multiple-Choice Questions

#### Question 1: Basics
1. What is XV6?
   - a. A programming language
   - b. A Unix-like operating system
   - c. A file system
   - d. An assembly language

#### Question 2: Architecture
2. XV6 is based on which earlier operating system?
   - a. Windows
   - b. Linux
   - c. BSD
   - d. DOS

#### Question 3: File System
3. Which file system is used in XV6?
   - a. FAT32
   - b. NTFS
   - c. ext4
   - d. simple

#### Question 4: System Calls
4. How are system calls implemented in XV6?
   - a. As functions in the C standard library
   - b. As interrupts
   - c. Through the command line
   - d. As external programs

#### Question 5: Processes
5. In XV6, what is the maximum number of processes that can run simultaneously?
   - a. 128
   - b. 256
   - c. 512
   - d. 1024

#### Question 6: Shell
6. What is the name of the shell used in XV6?
   - a. Bash
   - b. Zsh
   - c. Sh
   - d. Fish

#### Question 7: Scheduling
7. How does XV6 handle process scheduling?
   - a. Round-robin scheduling
   - b. Priority-based scheduling
   - c. First-Come-First-Serve (FCFS)
   - d. Random scheduling

#### Question 8: Memory Management
8. Which memory management technique is used in XV6?
   - a. Paging
   - b. Segmentation
   - c. Virtual Memory
   - d. None of the above

#### Question 9: Interrupts
9. How are interrupts handled in XV6?
   - a. Through polling
   - b. Using hardware interrupts
   - c. Using software interrupts
   - d. Both b and c

#### Question 10: Multithreading
10. Does XV6 support multithreading?
    - a. Yes
    - b. No

#### Bonus Question:
11. Who developed XV6?
    - a. Microsoft
    - b. Google
    - c. MIT
    - d. IBM

## Theoretical Questions

#### Question 12: Process States
12. Briefly explain the different states a process can be in within the XV6 operating system.

#### Question 13: File System Structure
13. Describe the structure of the file system in XV6. Include the key components and their roles.

#### Question 14: System Calls vs. Library Functions
14. Explain the difference between system calls and library functions in the context of XV6. Provide examples of each.

#### Question 15: Memory Paging
15. How does memory paging work in XV6? Discuss the benefits of using paging in memory management.

#### Question 16: Shell Commands
16. Name and briefly explain three essential shell commands in the XV6 operating system.

#### Question 17: Process Synchronization
17. Discuss the concept of process synchronization in XV6. Why is it essential, and what mechanisms are used to achieve it?

#### Question 18: Interrupt Handling
18. Explain the role of interrupts in the XV6 operating system. How are interrupts handled, and what is their significance in system operation?

#### Question 19: Virtual Memory
19. What is virtual memory, and how is it implemented in XV6? Discuss the advantages of using virtual memory.

#### Question 20: Boot Process
20. Outline the steps involved in the boot process of XV6. What happens from the moment the computer is powered on to when the XV6 kernel is loaded into memory?

## Answers
Please write your answers here

1.  b
2.  c
3.  d
4.  b
5.  a
6.  c
7.  a
8.  a
9.  d
10.  b   
11.  c

12. -->UNUSED: The process is not in use and is available for allocation. 
    -->EMBRYO: The process is in the process of being created but has not yet been fully initialized.
    -->SLEEPING: The process is waiting for some event to occur, such as the completion of I/O or the expiration of a timer. 
    -->RUNNABLE: The process is ready to run but is not currently executing. 
    -->RUNNING: The process is currently being executed on the CPU.
    -->ZOMBIE: The process has completed its execution, but its parent has not yet collected its exit status.

13. 6 layers in File sytsem
    --> Systems calls
    --> Pathnames
    --> directories
    --> files
    --> transactions
    --> blocks

    At the lowest layer are data blocks. Blocks are the basic unit of storage on a disk.
    Transactions provide a way to group multiple operations into a single atomic operation.
    The file layer manages the organization and storage of user data. Each file has a specific structure and is associated with metadata (attributes like permissions, timestamps, etc.).
    Directories organize files hierarchically. They contain entries that map names to inodes (file identifiers).
    Pathnames are strings that represent the location of a file within the file system hierarchy.
    The system calls layer serves as the interface between user-level applications and the kernel. 

 
14. It makes a system call to the os when it wants to do something, like open a file. The library functions are more complex functions that make our lives easier. Most of the time, they come after system calls. Open() is a system call, while fopen() is a library method. 

15. Virtual memory is split into pages of a certain size, and real memory is split into frames that are the same size. It's smart to use memory for paging, keeps tasks separate, and lets you do things like demand paging.

16. ls: Lists the files in the current directory.
    cp: Copies files or directories.
    rm: Removes (deletes) files or directories.

17. Synchronization of processes is used to keep many processes going smoothly and trouble-free. In XV6, locks and semaphores are used to keep shared resources from being used by too many people at once and to stop races. 

18. Interrupts are events that make the CPU temporarily hand over control to a different piece of code. ISRs, or interrupt service routines, handle events in XV6.

19. Virtual memory is an illusion of a bigger memory. Virtual memory makes a "idealized abstraction" of your computer's storage resources when you use it to control your memory. XV6 makes virtual memory with swapping. It is easy to write programs and good use of memory when processes are kept separate.

20. The BIOS or UEFI software sets up the hardware, loads the bootloader (like GRUB), and then loads the XV6 kernel into memory. The kernel then takes over, sets up the data structures it needs, and starts the process of setup. It goes to the user area and starts the shell in the end.
     
