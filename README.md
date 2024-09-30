# Assignment-3 : Linux_and_Sql

## Linux

### Task - 1 [File Permissions]
To create a new empty file named `example.txt`, and change gile permissions, use these commands : 
```bash
touch example.txt
chmod 600 example.txt

# This command sets the permissions to 600, where:
# 6 (owner): Read and Write
# 0 (group): No permissions
# 0 (others): No permissions
# rwx --> r:4 w:2 x:1 

ls -l example.txt
# output  :-rw------- 1 owner owner 0 Sep 30 10:00 example.txt
```
![task-1](https://github.com/user-attachments/assets/b0afe6de-c9a0-47bd-b478-64b5b2707c0e)

---

### Task - 2 [Process Management]

To view all the currently running processes in real-time, use the `top` command:
```bash
top
# Shows a dynamic list of processes, including their Process ID (PID), user, CPU, memory usage.

pidof firefox
# 5783
#This command returns the PID(s) associated with the firefox process.

kill 5783
# kills the firefox (closes it)

kill 5783
# kill: (5783) - No such process
```
![task-2 1](https://github.com/user-attachments/assets/375566f7-5d1c-423d-be8f-98b84fec2870)
![task-2 2](https://github.com/user-attachments/assets/7dfa99cd-8786-4590-9c6b-9a72100282a6)

---

### Task - 3 [Monitor and Kill Process]

* The script continuously runs using a while true loop and checks every 10 seconds for processes whose name starts with Kill_Me using the ps aux | grep command.
* The awk command extracts the process ID (PID) and process name.
* If a process is found, its termination details (name, PID, and time) are logged in killed_processes.log.
* The process is forcefully terminated using the kill -9 command.
* Each time a process is killed, the event is logged in the format: Date: Process Name with PID was terminated in killed_processes.log.
* The script checks for new processes every 10 seconds using the sleep 10 command, ensuring it pauses between checks to avoid continuous execution.

![task-3](https://github.com/user-attachments/assets/dd96f07d-8e52-40bc-b57e-1a827d62937c)

---

### Task - 4 [Shell Script to Perform tasks]
![Screenshot from 2024-09-30 20-20-14](https://github.com/user-attachments/assets/45bd0495-7bd8-427b-8e9a-f297395f9e6f)

---
---

## SQL

### Task - 1 [Filtering and Sorting]
- `CREATE DATABASE`: Used to create a new database for storing tables and data.
- `CREATE TABLE`: Creates a new table with specified columns and data types.
- `INSERT INTO`: Adds new records into a table.

- `CURDATE()`: Retrieves the current date.
  - `INTERVAL 30 DAY`: Used with `CURDATE()` to filter data from the last 30 days.

![1](https://github.com/user-attachments/assets/0f918d5f-d11f-40cb-a069-68fe072d7b33)

---

### Task - 2 [Join with multiple Tables]

---

### Task - 3 [Set Operations]

---

### Task - 4 [Combining Linux and SQL]
![4](https://github.com/user-attachments/assets/bc8c9b01-6144-41db-a7bd-1ed5fdfc3671)


---
