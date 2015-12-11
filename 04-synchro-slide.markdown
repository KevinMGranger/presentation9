# Synchronization

- New processes created with fork() and rfork()

- Third system call for inter-process synchronization
  - rendezvous()
  - Allows two processes to synchronize and exchange a value

- Two processes call rendezvous() with a common tag, and a value
  - Tag is typically a shared memory address
  - First process to access the rendezvous call sleeps until other process reaches it
  - Finally, values are swapped and returned, and both processes are awakened

- Can be used to implement more complicated routines
  - sleep/wakeup
  - queueing locks
  - reader/writer locks

- Channels
  - A queue for fixed-size messages
    - Can be buffered or unbuffered
  - Processes and threads can send() and recv() messages
    - Unbuffered channels block on send, unblock on corresponding recv

