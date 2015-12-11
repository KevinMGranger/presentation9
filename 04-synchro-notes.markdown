# Synchronization

- In Plan 9, new processes can only be created by forking with the fork and rfork system calls.
  - In reality, fork is just a shortcut to calling rfork with some default flags.
  - The flags passed to rfork determine which data (if any) is shared between the parent and child processes.

- Another important system call with regards to inter-process synchronization is rendezvous()
  - Basically, rendezvous() allows two processes to synchronize with eachother, and exchange a single value.

- To do this, the two processes each call rendezvous seperately, passing in a common tag (usually a shared address in memory) and the value to pass to the other process when the call is complete.

- The first process to reach the rendezvous call suspends execution until the other process reaches its own.  Then, botth processes are awakened, and their respective calls to rendezvous return the value the other process passed in.

- The rendezvous system call is deceptively simple, and can be used to implement more complicated synchronization routines.

- Another method for interprocess communication is a through mechanism called Channels.  
  - Channels are essentialy queues where processes can put fixed-size messages.  
    - These can be buffered and unbuffered.
  - Processes and threads use the send and recv syscalls to communicate using the Channels
    - When using an unbuffered channel, send()ing a message to it causes it to lock until it recieves a recv system call.

- These channels are similar to the ones found in the Go programming language, which is coincidentally developed by some of the same people.
