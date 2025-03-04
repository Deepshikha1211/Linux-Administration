# File and Directory Management in Linux

## Objective
The objective of this lab is to practice creating files and directories using the Linux command line. We will learn how to use the `touch` command for creating files and the `mkdir` command for creating multiple directories simultaneously.

## Commands Used
### Creating Multiple Files
To create multiple files with specific names, we use the `touch` command along with **brace expansion**. The syntax is:
```bash
touch song{1..6}.mp3 snap{1..6}.jpg film{1..6}.avi
```
#### Explanation:
- `song{1..6}.mp3`: This expands to `song1.mp3 song2.mp3 song3.mp3 song4.mp3 song5.mp3 song6.mp3`
- `snap{1..6}.jpg`: This expands to `snap1.jpg snap2.jpg snap3.jpg snap4.jpg snap5.jpg snap6.jpg`
- `film{1..6}.avi`: This expands to `film1.avi film2.avi film3.avi film4.avi film5.avi film6.avi`
- The `touch` command ensures all these files are created in the current directory.

  ![image](https://github.com/user-attachments/assets/49f0c074-7ddc-43b4-95ac-1ed97f1c1b95)

### Creating Multiple Directories
To create multiple directories at once, we use the `mkdir` command:
```bash
mkdir friends family work
```
#### Explanation:
- `mkdir` is used to create directories.
- Listing multiple directory names separated by spaces creates them simultaneously.
- The three directories created are `friends`, `family`, and `work`.

  ![image](https://github.com/user-attachments/assets/08305aad-9139-4e17-8c06-c05392804a63)

## Verifying the Creation of Files and Directories
After running the above commands, use the `ls` command to list the created files and directories:
```bash
ls
```
Output:
```
friends  family  work  song1.mp3  song2.mp3  song3.mp3  song4.mp3  song5.mp3  song6.mp3  snap1.jpg  snap2.jpg  snap3.jpg  snap4.jpg  snap5.jpg  snap6.jpg  film1.avi  film2.avi  film3.avi  film4.avi  film5.avi  film6.avi
```

## Conclusion
In this lab, we successfully created multiple files using `touch` with brace expansion and multiple directories using `mkdir`.
