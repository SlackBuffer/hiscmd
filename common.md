# Table of contents
[`ps`](#ps)  
[`top`](#top)

---
# `ps`

```bash
ps aux | grep PID


#------------------------
# processes associated with the current terminal session
ps
# all processes owned by you (same EUID as ps)
ps x
## ? in the TTY column indicates no controlling terminal
## the new column STAT is short for state (see `man ps` or 10_processes.md for process state detail)
# processes belonging to every user
ps aux
```

# `top`

```bash
top # shift+m 按占用内存大小排序，shift+p 按消耗 CPU 大小排序


#------------------------
top
## 1 user:
## load average: 0.00, 0.01, 0.05: the number of processes that are in a runnable state and are sharing the CPU for the last 60 seconds, the next the previous 5 minutes, and finally the previous 15 minutes. Values less than 1.0 indicate that the machine is not busy.
## 0.0 us: percent of the CPU being used for un-niced (high-priority, <) user processes
## 0.0 sy: percent of the CPU being used for system (kernel) processes
## 0.0 ni: percent of the CPU being used by “nice” (low-priority, N) user processes
## 100.0 id: percent of the CPU that is idle
## 0.0 wa: percent of the CPU waiting for I/O
## 0.0 hi: time spent servicing hardware interrupts
## 0.0 si: time spent servicing software interrupts
## 0.0 st: time stolen from this vm by the hypervisor
## Mem: physical RAM
## Swap: swap space (virtual memory)
```