# Scheduling in Plan 9

- As with most modern operating systems, Plan 9's scheduler is preemptive, giving it the ability to take control of the processor away from processes at will
- The scheduler itself makes use of a global run queue, containing every process that is currently available to be dispatched.
  - This queue is shared between all processors.
- The scheduler uses a round-robin algorithm to determine which process to dispatch
  - There are a few tricks in the implementation that causes the scheduler to prefer rescheduling processes on the same CPU.
- It's worth noting that in Plan 9, the scheduler dispatches processes, not threads.  What the process does with the CPU time is up to the process.
  - While threads exist, they are cooperatively scheduled subroutines under the control of the process.  The rfork system call, which is used to create new processes, can be used to create a new process which shares all resources with its parent, much like a kernel thread in other systems.
