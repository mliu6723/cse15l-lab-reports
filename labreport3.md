# Lab Report 3

In this lab report I will be researching the `find` command

# Option 1: `find -name`

Source: [find manual](https://man7.org/linux/man-pages/man1/find.1.html)

**Example 1**
```
find written_2 -name "Poland-History.txt"
written_2/travel_guides/berlitz2/Poland-History.txt
```
This command is looking in the directory `written_2` and finding the file named "Poland-History.txt." This command is helpful because it allows us to search for a file based on its name in a large directory. 

**Example 2**
```
find written_2/non-fiction/OUP/Abernathy -name "*.txt"
written_2/non-fiction/OUP/Abernathy/ch2.txt
written_2/non-fiction/OUP/Abernathy/ch3.txt
written_2/non-fiction/OUP/Abernathy/ch1.txt
written_2/non-fiction/OUP/Abernathy/ch7.txt
written_2/non-fiction/OUP/Abernathy/ch6.txt
written_2/non-fiction/OUP/Abernathy/ch8.txt
written_2/non-fiction/OUP/Abernathy/ch9.txt
written_2/non-fiction/OUP/Abernathy/ch15.txt
written_2/non-fiction/OUP/Abernathy/ch14.txt
```
This command is looking in the directory `written_2/non-fiction/OUP/Abernathy` for all files that have a name ending with .txt. This command is helpful because it allows us to search for files of a specific type, in this case ".txt"

# Option 2: `find -size`

Source: [find manual](https://man7.org/linux/man-pages/man1/find.1.html)

**Example 1**
```
find written_2/non-fiction/OUP/Abernathy -size -10M
written_2/non-fiction/OUP/Abernathy
written_2/non-fiction/OUP/Abernathy/ch2.txt
written_2/non-fiction/OUP/Abernathy/ch3.txt
written_2/non-fiction/OUP/Abernathy/ch1.txt
written_2/non-fiction/OUP/Abernathy/ch7.txt
written_2/non-fiction/OUP/Abernathy/ch6.txt
written_2/non-fiction/OUP/Abernathy/ch8.txt
written_2/non-fiction/OUP/Abernathy/ch9.txt
written_2/non-fiction/OUP/Abernathy/ch15.txt
written_2/non-fiction/OUP/Abernathy/ch14.txt
```
This command is looking in the directory `written_2/non-fiction/OUP/Abernathy` for all files that are less than 10 megabytes. This command is helpful because it allows us to search for files of a specific size requirement. 

**Example 2**
```
find written_2/non-fiction/OUP/Abernathy -size +1k
written_2/non-fiction/OUP/Abernathy/ch2.txt
written_2/non-fiction/OUP/Abernathy/ch3.txt
written_2/non-fiction/OUP/Abernathy/ch1.txt
written_2/non-fiction/OUP/Abernathy/ch7.txt
written_2/non-fiction/OUP/Abernathy/ch6.txt
written_2/non-fiction/OUP/Abernathy/ch8.txt
written_2/non-fiction/OUP/Abernathy/ch9.txt
written_2/non-fiction/OUP/Abernathy/ch15.txt
written_2/non-fiction/OUP/Abernathy/ch14.txt
```
This command is looking in the directory `written_2/non-fiction/OUP/Abernathy` for all files that are greater than 1 kilobyte. This command is helpful because it allows us to search for files that are bigger than a certain size.

# Option 3: `find -type`

Source: [find manual](https://man7.org/linux/man-pages/man1/find.1.html)

**Example 1**
```
find written_2/non-fiction/OUP/Abernathy -type f  
written_2/non-fiction/OUP/Abernathy/ch2.txt
written_2/non-fiction/OUP/Abernathy/ch3.txt
written_2/non-fiction/OUP/Abernathy/ch1.txt
written_2/non-fiction/OUP/Abernathy/ch7.txt
written_2/non-fiction/OUP/Abernathy/ch6.txt
written_2/non-fiction/OUP/Abernathy/ch8.txt
written_2/non-fiction/OUP/Abernathy/ch9.txt
written_2/non-fiction/OUP/Abernathy/ch15.txt
written_2/non-fiction/OUP/Abernathy/ch14.txt
```
This command is looking in the directory `written_2/non-fiction/OUP/Abernathy` for all files that are a regular file type. This command is helpful because it allows us to search for files of a specific type, in this case, regular files. 

**Example 2**
```
find written_2/non-fiction/OUP -type d          
written_2/non-fiction/OUP
written_2/non-fiction/OUP/Berk
written_2/non-fiction/OUP/Abernathy
written_2/non-fiction/OUP/Rybczynski
written_2/non-fiction/OUP/Kauffman
written_2/non-fiction/OUP/Fletcher
written_2/non-fiction/OUP/Castro
```
This command is looking in the directory `written_2/non-fiction/OUP` for all directories. This command is helpful because it allows us to search for files of a specific type, in this case, directories. 

# Option 4: `find -cmin`

Source: [find manual](https://man7.org/linux/man-pages/man1/find.1.html)

**Example 1**
```
find written_2/non-fiction/OUP/Abernathy -cmin +5
written_2/non-fiction/OUP/Abernathy
written_2/non-fiction/OUP/Abernathy/ch2.txt
written_2/non-fiction/OUP/Abernathy/ch3.txt
written_2/non-fiction/OUP/Abernathy/ch1.txt
written_2/non-fiction/OUP/Abernathy/ch7.txt
written_2/non-fiction/OUP/Abernathy/ch6.txt
written_2/non-fiction/OUP/Abernathy/ch8.txt
written_2/non-fiction/OUP/Abernathy/ch9.txt
written_2/non-fiction/OUP/Abernathy/ch15.txt
written_2/non-fiction/OUP/Abernathy/ch14.txt
```
This command is looking in the directory `written_2/non-fiction/OUP/Abernathy` for files that have been last changed more than 5 minutes ago. This command is helpful because it allows us to search for files that have not been altered for more than a certain amount of time.

**Example 2**
```
find written_2/non-fiction/OUP/Abernathy -cmin -10000
written_2/non-fiction/OUP/Abernathy
written_2/non-fiction/OUP/Abernathy/ch2.txt
written_2/non-fiction/OUP/Abernathy/ch3.txt
written_2/non-fiction/OUP/Abernathy/ch1.txt
written_2/non-fiction/OUP/Abernathy/ch7.txt
written_2/non-fiction/OUP/Abernathy/ch6.txt
written_2/non-fiction/OUP/Abernathy/ch8.txt
written_2/non-fiction/OUP/Abernathy/ch9.txt
written_2/non-fiction/OUP/Abernathy/ch15.txt
written_2/non-fiction/OUP/Abernathy/ch14.txt
```
This command is looking in the directory `written_2/non-fiction/OUP/Abernathy` for files that have been last changed less than 10000 minutes ago. This command is helpful because it allows us to search for files that have been altered in under a certain amount of time. It could be used to find files that have had recent changes.
