# Topic: Researching Commands
For this week's lab report, I'll be looking at 4 different ways of using the `find` command.

## find /path/to/directory -name "pattern"
```
find written_2/ -name "ch*.txt" > names.txt
cat names.txt
```
![image](https://raw.githubusercontent.com/cheahfulnic/lab5/main/wk5-ss/week5-1.png)
```
find written_2/ -name "Intro*" > names.txt
cat names.txt
```
![image](https://raw.githubusercontent.com/cheahfulnic/lab5/main/wk5-ss/week5-2.png)
* The -name parameter allows users to search for files in the directory /path/to/directory whose names match the pattern "pattern". The output redirection sign, >, and cat is used to display the files.


## find /path/to/directory -type [f|d]
```
find written_2/non_fiction/OUP/ -type -f > types.txt
cat types.txt
```
![image](https://raw.githubusercontent.com/cheahfulnic/lab5/main/wk5-ss/week5-3.png)
* The -type f parameter allows users to search for files in the directory /path/to/directory. The output redirection sign, >, and cat is used to display the files.
```
find written_2/ -type d > types.txt
cat types.txt
```
![image](https://raw.githubusercontent.com/cheahfulnic/lab5/main/wk5-ss/week5-4.png)
* The -type d parameter allows users to search for directories in the directory /path/to/directory. The output redirection sign, >, and cat is used to display the files.


## find /path/to/directory -size [num][c|k|M|G]
```
find written_2/ -size 2k > names.txt
cat names.txt
```
![image](https://raw.githubusercontent.com/cheahfulnic/lab5/main/wk5-ss/week5-5.png)
```
find written_2/ -size -2k > sizes.txt
cat sizes.txt
```
![image](https://raw.githubusercontent.com/cheahfulnic/lab5/main/wk5-ss/week5-6.png)
* The -size parameter allows users to search for files in the directory /path/to/directory whose size is equal to [num] bytes, kilobytes (k), megabytes (M), or gigabytes (G). + or - can be used before the num to indicate more than or less than. The output redirection sign, >, and cat is used to display the files.


## find /path/to/directory -exec command {} \;
```
find written_2/ -size -2k > sizes.txt
cat sizes.txt
```
![image](https://raw.githubusercontent.com/cheahfulnic/lab5/main/wk5-ss/week5-7.png)
```
find written_2/ -name "ch*.txt" > names.txt
cat names.txt
```
![image](https://raw.githubusercontent.com/cheahfulnic/lab5/main/wk5-ss/week5-8.png)
* The -exec parameter, in conjunction with the -type parameter allows users to search for files (first case) or directories (second case) in the directory /path/to/directory, and perform the command on each of them. This is similar to the xargs parameter. The echo command is used to display the files/directories.
