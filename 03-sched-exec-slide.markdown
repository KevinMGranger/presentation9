# Scheduling in Plan 9

- Preemptive
- Global run queue
  - One run queue shared between all processors
  - One run queue lock
  - Sub-queues corresponding to priority
- Scheduler dispatches processes, not threads  
