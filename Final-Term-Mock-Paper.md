# OPS145 – Mock Final Exam

## 📚 Table of Contents

* [Overview](#-overview)
* [Instructions](#-instructions)
* [Topics Covered](#-topics-covered)
* [Mock Final Exam Questions](#-mock-final-exam-questions)

  * [Section A – Windows OS & Processes](#section-a--windows-os--processes)
  * [Section B – Linux OS & Processes](#section-b--linux-os--processes)
  * [Section C – Bash Scripting](#section-c--bash-scripting)
  * [Section D – Windows CMD Scripting](#section-d--windows-cmd-scripting)
  * [Section E – Regular Expressions](#section-e--regular-expressions-linux--windows)
* [How to Use This Mock Final](#how-to-use-this-mock-final)
* [Additional Resources](#additional-resources)



## 📝 Overview

This mock final exam is designed to help you practice all major topics covered in **OPS145** from Labs 6–10.
Difficulty and style closely match the real labs and lecture examples.



## 📌 Instructions

* Total recommended time: **1 hour 30 minutes**
* You may complete the exam during or after the SLG session
* Use **Matrix**, **Windows CMD**, and **PowerShell** as required
* Use the command line for all answers
* Show *commands* and *outputs* where applicable



## 🧠 Topics Covered

This mock exam includes questions from:

* Windows OS commands (systeminfo, tasklist, taskkill, PowerShell cmdlets)
* Linux OS monitoring (top, ps, kill)
* Bash scripting (loops, file testing, formatting)
* CMD scripting (variables, loops, conditions, backups)
* Regular expressions in Linux (`grep`) and Windows (`findstr`)



## 🧪 Mock Final Exam Questions

### **Section A – Windows OS & Processes**

1. Using the **systeminfo** command, determine:
   a) The exact CPU model
   b) Total installed physical memory
   c) Available physical memory

2. Start the *Camera* app.
   Use `tasklist` to find the Camera process and record:

   * Process ID
   * Memory usage
   * Program name

3. Terminate the process using **taskkill** by PID.
   If it doesn’t terminate, try again with the force option.

   * Why is `/F` sometimes required?

4. Restart Camera.

   * Why is the new PID different?

5. Switch to **PowerShell**.
   Using `get-process`, find Camera again and record:

   * PID
   * Working set
   * CPU time

6. Terminate the Camera app using `stop-process -name`.



### **Section B – Linux OS & Processes**

7. View `/proc/cpuinfo`.

   * How many processors/cores are available?

8. Run `top`. Record:

   * Total memory
   * Available memory
   * CPU idle percentage

9. Sort by CPU (`Shift+P`) and memory (`Shift+M`).

   * List the top 3 CPU-consuming processes
   * List the top 3 memory-consuming processes

10. Start this long-running process:

```
for ((x=0; x<20000; x++)) ; do sleep 0.01 ; done &
```

* Identify its PID using `ps`
* Terminate it using `kill`

11. Explain why **killall** may not be ideal for terminating a bash loop like this.



### **Section C – Bash Scripting**

12. Write a bash script `info.sh` that displays:

* Current user
* Current directory
* Whether the directory is $HOME
* Disk usage of home directory (`du -sh ~`)
* Current time (`date +%R`)
  All output must be **aligned neatly**.

13. Consider this script:

```
F=0
for NAME in *
do
  if [[ -f "$NAME" ]]
  then
    ((F++))
  fi
done
echo "Result: $F"
```

a) What does it output?
b) What does it count?
c) Does it include subdirectories?

14. Modify the script to count:

* Regular files
* Directories
* Symbolic links
* Total items
  Provide formatted output.



### **Section D – Windows CMD Scripting**

15. Explain what this script does:

```
set F=0
for %%N in (*) do (
    if exist %%N set /a F+=1
)
echo Result: %F%
```

a) What does it count?
b) Why are parentheses needed?

16. Create a CMD script `backup.cmd` that:

* Asks user for a directory name
* Checks if it exists
* Creates it if not
* Copies all files from current directory
* Displays each filename
* Shows total copied files



### **Section E – Regular Expressions (Linux + Windows)**

17. Using grep with a regex, find all lines in `/etc/services` that refer to **SSH** (case insensitive).

18. Using Windows `findstr /r`, find all processes using **less than 100,000 K** of memory from `tasklist`.

19. From `driverquery`, find all drivers with:

* ModuleName containing "SMB" (case-insensitive)
* DriverType = Kernel



## 🎯 How to Use This Mock Final

* Attempt each question on Matrix or Windows
* You can discuss strategies during the SLG session
* Complete the exam fully at home for best results
* Bring any questions to the next review session


