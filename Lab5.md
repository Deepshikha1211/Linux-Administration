
# Process Management and Software Management in Linux

## Objective
The objective of this lab is to learn how to manage processes using commands like `ps`, `top`, and `kill`, and to understand how to install, update, and remove software using the `apt-get` command in Linux.


## Commands Used

### 1. Process Management Commands

#### a. **`ps` Command**
The `ps` command is used to display information about active processes.

##### Example 1: Display Processes for the Current User
```bash
ps
```


![image](https://github.com/user-attachments/assets/f3dc1587-63c7-4dd8-bd21-13c517edd13c)



##### Example 2: Display All Processes
```bash
ps -e
```


![image](https://github.com/user-attachments/assets/e4dbf873-9e8e-44d8-beec-69d23fa86d9c)


##### Example 3: Display Processes in Full Format
```bash
ps -ef
```


![image](https://github.com/user-attachments/assets/ce61de43-4c57-405a-9774-4415dcd37281)


---

#### b. **`top` Command**
The `top` command provides a real-time view of system processes.

##### Example: Run `top` to Monitor Processes
```bash
top
```


![image](https://github.com/user-attachments/assets/4cddbb5a-242d-4a5f-b96a-ca8e6a5f9bb5)


---

#### c. **`kill` Command**
The `kill` command is used to terminate processes.

##### Example 1: Terminate a Process by PID
First, find the PID of the process using `ps` or `top`, then terminate it:
```bash
kill <PID>
```


![image](https://github.com/user-attachments/assets/5a4be0d4-5006-43a7-a332-72bc45ad0324)


##### Example 2: Forcefully Terminate a Process
```bash
kill -9 <PID>
```


![image](https://github.com/user-attachments/assets/ac86d9f0-4084-4f30-bf77-de2982386166)


---

### 2. Software Management with `apt-get`

#### a. **Installing Software**
To install a software package, use the `apt-get install` command.

##### Example: Install `git`
```bash
sudo apt-get install git
```


![image](https://github.com/user-attachments/assets/7c20a20d-19c6-47f6-b84f-4873a1bbb86a)


---

#### b. **Updating Software**
To update the list of available packages and their versions, use:
```bash
sudo apt-get update
```


![image](https://github.com/user-attachments/assets/22cca233-949b-4b2a-8236-b87b08bdd4a2)


To upgrade installed packages to their latest versions, use:
```bash
sudo apt-get upgrade
```


![image](https://github.com/user-attachments/assets/46a01261-6257-4121-9e87-41e49b5d8ad9)


---

#### c. **Removing Software**
To remove a software package, use the `apt-get remove` command.

##### Example: Remove `git`
```bash
sudo apt-get remove git
```


![image](https://github.com/user-attachments/assets/de2ee6f4-d39d-4474-a239-bcb20b401a53)


To remove the package along with its configuration files, use:
```bash
sudo apt-get purge git
```


![image](https://github.com/user-attachments/assets/d355a0c2-d609-49cb-91c3-5db96c231051)


---

### 3. Verifying Software Installation and Removal
To verify if a package is installed, use the `dpkg` command:
```bash
dpkg -l | grep git
```


![image](https://github.com/user-attachments/assets/9d394eb3-9d6a-4372-b6b7-e1da22a0ac7a)


---

## Conclusion
In this lab, you learned how to:
1. Manage processes using `ps`, `top`, and `kill`.
2. Install, update, and remove software using `apt-get`.

