# Synchronization

- In Plan 9, new processes can only be created by forking with the fork and rfork system calls.
  - In reality, fork is just a shortcut to calling rfork with some default flags.
  - The flags passed to rfork determine which data (if any) is shared between the parent and child processes.

- Another important system call with regards to inter-process synchronization is rendezvous()
  - Basically, rendezvous() allows two processes to synchronize with eachother, and exchange a single value.

- To do this, the two processes each call rendezvous seperately, passing in a common tag (usually a shared address in memory) and the value to pass to the other process when the call is complete.

- The first process to reach the rendezvous call suspends execution until the other process reaches its own.  Then, botth processes are awakened, and their respective calls to rendezvous return the value the other process passed in.

- The rendezvous system call is deceptively simple, and can be used to implement more complicated synchronization routines.
