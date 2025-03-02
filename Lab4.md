# Managing Permissions and Directories in Linux

## Objective
The objective of this lab is to learn how to manage directories, set permissions using both symbolic and octal methods, and configure the `umask` for a user. You will create a directory, modify its permissions, and ensure proper access control for groups and users.



## Commands and Concepts Used

### 1. Create the `/home/consultants` Directory
To create the `/home/consultants` directory, use the `mkdir` command:
```bash
sudo mkdir /home/consultants
```


![image](https://github.com/user-attachments/assets/f6f498e4-4113-4a94-9d9f-f949e96da456)




### 2. Add Write Permission to the `consultants` Group
To add write permission to the `consultants` group, use the `chmod` command with the symbolic method:
```bash
sudo chmod g+w /home/consultants
```

#### Explanation:
- `g+w`: Adds write (`w`) permission for the group (`g`).

![image](https://github.com/user-attachments/assets/54d241d5-2b96-4cbf-8f4f-9706c9a2fef4)




### 3. Forbid Others from Accessing the Directory
To forbid others from accessing the `/home/consultants` directory, use the `chmod` command with the octal method:
```bash
sudo chmod 770 /home/consultants
```

#### Explanation:
- `770`: 
  - `7` (owner): Read, write, and execute permissions.
  - `7` (group): Read, write, and execute permissions.
  - `0` (others): No permissions.

![image](https://github.com/user-attachments/assets/93699379-5dcc-48f7-846d-902f35e1f85b)





### 4. Verify Permissions
To verify the permissions of the `/home/consultants` directory, use the `ls -ld` command:
```bash
ls -ld /home/consultants
```

#### Expected Output:
```
drwxrwx--- 2 root root 4096 Feb 4 10:36 /home/consultants
```

![image](https://github.com/user-attachments/assets/2ef85558-6ee6-43fe-aafb-817f915ab3f1)



### 5. Change the Default `umask` for the `operator1` User

## To ensure that files created by operator1 are not accessible by others:
The `umask` determines the default permissions for newly created files and directories. To change the `umask` for the `operator1` user, follow these steps:

1. Open the user's shell profile file:
   
    ```bash
    sudo nano /home/operator1/.bashrc
    ```
  

  ![image](https://github.com/user-attachments/assets/aa9ebf90-d511-41e7-8c9e-3d1f68d7a15e)


2. Add the following line at the end:
   
   ```bash
   umask 007
   ```

![image](https://github.com/user-attachments/assets/28fac600-49e9-41dd-ba17-a1da9bac48b2)

- `007` → Owner & group have full access `(rwx)`, others have no access `(---)`.

3. Apply the changes:
   ```bash
   source /home/operator1/.bashrc
   ```

4. Verify the new `umask`:
   ```bash
   umask
   ```
  ![image](https://github.com/user-attachments/assets/49737d03-a403-4a0b-8729-7772a93ffde7)



#### Explanation:
- `umask 007`: 
  - `0` (owner): Full permissions (default).
  - `0` (group): Full permissions (default).
  - `7` (others): No permissions.


## Conclusion
In this lab, you learned how to:
1. Create directories and manage their permissions using both symbolic and octal methods.
2. Restrict access to specific groups and users.
3. Configure the `umask` for a user to control default file and directory permissions.

