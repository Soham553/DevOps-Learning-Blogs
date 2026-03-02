- ps: show Current terminal processes. 
- ps -a: Shows all terminal processes.
- ps -e: All processes
- ps aux: All processes with resource usage.
- ps ajx: 

- sleep: Use to pause a process according to the flags
    flags:
      - infinity: pause a process indefinitely.
      - 10s
      - 5m
      - 1h
      - 1d
    Note: sleep 30 &: (& indicates that run sleep in background).

- jobs: Check running background jobs

- kill job_number: Kill a job using job number or using PID.  

- top: a dynamic, real-time view of running system processes

- htop:  interactive system monitor and process manager 

- vmstat	Display a single summary report with averages since boot.