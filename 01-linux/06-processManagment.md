# 06 – Process Management (Linux)

Process management is the ability to **monitor, control, and manage running programs** in a Linux system.

Every running program is called a **process** and is assigned a unique **PID (Process ID)**.

---

## What Is a Process?

- A process is an instance of a running program  
- Linux is multitasking → multiple processes run simultaneously  
- Each process has:
  - PID (Process ID)
  - User (owner)
  - CPU & Memory usage
  - State (Running, Sleeping, Stopped, Zombie)

---

## Viewing Processes

### Show processes for current terminal
```bash
ps
Show all running processes (detailed view)
ps aux

a → all users

u → detailed user format

x → include background processes

Real-Time Monitoring
Live process monitoring
top

Shows CPU & RAM usage

Updates in real time

Press q to exit

Enhanced interactive viewer (if installed)
htop

Easier navigation

Colorful interface

Allows direct process control

Searching for a Process
Find a process by name
ps aux | grep process_name
Get PID directly
pidof process_name
Process States

Common states:

R → Running

S → Sleeping

T → Stopped

Z → Zombie (terminated but not cleaned)

Zombie processes indicate improper cleanup.

Killing / Stopping Processes
Kill using PID
kill PID
Force kill (immediate termination)
kill -9 PID
Kill by name
pkill process_name

Use kill -9 only if normal kill fails.

Process Priority (Nice Value)

Priority range:

-20 → Highest priority

19 → Lowest priority

Default → 0

Start process with priority
nice -n 10 command
Change priority of running process
renice 5 -p PID
Background & Foreground Jobs
Run command in background
command &
View background jobs
jobs
Bring job to foreground
fg %1
Why Process Management Matters (Cybersecurity)

Detect suspicious or malicious processes

Identify resource abuse

Stop unauthorized programs

Analyze system behavior during incidents

Essential for system administration and security monitoring

Key Takeaway

Process management allows you to observe, control, and secure running programs in a Linux system.