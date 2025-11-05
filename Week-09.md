# SLG Session – OPS102 (Processes & Command Tools)

**Date:** October 31, 2025 <br/>
**Duration:** 90 minutes <br/>
**Topic:** Process Management and System Monitoring on Windows & Linux <br/>



### **Agenda for Today**

1. **Welcome & Brain Dump (10 mins)**
   Quick recall of previous concepts and warm-up discussion.
2. **Activity 1 – Windows Task Management (20 mins)**
   Hands-on with `tasklist`, `taskkill`, and PowerShell equivalents.
3. **Icebreaker (10 mins)**
   Light and interactive discussion to re-energize the group.
4. **Activity 2 – Linux Process Monitoring (25 mins)**
   Exploring `/proc/cpuinfo`, `top`, and process control using `ps` and `kill`.
5. **Activity 3 – HTOP Deep Dive (20 mins)**
   Visual analysis of process data and interpreting metrics.
6. **Wrap-up & Reflection (5 mins)**
   Review of key learnings and open Q&A.


### **Brain Dump (10 mins)**

Without checking notes, list as many command-line tools as you can recall from the first half of the course - for both `Windows` and `Linux`. Then, share which one you’ve actually used outside the lab and why.

### **Activity 1 – Windows Task Management (20 mins)**

**Objective:** Understand and practice process monitoring and termination on Windows.

**Steps:**

1. Open CMD and run `systeminfo` or use the *System Information* app.
2. Record CPU and memory stats.
3. Use `tasklist | more` to view processes.
4. Identify the *Camera* process and record PID and memory usage.
5. Terminate it using `taskkill /PID <number>` and then by name.
6. Switch to PowerShell and repeat using `get-process` and `stop-process`.

**Discussion:**

* Why does the process ID change when restarted?
* What is the difference between CMD and PowerShell commands?

### **Icebreaker (10 mins): “Tech Talk Chain”**

**How it works:**
Each student names one command they like or find interesting and explains it in one line.
The next student must connect it to another command or tool that serves a similar purpose.

### **Activity 2 – Linux Process Monitoring (25 mins)**

**Objective:** Explore Linux system processes and resource monitoring tools.

**Steps:**

1. Use `cat /proc/cpuinfo` to check processor details.
2. Run `top` and record total and available memory.
3. Identify top 5 programs using most CPU and memory.
4. Run a background loop process using:

   ```bash
   for ((x=0; x<20000; x++)) ; do sleep 0.01 ; done &
   ```
5. Use `top` to locate and kill the process using `K`.
6. Repeat using `ps` and `kill` commands.

**Discussion:**

* What’s the difference between using `kill` and `killall`?
* How does Linux represent running processes differently from Windows?

### **Activity 3 – HTOP Deep Dive (20 mins)**

**Objective:** Interpret key system metrics and manage processes visually.

**Steps:**

1. Launch `htop` and explore its sections.
2. Identify and explain:

   * CPU bars
   * Memory and swap usage
   * Tasks, threads, uptime
   * PRI and NI values
3. Kill a process using `F9` and observe system response.

**Discussion Questions:**

* What is the default signal sent when killing a process?
* Why might adjusting priority (NI) be useful in performance tuning?
* Compare `htop`, `top`, and `btop` in usability.

### **Conclusion (5 mins)**

* Review the differences between Windows and Linux process management tools.
* Reinforce understanding of PID, memory usage, and CPU monitoring.
* Quick recap quiz:

  * One CMD command for viewing processes
  * One Linux command for killing a process
  * One metric shown in `htop`

**Takeaway:**
By the end of today’s session, you should feel confident navigating and controlling system processes across both operating systems using GUI and CLI tools.

