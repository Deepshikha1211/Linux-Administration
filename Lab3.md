<h2>Objective:</h2>

The objective of this lab is to familiarize yourself with two popular text editors in Linux: Vim and Nano. You will use these editors to modify the editing_final_lab.txt file, manipulate text using Vim's visual mode, and perform specific edits such as removing characters and preserving specific portions of text.

**Commands Used:**

**1. Setting Up the Lab File**
Before starting, ensure you have the editing_final_lab.txt file. If it doesn't exist, create it using the following command:

```sh
touch editing_final_lab.txt
```


   
To store the file path in a shell variable for easier access:
```sh
lab_file="editing_final_lab.txt
```

**Setting the shell variable**

![image](https://github.com/user-attachments/assets/0f2d48fb-a2d5-4ab9-8406-6566704ca50c)





**2. Editing with Nano**
Nano is a simple and user-friendly text editor. To open the file in Nano:

```sh
nano $lab_file
```
   

**Opening Nano**

![image](https://github.com/user-attachments/assets/3b2b093f-bc12-4727-846e-90f0deace27e)


**Tasks in Nano:**
Add the following text to the file:

```sh
This is the first line of this file.
This is the second line of this file.
This is the third line of this file.
```

Save the file by pressing `CTRL + O`, then exit Nano by pressing `CTRL + X`.


**Saving and exiting Nano**  

![image](https://github.com/user-attachments/assets/c85bed40-fba3-426d-881b-ed70f06e633f)


**3. Editing with Vim**
Vim is a powerful and highly configurable text editor. To open the file in Vim:

```sh
vim $lab_file
```
   

**Opening Vim:** 

![image](https://github.com/user-attachments/assets/b22aa363-cb8d-4f97-938a-2ef18c3f8c12)


Tasks in Vim:
Enter Visual Mode:

- Move the cursor to the first line.

- Press `v` to enter visual mode.


**Entering Visual Mode**

![image](https://github.com/user-attachments/assets/9f59c95f-1146-4e83-9f34-1625b7ed98ce)


**Remove the Last Seven Characters from the First Column:**

- In visual mode, highlight the last seven characters of the first line.

![image](https://github.com/user-attachments/assets/00320df5-81fb-478e-90ce-4b350278893e)

- Press `d` to delete the highlighted text.

![image](https://github.com/user-attachments/assets/f20d9c84-3ebf-4e1c-8be0-7f63e56103ba)





**Preserve Only the First Four Characters of the First Column:**

- Move the cursor to the beginning of the first line.

- Press 4l to move the cursor to the fourth character.

- Press v to enter visual mode, then highlight the remaining characters after the fourth character.

- Press d to delete the highlighted text.

**Save and Exit:**

- Press `ESC` to ensure you're in command mode.

- Type `:wq` and press Enter to save and exit Vim.

**Verifying Command Execution:**

- After completing the tasks, verify the contents of the file using:

```sh
cat $lab_file
```

- Verifying file contents

![image](https://github.com/user-attachments/assets/bb4a8288-1bca-48af-b6cf-73fc41fc507c)


**Expected Output:**

If the file initially contained:

```sh
This is the first line of this file.

This is the second line of this file.

This is the third line of this file.
```

After editing with Vim, the first line should be:

```sh
This
```

**Conclusion:**

In this lab, you learned how to use Nano and Vim to edit files in Linux. You practiced basic text manipulation in Vim, including entering visual mode, deleting specific characters, and preserving portions of text. These skills are essential for efficient file editing and scripting in Linux.








