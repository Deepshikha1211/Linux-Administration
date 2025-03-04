# Using man Pages, Searching Commands, and Brace Expansion in Linux

## Objective
The objective of this lab is to explore Linux manual (`man`) pages, search for commands related to `ext4`, and understand the usage of **brace expansion** for generating discretionary strings of characters.

## Commands Used

### Viewing the `gedit` man Page
1. To view the manual page for `gedit`, use the `man` command:
```bash
man gedit
```
#### Explanation:
- The `man` command displays the manual page for a specified command.
- `gedit` is a text editor for the GNOME desktop environment.

![image](https://github.com/user-attachments/assets/6ad49c14-8e1a-43bb-9bb6-fc3cea7a5659)

This will display details about the gedit text editor.

![image](https://github.com/user-attachments/assets/c19c4709-7035-4eeb-892a-f9195b8fa117)


2. Find the Command to Tune ext4 File-System Parameters
   
To find relevant commands for ext4, use:

```bash
man tune2fs
```


The result will show various ext4-related commands. The command used for tuning ext4 parameters is:

![image](https://github.com/user-attachments/assets/abed3356-70bf-4ff5-80dc-09ed660adabc)

This will open the manual page for tune2fs, which is used to adjust tunable parameters of ext2, ext3, and ext4 file systems.

![image](https://github.com/user-attachments/assets/f856e8d7-4ad4-4976-8722-64b930b636b8)


### Using Brace Expansion
Brace expansion generates arbitrary strings of characters. It can be used for creating lists or sequences efficiently.

#### Generating a List of Strings
```bash
echo file_{1,2,3}.txt
```
**Output:**
```
file_1.txt file_2.txt file_3.txt
```

![image](https://github.com/user-attachments/assets/cd72154c-1fea-40b3-ad29-0a4a6746df98)

### Using Sequence Expansion

```bash
echo song_{1..5}.mp3
```
**Output:**
```
song_1.mp3 song_2.mp3 song_3.mp3 song_4.mp3 song_5.mp3

```



![image](https://github.com/user-attachments/assets/9b19fee3-70f2-43e7-89d7-e6297ef43c78)







