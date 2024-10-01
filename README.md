# Assignment-3 : Linux_and_Sql

## Linux

### Task - 1 [File Permissions]
Created a file named `example.txt`, and changed its permissions using `chmod` command. 
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

- to view all the currently running processes in real-time, we use the `top` command.
- to get the process id of firefox, used `pidof` command,
- then killed the process using `kill` command,
- and to verify whether the process is killed or not, we can run the `kill` command with same process id
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
### SQL Exercise: Join with Multiple Tables

- `JOIN`: Combines rows from two or more tables based on a related column.
  - `INNER JOIN`: Retrieves records that have matching values in both tables.

- `ON`: Specifies the condition for the join.
  - Used to join the `customers` and `orders` tables on the `customer_id`.

- `JOIN with multiple tables`: Combines rows from `customers`, `orders`, and `products` tables.
  - The `products` table is joined with the previous result set to display the products ordered by each customer.

- `GROUP BY`: Groups the result set by one or more columns.
  - Groups by `customer_name` to aggregate the total order amount.

- `HAVING`: Filters groups of rows based on a specified condition.
  - Used to filter out customers or orders based on certain conditions after grouping (if required).

![2](https://github.com/user-attachments/assets/ec307fcf-28e3-42b2-a2d7-07168be4dc64)

---

### Task - 3 [Set Operations]
### SQL Exercise: Set Operations

- `UNION`: Combines the result set of two or more `SELECT` statements, returning unique records.
  - Used to get a list of unique employees from both the `employees_2023` and `employees_2024` tables.

- `INTERSECT`: Returns the common rows from both `SELECT` statements.
  - Used to find employees who worked in both 2023 and 2024.

- `EXCEPT`: Returns rows from the first `SELECT` statement that are not in the second `SELECT` statement.

![3](https://github.com/user-attachments/assets/e1d69378-3755-4931-89d5-7da0429f8a71)

---

### Task - 4 [Combining Linux and SQL]

![4](https://github.com/user-attachments/assets/bc8c9b01-6144-41db-a7bd-1ed5fdfc3671)


---
