# Scheduling in Plan 9

- Preemptive

- Global run queue
  - One run queue shared between all processors
  - One run queue lock
  - Sub-queues corresponding to priority

- Algorithm: Round Robin
  - Prefers rescheduling on same CPU

- Scheduler dispatches processes, not threads  
