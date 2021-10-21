# Chapter 3, 4 & 5 by TEAM 7
## Principal Investigator: Dr. Joshua Adams
## Compilation by: Srikanth & Yezdani

### Chapter 3 – 
#### Process scheduling 
In multiprogramming operating systems, process scheduling is the key factor to operating with multiple CPU cores and maximizing CPU utilization. Process scheduling handles the removal of the current process from the CPU and assigns a new process on the CPU based on a strategy for time efficiency and maximum CPU utilization. A CPU can manage one process at a time and multiprocessing can only be done on multiple CPU core systems. Multiple processes cannot be run on a single CPU core, here the CPU handles one process after one, and each process must wait for the CPU in a queue. 
There are three process scheduling queues, job queue, ready queue, and device queue. The operating system handles all PCBs in these queues. All the processes in the system will be in the job queue. The new processes, which are in main memory and are ready to execute will wait in this queue. Finally, the device queue constitutes the processes that are blocked due to the unavailability of the input device.  
#### Producer-Consumer problem
The producer-Consumer problem is also known as a bounded-buffer problem. Under this, a single buffer is shared by multiple producers and consumers at the same time. In the chapter on processes, a producer process creates data that operates by the consumer process. For example, assembly code complied by a complier and consumed by the assembler. This chain of commands goes further from assemblers who produce object modules provided to the loaders. Therefore, it becomes difficult to run multiple programs on a single buffer. To solve this problem, shared memory has an accessible number of buffer items which will permit both the producer and the consumer to produce and consume the items simultaneously. It will avoid consumers to not to consume data that has not been produced. Moreover, there are two types of a buffer that function differently. 
1.	The unbounded buffer – Under this, there is no practical limit set for the buffer size. The producer continuously runs a process though the consumer may wait for some time.
2.	The bounded buffer – The bounded buffer is a routine buffer under which each buffer is stable by a routine scheduled time. The consumer may wait for a new item while the producer has to wait only when the buffer is full.

### Chapter 4 -
#### Multi-threading model
In this concept of multi-threading, each thread refers to the parts of the program, and execution of all these threads or parts of the program at the same time is called multi-threading. CPU utilization and efficiency will be maximum by using this technique, where each part of the program, thread, will perform a different task and makes it fast and economical. There are three different models available in this technique, they are one to one, one too many, and many too many. 
There is a good number of benefits in multi-thread programming usage. Users will get good responsiveness in this model, where even a thread is busy doing a long task, another thread will be responsive to the user. So, the user interface will be good. Sharing of resources between these threads will allow having the same address space for all the threads of any application. The creation of thread will take less time and fewer resources, it is economical. Multi-threading will be more advantageous in multiprocessor systems.
#### Thread Libraries
It is a thread library that provides programmers with an API for creating and managing threads. It is helpful in either user space or kernel. In user space, kernel support is null, so all codes and structures for the library exist in user space. The second approach is a kernel-level library supported by the operating system. Codes and Structures exist in kernel space, and the function invokes the API for the library resulting in a system call. 
Nowadays, only three threads are in use to run the program. They are POSIX thread, Windows, and Java. Pthreads are operated in either user space or kernel-level library, Windows on the only kernel-level library, and Java in Java programs. Let us take an example of a thread that is: sum = ∑ N i=1 i. Now, suppose N is 5, then the summation of numbers that is 15 will represent integers from 1 to 5. On the command line, the total provided by the user will run the three programs. To create and run multi-threads, two strategies perform their duty accordingly. These strategies are:
1.	Asynchronous threading - This type of threading helps design responsive user interfaces. After the thread is developed by its parent thread, the first and the second thread will start execution at the same time.
2.	Synchronous threading – In synchronous threading, after the multiple threads are created by the parent thread, the parent thread then waits for all the other sub-threads to execute before it starts again. Parent threads work simultaneously with its sub-threads, but they have to wait for its child threads to execute the program and finish it then only they work together.

### Chapter 5 –
#### Real-time CPU scheduling 
CPU scheduling in real-time is not an easy task, some unique problems will be generated during this. Hard real-time and soft real-time are the two types available in real-time scheduling. Soft real times are more flexible as they don’t have any timelines to finish or any urgency, even in case of missing any deadlines there is an option of rescheduling. 
Coming to the hard real-time scheduling, here time plays a major role and it's more complex when compared to soft real-time. Here there is a deadline for every process, and it should be scheduled at that time. There is no rescheduling option available here and a task done after the deadline is considered as a task not done. Mitigating the response time is the most crucial task of the scheduler. The performance of the real-time will be affected by the interrupt latency and dispatch latency, so minimizing the latency is also an important factor. 
#### Processor Affinity
Processor affinity is explained by considering cache memory running on a specific processor, and the data first accessed by the thread increases the cache for the processor. As a result, data is stored in a structure called warm cache. However, if the thread is transferring to another processor because of load balancing, then the cache must not be validated in the first processor and shifts to a new processor. In order to avoid this transferring of threads from one processor to another, most of the operating systems use SMP support that tries to avoid this migrating. The warm caches are very helpful to run the threads on the same processor. It is called processor affinity. Processor affinity has many types to perform their task accordingly. When the process is running on one processor, but it does not guarantee that it will remain running as same in an operating system, then this process is called soft affinity. Due to load balancing, threads maybe transfer to another processor. On the other hand, there are systems with system calls that help the process to run in allocated processors, which are called hard affinity. Let us take an example of Linux that provides soft affinity thus by the command; sched_setaffinity () on the system call will allow a thread to specify the set of CPUs to run. This command supports the hard affinity. We have discussed several benefits of processor affinity in this discussion, but the occurrence of load balancing may hinder the processor affinity advantages. Processor affinity keeps the thread running on the constant processor’s cache memory. However, load balancing shifts the process to another processor resulting in minimizing the benefits of processor affinity. This further may lead to extended memory access time.

### Questions 
1. What are the queues available in process scheduling and what’s their functions?
2. What are the advantages of multi-threading? 
3. Which is the real tike CPU schedule algorithm?
4. What are the solutions to producer consumer problem in threads? 
5. What are the types of process affinity? 
6. How multi-threading is helpful in thread libraries? Explain.





