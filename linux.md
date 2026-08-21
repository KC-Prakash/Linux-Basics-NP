# Linux 491 Commands — Category-wise Nepali Quick Guide

> **Source:** संलग्न `linux.pdf` मा रहेका 491 Linux commands को सूची र category structure लाई आधार बनाइएको छ। PDF ले command को छोटो उद्देश्य/description दिन्छ; तलका **Example** र **Output** हरू सिकाइका लागि तयार गरिएका representative/illustrative examples हुन्, त्यसैले वास्तविक output Linux distribution, version, user, file, hardware र configuration अनुसार फरक हुन सक्छ।

## 📌 कसरी प्रयोग गर्ने
- `Command` = चलाउने command
- `Example` = practical syntax
- `Output` = सामान्य/illustrative परिणाम
- ⚠️ `sudo`, `rm`, `dd`, `mkfs`, partition, firewall, user-management जस्ता commands production system मा सावधानीपूर्वक चलाउनुहोस्।

## 📚 Categories
- [📁 Basic File and Directory Operations](#cat-1-52) — **52 commands**
- [📝 Text Processing and Editing](#cat-53-96) — **44 commands**
- [📊 System Monitoring and Management](#cat-97-145) — **49 commands**
- [👤 User and Permission Management](#cat-146-175) — **30 commands**
- [🌐 Networking and Communication](#cat-176-243) — **68 commands**
- [💽 Disk and File System Utilities](#cat-244-286) — **43 commands**
- [📦 Compression and Archiving](#cat-287-309) — **23 commands**
- [⚙️ Process Management](#cat-310-333) — **24 commands**
- [🛠️ System Configuration and Settings](#cat-334-491) — **158 commands**

---

<a id="cat-1-52"></a>
## 📁 Basic File and Directory Operations

**Commands 1–52 (52 commands)**

### 1. `ls`
**संक्षिप्त जानकारी:** the Linux ls command and its practical applications for managing files and directories. Learn how to utilize various options to retrieve detailed file information and navigate directory structures effectively.

**Example:**
```bash
ls -la
```

**Output (sample):**
```text
total ...
drwxr-xr-x ... .
-rw-r--r-- ... file.txt
```

### 2. `cd`
**संक्षिप्त जानकारी:** the Linux cd command, learn how to navigate the file system, and understand the difference between relative and absolute paths.

**Example:**
```bash
cd /var/log
```

**Output (sample):**
```text
No output; the working directory changes.
```

### 3. `pwd`
**संक्षिप्त जानकारी:** the Linux pwd command, its purpose, and practical examples of using it with other commands to manage files and directories.

**Example:**
```bash
pwd
```

**Output (sample):**
```text
/home/user
```

### 4. `mkdir`
**संक्षिप्त जानकारी:** the mkdir command in Linux, learn how to create directories, manage permissions, and work with nested directories through practical examples.

**Example:**
```bash
mkdir projects
```

**Output (sample):**
```text
No output; directory 'projects' is created.
```

### 5. `touch`
**संक्षिप्त जानकारी:** the versatile Linux touch command to create new files, modify file timestamps, and manage file operations efficiently. Gain practical experience through hands-on examples.

**Example:**
```bash
touch notes.txt
```

**Output (sample):**
```text
No output; 'notes.txt' is created if it does not exist.
```

### 6. `cp`
**संक्षिप्त जानकारी:** the versatile Linux cp command through practical examples. Learn how to copy files, directories, and preserve file attributes and timestamps effectively.

**Example:**
```bash
cp file.txt backup.txt
```

**Output (sample):**
```text
No output; 'backup.txt' is created.
```

### 7. `mv`
**संक्षिप्त जानकारी:** the Linux mv command and learn how to rename files, move multiple files, and perform other file management tasks with practical examples.

**Example:**
```bash
mv old.txt new.txt
```

**Output (sample):**
```text
No output; the file is renamed.
```

### 8. `rm`
**संक्षिप्त जानकारी:** the Linux rm command with practical examples. Learn how to remove files and directories, handle confirmation prompts, and force removal for efficient file management.

**Example:**
```bash
rm old.txt
```

**Output (sample):**
```text
No output when the file is removed successfully.
```

### 9. `ln`
**संक्षिप्त जानकारी:** the ln command in Linux, learn how to create hard and symbolic links, and understand their practical applications through hands-on examples.

**Example:**
```bash
ln -s /var/log/syslog syslog.link
```

**Output (sample):**
```text
No output; a symbolic link is created.
```

### 10. `cat`
**संक्षिप्त जानकारी:** the versatile Linux cat command through practical examples. Learn to concatenate and display text files, as well as append content to existing files, enhancing your basic file and directory operations skills.

**Example:**
```bash
cat hello.txt
```

**Output (sample):**
```text
Hello Linux
```

### 11. `less`
**संक्षिप्त जानकारी:** the less command, a powerful text viewer for Linux. Learn how to navigate through text files, search and highlight content, and utilize less effectively for your daily tasks.

**Example:**
```bash
less hello.txt
```

**Output (sample):**
```text
Interactive pager opens; press q to quit.
```

### 12. `more`
**संक्षिप्त जानकारी:** the versatile more command in Linux, learn how to navigate and search through text files, and customize its behavior for efficient file viewing.

**Example:**
```bash
more hello.txt
```

**Output (sample):**
```text
Hello Linux
```

### 13. `tree`
**संक्षिप्त जानकारी:** the Linux tree command, a powerful tool for visualizing directory structures. Learn its basic options, and apply it to specific directories and files for practical use cases.

**Example:**
```bash
tree demo
```

**Output (sample):**
```text
demo
└── hello.txt
```

### 14. `du`
**संक्षिप्त जानकारी:** the Linux du command to measure disk usage, understand its options, and learn how to exclude directories from the measurement process.

**Example:**
```bash
du -sh .
```

**Output (sample):**
```text
12M	.
```

### 15. `df`
**संक्षिप्त जानकारी:** the Linux df command, a powerful tool for monitoring disk usage. Learn how to customize the output and gain practical insights into your system's storage capacity.

**Example:**
```bash
df -h /
```

**Output (sample):**
```text
Filesystem  Size  Used  Avail  Use%  Mounted on
/dev/sda1   50G   18G   30G   38%   /
```

### 16. `stat`
**संक्षिप्त जानकारी:** the Linux stat command, learn how to retrieve file metadata, and analyze file permissions and ownership with practical examples.

**Example:**
```bash
stat hello.txt
```

**Output (sample):**
```text
File: hello.txt
Size: 12	Blocks: ...
Access: (0644/-rw-r--r--)
```

### 17. `find`
**संक्षिप्त जानकारी:** the power of the Linux find command with practical examples. Learn to search for files by name, file type, and combine find with other commands for advanced file system operations.

**Example:**
```bash
find . -name '*.txt'
```

**Output (sample):**
```text
./notes.txt
./docs/readme.txt
```

### 18. `locate`
**संक्षिप्त जानकारी:** the Linux locate command, a powerful tool for quickly searching and finding files on your system. Learn how to install the mlocate package and use locate to search for files and directories.

**Example:**
```bash
locate notes.txt
```

**Output (sample):**
```text
/home/user/notes.txt
```

### 19. `updatedb`
**संक्षिप्त जानकारी:** the updatedb command in Linux, which updates the locate database for efficient file searches. Learn how to use updatedb and the locate command with practical examples.

**Example:**
```bash
sudo updatedb
```

**Output (sample):**
```text
No output on success.
```

### 20. `which`
**संक्षिप्त जानकारी:** the Linux which command, learn how to locate the path of executable files, and discover advanced usage scenarios with practical examples.

**Example:**
```bash
which bash
```

**Output (sample):**
```text
/usr/bin/bash
```

### 21. `whereis`
**संक्षिप्त जानकारी:** the Linux whereis command and learn how to locate executable files, source code, and manual pages on your system. Customize the search behavior to suit your needs.

**Example:**
```bash
whereis bash
```

**Output (sample):**
```text
bash: /usr/bin/bash /usr/share/man/man1/bash.1.gz
```

### 22. `file`
**संक्षिप्त जानकारी:** the versatile file command in Linux, learn to identify file types, and handle compressed files effectively.

**Example:**
```bash
file hello.txt
```

**Output (sample):**
```text
hello.txt: ASCII text
```

### 23. `od`
**संक्षिप्त जानकारी:** the od command in Linux, learn its options, and perform hexadecimal dumps of files with practical examples.

**Example:**
```bash
od -An -tc hello.txt
```

**Output (sample):**
```text
 H e l l o \n
```

### 24. `mktemp`
**संक्षिप्त जानकारी:** the mktemp command in Linux, learn how to create secure temporary files, and discover practical examples for efficient file management.

**Example:**
```bash
mktemp
```

**Output (sample):**
```text
/tmp/tmp.XYZ123
```

### 25. `basename`
**संक्षिप्त जानकारी:** the basename command in Linux, learn how to extract filenames from full paths, and combine it with other commands for efficient file and directory operations.

**Example:**
```bash
basename /home/user/file.txt
```

**Output (sample):**
```text
file.txt
```

### 26. `dirname`
**संक्षिप्त जानकारी:** how to use the dirname command in Linux to retrieve the directory name from a file path. Explore practical examples and combine dirname with other Linux commands.

**Example:**
```bash
dirname /home/user/file.txt
```

**Output (sample):**
```text
/home/user
```

### 27. `dirs`
**संक्षिप्त जानकारी:** the Linux dirs command, which allows you to manage the directory stack, navigate directories efficiently, and understand the practical applications of this powerful tool.

**Example:**
```bash
dirs
```

**Output (sample):**
```text
~ /var/log
```

### 28. `mc`
**संक्षिप्त जानकारी:** the Midnight Commander (mc) file manager, learn how to install it on Ubuntu 22.04, and perform essential file and directory operations using this powerful command-line tool.

**Example:**
```bash
mc --help
```

**Output (sample):**
```text
Usage/help information for `mc` (illustrative; exact output varies by distribution/version).
```

### 29. `readlink`
**संक्षिप्त जानकारी:** the readlink command in Linux, learn its syntax and options, and practice resolving symbolic links with practical examples.

**Example:**
```bash
readlink -f syslog.link
```

**Output (sample):**
```text
/var/log/syslog
```

### 30. `rename`
**संक्षिप्त जानकारी:** how to use the Linux rename command to efficiently rename files and directories. Explore practical examples and batch renaming techniques.

**Example:**
```bash
rename 's/\.txt$/.bak/' *.txt
```

**Output (sample):**
```text
No output on success.
```

### 31. `rmdir`
**संक्षिप्त जानकारी:** the rmdir command in Linux, learn how to create and delete empty directories, and remove non-empty directories using practical examples.

**Example:**
```bash
rmdir emptydir
```

**Output (sample):**
```text
No output on success.
```

### 32. `shred`
**संक्षिप्त जानकारी:** the Linux shred command, which securely deletes files by overwriting their contents multiple times, ensuring complete data erasure. Learn practical examples of using shred to delete files and wipe disk partitions.

**Example:**
```bash
shred -n 1 -z secret.txt
```

**Output (sample):**
```text
No output on success.
```

### 33. `chattr`
**संक्षिप्त जानकारी:** the Linux chattr command, learn how to modify file attributes, and protect important files with the immutable attribute. Gain a deeper understanding of file management in Linux.

**Example:**
```bash
sudo chattr +i important.txt
```

**Output (sample):**
```text
No output on success.
```

### 34. `lsattr`
**संक्षिप्त जानकारी:** the lsattr command in Linux, which allows you to view and manage file attributes. Learn how to use this powerful tool to understand and manipulate file properties, enhancing your file management skills.

**Example:**
```bash
lsattr important.txt
```

**Output (sample):**
```text
----i--------- important.txt
```

### 35. `cksum`
**संक्षिप्त जानकारी:** the cksum command in Linux, learn how to calculate checksums for files, and verify file integrity using practical examples.

**Example:**
```bash
cksum hello.txt
```

**Output (sample):**
```text
123456789 12 hello.txt
```

### 36. `cmp`
**संक्षिप्त जानकारी:** the cmp command in Linux, learn how to compare text and binary files, and gain practical experience with hands-on examples.

**Example:**
```bash
cmp file1.txt file2.txt
```

**Output (sample):**
```text
No output if the files are identical.
```

### 37. `mtools`
**संक्षिप्त जानकारी:** the mtools command-line utilities for managing floppy disk images on Ubuntu 22.04. Learn how to install mtools, use various commands, and perform practical operations on floppy disk images.

**Example:**
```bash
mtools --help
```

**Output (sample):**
```text
Usage/help information for `mtools` (illustrative; exact output varies by distribution/version).
```

### 38. `mcopy`
**संक्षिप्त जानकारी:** the Linux mcopy command, learn how to copy files and directories, and discover advanced options for efficient file management.

**Example:**
```bash
mcopy --help
```

**Output (sample):**
```text
Usage/help information for `mcopy` (illustrative; exact output varies by distribution/version).
```

### 39. `mdel`
**संक्षिप्त जानकारी:** the mdel command in Linux, learn its syntax, and practice creating and managing multiple directories using practical examples.

**Example:**
```bash
mdel --help
```

**Output (sample):**
```text
Usage/help information for `mdel` (illustrative; exact output varies by distribution/version).
```

### 40. `mdir`
**संक्षिप्त जानकारी:** the Linux mdir command with practical examples. Learn how to create and manage directories, and discover advanced options for efficient directory operations.

**Example:**
```bash
mdir --help
```

**Output (sample):**
```text
Usage/help information for `mdir` (illustrative; exact output varies by distribution/version).
```

### 41. `mmove`
**संक्षिप्त जानकारी:** the Linux mmove command and learn how to effectively move files and directories with practical examples. Discover advanced options to enhance your file management skills.

**Example:**
```bash
mmove --help
```

**Output (sample):**
```text
Usage/help information for `mmove` (illustrative; exact output varies by distribution/version).
```

### 42. `mread`
**संक्षिप्त जानकारी:** the Linux mread command and learn how to use it for efficient file reading with practical examples.

**Example:**
```bash
mread --help
```

**Output (sample):**
```text
Usage/help information for `mread` (illustrative; exact output varies by distribution/version).
```

### 43. `mren`
**संक्षिप्त जानकारी:** the mren command in Linux, a powerful tool for renaming multiple files efficiently. Learn practical examples and advanced usage with regular expressions.

**Example:**
```bash
mren --help
```

**Output (sample):**
```text
Usage/help information for `mren` (illustrative; exact output varies by distribution/version).
```

### 44. `mshowfat`
**संक्षिप्त जानकारी:** the mshowfat command in Linux, which provides detailed information about the FAT file system structure. Learn how to use mshowfat to analyze and troubleshoot FAT-based storage devices.

**Example:**
```bash
mshowfat --help
```

**Output (sample):**
```text
Usage/help information for `mshowfat` (illustrative; exact output varies by distribution/version).
```

### 45. `mtype`
**संक्षिप्त जानकारी:** the Linux mtype command, its options, and practical examples to enhance your understanding of basic file and directory operations.

**Example:**
```bash
mtype --help
```

**Output (sample):**
```text
Usage/help information for `mtype` (illustrative; exact output varies by distribution/version).
```

### 46. `mattrib`
**संक्षिप्त जानकारी:** the Linux mattrib command and its practical applications for modifying file attributes, managing multiple files and directories, and understanding its syntax and purpose.

**Example:**
```bash
mattrib --help
```

**Output (sample):**
```text
Usage/help information for `mattrib` (illustrative; exact output varies by distribution/version).
```

### 47. `mmd`
**संक्षिप्त जानकारी:** the mmd command in Linux, learn how to create Markdown files, and convert them to HTML and PDF formats for various use cases.

**Example:**
```bash
mmd --help
```

**Output (sample):**
```text
Usage/help information for `mmd` (illustrative; exact output varies by distribution/version).
```

### 48. `mrd`
**संक्षिप्त जानकारी:** the mrd command in Linux, a tool for managing directories. Learn its syntax, options, and practical applications through hands-on exercises.

**Example:**
```bash
mrd --help
```

**Output (sample):**
```text
Usage/help information for `mrd` (illustrative; exact output varies by distribution/version).
```

### 49. `mzip`
**संक्षिप्त जानकारी:** the mzip command in Linux, learn how to compress and extract files and directories using this versatile tool, and gain practical experience with real- world examples.

**Example:**
```bash
mzip --help
```

**Output (sample):**
```text
Usage/help information for `mzip` (illustrative; exact output varies by distribution/version).
```

### 50. `mtoolstest`
**संक्षिप्त जानकारी:** the mtoolstest command in Linux, learn how to verify its installation, and discover practical examples of its usage for file and directory operations.

**Example:**
```bash
mtoolstest --help
```

**Output (sample):**
```text
Usage/help information for `mtoolstest` (illustrative; exact output varies by distribution/version).
```

### 51. `tee`
**संक्षिप्त जानकारी:** the versatile tee command in Linux, learn how to redirect output to both a file and the terminal, and append output to existing files.

**Example:**
```bash
echo 'Hello' | tee hello.txt
```

**Output (sample):**
```text
Hello
```

### 52. `read`
**संक्षिप्त जानकारी:** the Linux read command and learn how to use it to capture user input, store it in variables, and validate the input. Gain practical experience through hands-on examples.

**Example:**
```bash
read name; echo "Hello $name"
```

**Output (sample):**
```text
Hello Prakash
```

---

<a id="cat-53-96"></a>
## 📝 Text Processing and Editing

**Commands 53–96 (44 commands)**

### 53. `grep`
**संक्षिप्त जानकारी:** the powerful grep command in Linux, learn how to search for patterns in text files, and combine grep with other commands for efficient text processing.

**Example:**
```bash
grep 'error' app.log
```

**Output (sample):**
```text
2026-08-21 error: connection failed
```

### 54. `sed`
**संक्षिप्त जानकारी:** the power of the sed command in Linux, learning how to perform text substitution, edit multiple files, and more through practical examples.

**Example:**
```bash
sed 's/Linux/Ubuntu/g' file.txt
```

**Output (sample):**
```text
Ubuntu is powerful.
```

### 55. `awk`
**संक्षिप्त जानकारी:** the power of the awk command in Linux, learn how to perform text processing, data manipulation, and analysis with practical examples.

**Example:**
```bash
awk '{print $1}' users.txt
```

**Output (sample):**
```text
alice
bob
```

### 56. `cut`
**संक्षिप्त जानकारी:** the versatile Linux cut command and learn how to extract specific columns from text files. Discover practical examples to enhance your text processing skills.

**Example:**
```bash
cut -d: -f1 /etc/passwd | head -n 2
```

**Output (sample):**
```text
root
user
```

### 57. `paste`
**संक्षिप्त जानकारी:** how to use the Linux paste command to combine multiple files, customize the output, and perform efficient text processing tasks.

**Example:**
```bash
paste names.txt ages.txt
```

**Output (sample):**
```text
Alice	30
Bob	25
```

### 58. `sort`
**संक्षिप्त जानकारी:** the powerful sort command in Linux, learn how to sort files by different criteria, and combine it with other commands for efficient text processing.

**Example:**
```bash
sort names.txt
```

**Output (sample):**
```text
Alice
Bob
Charlie
```

### 59. `uniq`
**संक्षिप्त जानकारी:** the uniq command in Linux, learn its syntax, and discover practical examples to remove duplicate lines and count unique occurrences in text files.

**Example:**
```bash
sort names.txt | uniq
```

**Output (sample):**
```text
Alice
Bob
Charlie
```

### 60. `tr`
**संक्षिप्त जानकारी:** the powerful Linux tr command and learn how to translate, delete, squeeze, and complement characters in text processing with practical examples.

**Example:**
```bash
echo 'hello' | tr 'a-z' 'A-Z'
```

**Output (sample):**
```text
HELLO
```

### 61. `head`
**संक्षिप्त जानकारी:** the Linux head command and learn how to use it effectively for text processing and editing tasks. Discover practical examples and master the various options to extract the top lines from files.

**Example:**
```bash
head -n 3 file.txt
```

**Output (sample):**
```text
line 1
line 2
line 3
```

### 62. `tail`
**संक्षिप्त जानकारी:** the Linux tail command and its practical applications, including monitoring log files and viewing the end of text files.

**Example:**
```bash
tail -n 3 file.txt
```

**Output (sample):**
```text
line 8
line 9
line 10
```

### 63. `wc`
**संक्षिप्त जानकारी:** the Linux wc command and learn how to count words, lines, and characters in files. Discover practical examples of using wc with other Linux commands for efficient text processing.

**Example:**
```bash
wc -l file.txt
```

**Output (sample):**
```text
10 file.txt
```

### 64. `diff`
**संक्षिप्त जानकारी:** the Linux diff command, a powerful tool for comparing and analyzing text files. Learn its syntax, practical examples, and advanced options to effectively manage and process text data.

**Example:**
```bash
diff file1.txt file2.txt
```

**Output (sample):**
```text
2c2
< old
---
> new
```

### 65. `patch`
**संक्षिप्त जानकारी:** how to use the Linux patch command to apply and revert changes to files. Explore practical examples and understand the syntax and purpose of this powerful text editing tool.

**Example:**
```bash
patch < changes.patch
```

**Output (sample):**
```text
patching file file.txt
```

### 66. `split`
**संक्षिप्त जानकारी:** the Linux split command and its practical applications. Learn how to split files into multiple parts, customize the split options, and efficiently manage your text data.

**Example:**
```bash
split -l 100 big.txt part_
```

**Output (sample):**
```text
part_aa
part_ab
```

### 67. `join`
**संक्षिप्त जानकारी:** the power of the join command in Linux, learn its syntax, and apply it to merge files based on common fields. Gain practical experience through step-by- step examples.

**Example:**
```bash
join users.txt departments.txt
```

**Output (sample):**
```text
101 Alice IT
```

### 68. `fmt`
**संक्षिप्त जानकारी:** the fmt command in Linux, a powerful tool for formatting text files. Learn how to use it effectively with practical examples and customization options.

**Example:**
```bash
fmt -w 40 notes.txt
```

**Output (sample):**
```text
Wrapped text output ...
```

### 69. `fold`
**संक्षिप्त जानकारी:** the Linux fold command and its practical applications for text processing and editing. Learn to fold text files with different column widths and combine the fold command with other Linux tools.

**Example:**
```bash
fold -w 20 file.txt
```

**Output (sample):**
```text
Long line wrapped at 20 columns.
```

### 70. `expand`
**संक्षिप्त जानकारी:** the Linux expand command and learn how to convert tabs to spaces in single or multiple files, enhancing text processing and editing workflows.

**Example:**
```bash
expand -t 4 file.txt
```

**Output (sample):**
```text
Tabs converted to spaces.
```

### 71. `col`
**संक्षिप्त जानकारी:** the versatile col command in Linux, learn how to manipulate tabular data, and combine it with other commands for advanced text formatting.

**Example:**
```bash
man ls | col -b | head -n 2
```

**Output (sample):**
```text
LS(1)
User Commands
```

### 72. `colrm`
**संक्षिप्त जानकारी:** how to use the Linux colrm command to remove specific columns from a file. Explore practical examples and combine colrm with other commands for efficient text processing.

**Example:**
```bash
printf 'abcdef\n' | colrm 3 4
```

**Output (sample):**
```text
abef
```

### 73. `comm`
**संक्षिप्त जानकारी:** the powerful comm command in Linux, learn how to compare and contrast sorted files, and customize the output with various options. Enhance your text processing and editing skills.

**Example:**
```bash
comm file1.txt file2.txt
```

**Output (sample):**
```text
Lines unique to file1
	Lines unique to file2
		Common lines
```

### 74. `csplit`
**संक्षिप्त जानकारी:** the csplit command in Linux, learn how to split files into multiple parts, and discover customization options for efficient text processing.

**Example:**
```bash
csplit file.txt '/^SECTION/'
```

**Output (sample):**
```text
100
250
```

### 75. `ispell`
**संक्षिप्त जानकारी:** how to use the ispell command in Linux to check the spelling of single words and text files. Explore practical examples and gain proficiency in text processing and editing.

**Example:**
```bash
ispell --help
```

**Output (sample):**
```text
Usage/help information for `ispell` (illustrative; exact output varies by distribution/version).
```

### 76. `spell`
**संक्षिप्त जानकारी:** the Linux spell command, learn how to install and use it for basic spell checking on text files. Enhance your text processing and editing skills.

**Example:**
```bash
spell --help
```

**Output (sample):**
```text
Usage/help information for `spell` (illustrative; exact output varies by distribution/version).
```

### 77. `diffstat`
**संक्षिप्त जानकारी:** the diffstat command, a powerful tool for analyzing changes in text files. Learn how to use diffstat to process patch files, Git diffs, and more, with practical examples.

**Example:**
```bash
diffstat --help
```

**Output (sample):**
```text
Usage/help information for `diffstat` (illustrative; exact output varies by distribution/version).
```

### 78. `expr`
**संक्षिप्त जानकारी:** the versatile expr command in Linux, learn its syntax, and discover practical examples for performing arithmetic operations, string manipulation, and conditional expressions.

**Example:**
```bash
expr 10 + 5
```

**Output (sample):**
```text
15
```

### 79. `aspell`
**संक्षिप्त जानकारी:** the Linux aspell command and learn how to correct spelling errors in text files, customize the aspell dictionary, and adjust preferences for efficient text processing and editing.

**Example:**
```bash
aspell check notes.txt
```

**Output (sample):**
```text
Interactive spell checker opens.
```

### 80. `emacs`
**संक्षिप्त जानकारी:** the powerful emacs text editor with this hands-on lab. Learn basic commands, shortcuts, and how to customize emacs for efficient text processing and editing.

**Example:**
```bash
emacs --help
```

**Output (sample):**
```text
Usage/help information for `emacs` (illustrative; exact output varies by distribution/version).
```

### 81. `gawk`
**संक्षिप्त जानकारी:** the powerful gawk command in Linux, learn how to extract data from text files, perform calculations, and transform data efficiently.

**Example:**
```bash
gawk '{print $1}' users.txt
```

**Output (sample):**
```text
alice
bob
```

### 82. `indent`
**संक्षिप्त जानकारी:** the Linux indent command, learn its syntax, and discover practical examples to format C/C++ source code with customizable options for different coding styles.

**Example:**
```bash
indent --help
```

**Output (sample):**
```text
Usage/help information for `indent` (illustrative; exact output varies by distribution/version).
```

### 83. `sdiff`
**संक्षिप्त जानकारी:** the sdiff command in Linux, a powerful tool for comparing and merging text files. Learn its syntax, practical examples, and how to customize the output for efficient text processing and editing.

**Example:**
```bash
sdiff file1.txt file2.txt
```

**Output (sample):**
```text
same line              same line
```

### 84. `tac`
**संक्षिप्त जानकारी:** the tac command in Linux, which reverses the order of lines in a text file. Learn practical examples and how to combine tac with other commands for advanced text processing.

**Example:**
```bash
tac file.txt
```

**Output (sample):**
```text
last line
first line
```

### 85. `unexpand`
**संक्षिप्त जानकारी:** the Linux unexpand command, which converts spaces to tabs, with practical examples. Learn how to customize the command and optimize text processing workflows.

**Example:**
```bash
unexpand -a file.txt
```

**Output (sample):**
```text
Spaces converted to tabs.
```

### 86. `unix2dos`
**संक्षिप्त जानकारी:** how to use the unix2dos command to convert text files from Unix to DOS format, handle newline characters, and perform practical text processing tasks on Linux/Unix systems.

**Example:**
```bash
unix2dos file.txt
```

**Output (sample):**
```text
unix2dos: converting file file.txt to DOS format...
```

### 87. `vi`
**संक्षिप्त जानकारी:** the powerful vi text editor in Linux, learn its basic navigation and editing commands, and dive into advanced features for efficient text processing.

**Example:**
```bash
vi notes.txt
```

**Output (sample):**
```text
Interactive editor opens.
```

### 88. `ed`
**संक्षिप्त जानकारी:** the powerful Linux ed command for text processing and editing. Learn how to edit text files, perform advanced operations, and enhance your command- line skills.

**Example:**
```bash
ed --help
```

**Output (sample):**
```text
Usage/help information for `ed` (illustrative; exact output varies by distribution/version).
```

### 89. `egrep`
**संक्षिप्त जानकारी:** the powerful egrep command in Linux, learn how to use regular expressions for efficient text processing, and discover practical examples to enhance your text manipulation skills.

**Example:**
```bash
egrep 'error|warning' app.log
```

**Output (sample):**
```text
error: failed
warning: retrying
```

### 90. `ex`
**संक्षिप्त जानकारी:** the ex command, a powerful text editor in Linux. Learn the basics, perform editing operations, and automate ex commands using scripts for efficient text processing.

**Example:**
```bash
ex --help
```

**Output (sample):**
```text
Usage/help information for `ex` (illustrative; exact output varies by distribution/version).
```

### 91. `fgrep`
**संक्षिप्त जानकारी:** the fgrep command in Linux, a powerful tool for searching fixed strings in text files. Learn practical examples and techniques to efficiently manipulate text data.

**Example:**
```bash
fgrep 'hello.world' file.txt
```

**Output (sample):**
```text
hello.world
```

### 92. `jed`
**संक्षिप्त जानकारी:** the jed text editor, a powerful and versatile tool for text processing and editing on Linux systems. Learn basic commands, navigation, and customization to enhance your productivity.

**Example:**
```bash
jed --help
```

**Output (sample):**
```text
Usage/help information for `jed` (illustrative; exact output varies by distribution/version).
```

### 93. `joe`
**संक्षिप्त जानकारी:** the powerful joe text editor on Ubuntu 22.04. Learn how to install, create, edit, and customize files using the joe command-line tool.

**Example:**
```bash
joe --help
```

**Output (sample):**
```text
Usage/help information for `joe` (illustrative; exact output varies by distribution/version).
```

### 94. `look`
**संक्षिप्त जानकारी:** how to use the Linux look command to search for specific words or phrases in text files. Explore practical examples and combine the look command with other Linux tools for efficient text processing.

**Example:**
```bash
look pre /usr/share/dict/words | head
```

**Output (sample):**
```text
prefix
prepare
present
```

### 95. `pico`
**संक्षिप्त जानकारी:** the pico text editor, a user- friendly command-line tool for text processing and editing on Linux systems. Learn basic commands, customization options, and practical examples to enhance your productivity.

**Example:**
```bash
pico --help
```

**Output (sample):**
```text
Usage/help information for `pico` (illustrative; exact output varies by distribution/version).
```

### 96. `column`
**संक्षिप्त जानकारी:** the Linux column command and learn how to format tabular data, customize output, and apply practical examples to enhance your text processing skills.

**Example:**
```bash
printf 'a 1\nb 2\n' | column -t
```

**Output (sample):**
```text
a  1
b  2
```

---

<a id="cat-97-145"></a>
## 📊 System Monitoring and Management

**Commands 97–145 (49 commands)**

### 97. `top`
**संक्षिप्त जानकारी:** the powerful top command in Linux, learn its options and customizations, and analyze system performance using real-world examples.

**Example:**
```bash
top
```

**Output (sample):**
```text
Interactive process monitor opens.
```

### 98. `ps`
**संक्षिप्त जानकारी:** the powerful Linux ps command and learn how to filter processes by user, monitor CPU and memory usage, and gain practical insights into system monitoring and management.

**Example:**
```bash
ps aux | head -n 3
```

**Output (sample):**
```text
USER PID %CPU %MEM COMMAND
root 1 ... /sbin/init
```

### 99. `free`
**संक्षिप्त जानकारी:** the Linux free command, learn its syntax, and analyze memory usage with practical examples. Customize the free command output to suit your system monitoring needs.

**Example:**
```bash
free -h
```

**Output (sample):**
```text
               total  used  free
Mem:            7.7Gi  3.1Gi  1.8Gi
```

### 100. `uname`
**संक्षिप्त जानकारी:** the versatile uname command in Linux, which provides detailed information about your system's hardware and software configurations. Learn how to retrieve system details and combine options for comprehensive output.

**Example:**
```bash
uname -a
```

**Output (sample):**
```text
Linux host 6.x.x-generic x86_64 GNU/Linux
```

### 101. `uptime`
**संक्षिप्त जानकारी:** the Linux uptime command and its practical applications for monitoring system uptime and load average. Learn how to effectively utilize this tool for system management and troubleshooting.

**Example:**
```bash
uptime
```

**Output (sample):**
```text
11:57:00 up 3 days, 2:10, 1 user, load average: 0.10, 0.08, 0.05
```

### 102. `lsof`
**संक्षिप्त जानकारी:** the powerful lsof command in Linux, learn how to identify open files by a process, and locate network connections. Gain practical system monitoring and management skills.

**Example:**
```bash
lsof -i :80
```

**Output (sample):**
```text
COMMAND PID USER FD TYPE DEVICE SIZE/OFF NODE NAME
nginx ... TCP *:http
```

### 103. `vmstat`
**संक्षिप्त जानकारी:** the powerful vmstat command in Linux, learn how to monitor system performance, and analyze CPU, memory, and disk I/O metrics with practical examples.

**Example:**
```bash
vmstat 1 2
```

**Output (sample):**
```text
procs ... memory ... swap ... io ... cpu ...
```

### 104. `iostat`
**संक्षिप्त जानकारी:** the powerful iostat command in Linux, learn to analyze CPU and I/O statistics, and monitor disk performance for effective system monitoring and management.

**Example:**
```bash
iostat
```

**Output (sample):**
```text
avg-cpu:  %user  %system  %idle
...
```

### 105. `dmesg`
**संक्षिप्त जानकारी:** the Linux kernel ring buffer using the dmesg command. Learn how to filter and analyze the output to monitor system events and troubleshoot issues.

**Example:**
```bash
dmesg | tail -n 3
```

**Output (sample):**
```text
[...] kernel: device event ...
```

### 106. `htop`
**संक्षिप्त जानकारी:** the powerful htop command in Linux, a real-time system monitoring tool. Learn how to navigate, interact, and customize htop to efficiently monitor and manage your system resources.

**Example:**
```bash
htop
```

**Output (sample):**
```text
Interactive process monitor opens.
```

### 107. `lshw`
**संक्षिप्त जानकारी:** the lshw command, a powerful tool for gathering detailed hardware information on your Linux system. Learn how to use lshw to customize output and save data to a file for analysis.

**Example:**
```bash
sudo lshw -short
```

**Output (sample):**
```text
H/W path  Device  Class  Description
/0 ... system ...
```

### 108. `lsusb`
**संक्षिप्त जानकारी:** the Linux lsusb command and learn how to use it to identify USB device information on your system. Understand the purpose and basic usage of this powerful system monitoring tool.

**Example:**
```bash
lsusb
```

**Output (sample):**
```text
Bus 001 Device 002: ID 1234:5678 USB Device
```

### 109. `lsblk`
**संक्षिप्त जानकारी:** the lsblk command in Linux, which lists information about block devices. Learn how to use various options and filters to effectively manage and monitor your system's storage devices.

**Example:**
```bash
lsblk
```

**Output (sample):**
```text
NAME   MAJ:MIN RM  SIZE RO TYPE MOUNTPOINTS
sda ...
```

### 110. `mpstat`
**संक्षिप्त जानकारी:** the Linux mpstat command, a powerful tool for monitoring and analyzing CPU utilization metrics across multiple CPUs. Learn how to use mpstat to gain insights into system performance and optimize resource allocation.

**Example:**
```bash
mpstat 1 2
```

**Output (sample):**
```text
Linux ...
Average: all  ... %idle
```

### 111. `pidof`
**संक्षिप्त जानकारी:** the Linux pidof command and its practical applications for finding the process ID (PID) of running processes. Learn how to locate multiple processes with the same name and gain insights into system monitoring and...

**Example:**
```bash
pidof sshd
```

**Output (sample):**
```text
812 790
```

### 112. `sar`
**संक्षिप्त जानकारी:** the powerful sar command in Linux and learn how to analyze system performance metrics through practical examples.

**Example:**
```bash
sar --help
```

**Output (sample):**
```text
Usage/help information for `sar` (illustrative; exact output varies by distribution/version).
```

### 113. `procinfo`
**संक्षिप्त जानकारी:** the Linux procinfo command and learn how to monitor system information, customize output, and gain practical insights into system performance and resource utilization.

**Example:**
```bash
procinfo --help
```

**Output (sample):**
```text
Usage/help information for `procinfo` (illustrative; exact output varies by distribution/version).
```

### 114. `pstree`
**संक्षिप्त जानकारी:** the process hierarchy on your Linux system using the pstree command. Learn how to filter and customize the output to gain a deeper understanding of your system's processes.

**Example:**
```bash
pstree -p | head
```

**Output (sample):**
```text
systemd(1)-+-sshd(790)---bash(812)
```

### 115. `tload`
**संक्षिप्त जानकारी:** the Linux tload command, a powerful tool for monitoring system load average. Learn how to interpret tload output and identify performance issues on your system.

**Example:**
```bash
tload --help
```

**Output (sample):**
```text
Usage/help information for `tload` (illustrative; exact output varies by distribution/version).
```

### 116. `logrotate`
**संक्षिप्त जानकारी:** the logrotate command in Linux, learn how to configure it for Apache web server logs, and customize the configuration for specific log files.

**Example:**
```bash
logrotate --help
```

**Output (sample):**
```text
Usage/help information for `logrotate` (illustrative; exact output varies by distribution/version).
```

### 117. `watch`
**संक्षिप्त जानकारी:** the powerful Linux watch command and its practical applications, including monitoring system processes and tracking file changes.

**Example:**
```bash
watch -n 2 'df -h /'
```

**Output (sample):**
```text
Repeated command output every 2 seconds.
```

### 118. `time`
**संक्षिप्त जानकारी:** the Linux time command and learn how to measure the execution time of commands, analyze their performance, and optimize system efficiency.

**Example:**
```bash
time sleep 1
```

**Output (sample):**
```text
real	0m1.00s
user	0m0.00s
sys	0m0.00s
```

### 119. `date`
**संक्षिप्त जानकारी:** the Linux date command and learn how to display, format, and manipulate date and time information on your system.

**Example:**
```bash
date '+%Y-%m-%d'
```

**Output (sample):**
```text
2026-08-21
```

### 120. `cal`
**संक्षिप्त जानकारी:** the Linux cal command, learn its syntax, and practice using it to display calendars for the current month, specific years, and months.

**Example:**
```bash
cal 2026
```

**Output (sample):**
```text
2026 calendar displayed.
```

### 121. `arch`
**संक्षिप्त जानकारी:** the arch command in Linux, learn how to identify your system's hardware architecture, and discover practical scenarios for using this powerful tool.

**Example:**
```bash
arch
```

**Output (sample):**
```text
x86_64
```

### 122. `dmidecode`
**संक्षिप्त जानकारी:** the dmidecode command, a powerful tool for retrieving detailed hardware information on Linux systems. Learn how to display system hardware details and extract specific hardware data.

**Example:**
```bash
dmidecode --help
```

**Output (sample):**
```text
Usage/help information for `dmidecode` (illustrative; exact output varies by distribution/version).
```

### 123. `dstat`
**संक्षिप्त जानकारी:** the dstat command, a versatile system monitoring tool, and learn how to use it to monitor CPU utilization, memory usage, and other system metrics on your Linux machine.

**Example:**
```bash
dstat --help
```

**Output (sample):**
```text
Usage/help information for `dstat` (illustrative; exact output varies by distribution/version).
```

### 124. `iotop`
**संक्षिप्त जानकारी:** the Linux iotop command, a powerful tool for monitoring disk I/O usage. Learn how to install, configure, and utilize iotop to analyze system performance and identify resource- intensive processes.

**Example:**
```bash
iotop --help
```

**Output (sample):**
```text
Usage/help information for `iotop` (illustrative; exact output varies by distribution/version).
```

### 125. `journalctl`
**संक्षिप्त जानकारी:** the powerful journalctl command in Linux, learn how to filter and analyze system logs, and gain practical experience with real-world examples.

**Example:**
```bash
journalctl -n 5
```

**Output (sample):**
```text
Recent systemd journal entries ...
```

### 126. `pmap`
**संक्षिप्त जानकारी:** the pmap command in Linux, a powerful tool for analyzing memory usage and identifying memory leaks in processes. Learn practical examples to optimize system performance.

**Example:**
```bash
pmap --help
```

**Output (sample):**
```text
Usage/help information for `pmap` (illustrative; exact output varies by distribution/version).
```

### 127. `adduser`
**संक्षिप्त जानकारी:** the Linux adduser command with practical examples. Learn how to create new user accounts, set passwords and expiration, and add users to existing groups for effective system management.

**Example:**
```bash
sudo adduser demo
```

**Output (sample):**
```text
Adding user `demo` ...
Adding new group `demo` ...
```

### 128. `chage`
**संक्षिप्त जानकारी:** the chage command in Linux, learn how to modify user password expiration dates, and enforce password expiration policies for enhanced system security.

**Example:**
```bash
chage --help
```

**Output (sample):**
```text
Usage/help information for `chage` (illustrative; exact output varies by distribution/version).
```

### 129. `chpasswd`
**संक्षिप्त जानकारी:** the chpasswd command in Linux, learn how to change user passwords in batch mode, and automate password changes using shell scripts.

**Example:**
```bash
chpasswd --help
```

**Output (sample):**
```text
Usage/help information for `chpasswd` (illustrative; exact output varies by distribution/version).
```

### 130. `grpck`
**संक्षिप्त जानकारी:** the Linux grpck command, which verifies the integrity of the group file. Learn how to use grpck to identify and repair group file issues, ensuring the proper management of user groups on your system.

**Example:**
```bash
grpck --help
```

**Output (sample):**
```text
Usage/help information for `grpck` (illustrative; exact output varies by distribution/version).
```

### 131. `vlock`
**संक्षिप्त जानकारी:** the Linux vlock command, which allows you to lock the current terminal session, providing a secure way to protect your system when stepping away from your computer.

**Example:**
```bash
vlock --help
```

**Output (sample):**
```text
Usage/help information for `vlock` (illustrative; exact output varies by distribution/version).
```

### 132. `logout`
**संक्षिप्त जानकारी:** the Linux logout command, learn its purpose, and discover practical examples to automate logout sessions using shell scripts.

**Example:**
```bash
help logout
```

**Output (sample):**
```text
Built-in shell command 'logout'; output/behavior depends on the shell.
```

### 133. `login`
**संक्षिप्त जानकारी:** the login command in Linux, learn how to log in as a regular user and the root user, and gain practical experience with hands-on examples.

**Example:**
```bash
login --help
```

**Output (sample):**
```text
Usage/help information for `login` (illustrative; exact output varies by distribution/version).
```

### 134. `logname`
**संक्षिप्त जानकारी:** the Linux logname command, its syntax, and practical examples to understand the current user's login name. Learn how to effectively use this command for system monitoring and management tasks.

**Example:**
```bash
logname --help
```

**Output (sample):**
```text
Usage/help information for `logname` (illustrative; exact output varies by distribution/version).
```

### 135. `rlogin`
**संक्षिप्त जानकारी:** the rlogin command in Linux, learn how to establish remote login sessions, execute remote commands, and transfer files securely between systems.

**Example:**
```bash
rlogin --help
```

**Output (sample):**
```text
Usage/help information for `rlogin` (illustrative; exact output varies by distribution/version).
```

### 136. `rsh`
**संक्षिप्त जानकारी:** the rsh command in Linux, learn how to establish remote shell connections, and execute remote commands effectively.

**Example:**
```bash
rsh --help
```

**Output (sample):**
```text
Usage/help information for `rsh` (illustrative; exact output varies by distribution/version).
```

### 137. `sliplogin`
**संक्षिप्त जानकारी:** the sliplogin command in Linux, learn how to configure it, and troubleshoot any issues that may arise, with practical examples to enhance your system monitoring and management skills.

**Example:**
```bash
sliplogin --help
```

**Output (sample):**
```text
Usage/help information for `sliplogin` (illustrative; exact output varies by distribution/version).
```

### 138. `swatch`
**संक्षिप्त जानकारी:** the swatch command in Linux, a powerful tool for monitoring log files and setting up custom alerts. Learn how to configure swatch to monitor specific events and receive notifications.

**Example:**
```bash
swatch --help
```

**Output (sample):**
```text
Usage/help information for `swatch` (illustrative; exact output varies by distribution/version).
```

### 139. `w`
**संक्षिप्त जानकारी:** the w command in Linux, learn how to analyze user login sessions, and monitor system load and resource utilization for effective system management.

**Example:**
```bash
w --help
```

**Output (sample):**
```text
Usage/help information for `w` (illustrative; exact output varies by distribution/version).
```

### 140. `rwho`
**संक्षिप्त जानकारी:** the rwho command in Linux, which allows you to monitor users logged into remote systems. Learn how to utilize this tool for user monitoring and system management.

**Example:**
```bash
rwho --help
```

**Output (sample):**
```text
Usage/help information for `rwho` (illustrative; exact output varies by distribution/version).
```

### 141. `shutdown`
**संक्षिप्त जानकारी:** the Linux shutdown command and its practical applications, including immediate system shutdown and scheduled shutdowns at specific times.

**Example:**
```bash
shutdown --help
```

**Output (sample):**
```text
Usage/help information for `shutdown` (illustrative; exact options vary by distribution).
```

### 142. `halt`
**संक्षिप्त जानकारी:** the Linux halt command, learn how to shut down the system, and discover additional options for managing system shutdown processes.

**Example:**
```bash
halt --help
```

**Output (sample):**
```text
Usage/help information for `halt` (illustrative; exact options vary by distribution).
```

### 143. `reboot`
**संक्षिप्त जानकारी:** the Linux reboot command and learn how to reboot your system immediately or schedule a reboot at a specific time. Gain practical knowledge for system monitoring and management.

**Example:**
```bash
reboot --help
```

**Output (sample):**
```text
Usage/help information for `reboot` (illustrative; exact options vary by distribution).
```

### 144. `exit`
**संक्षिप्त जानकारी:** the Linux exit command and its practical usage in shell scripts. Learn how to terminate scripts, utilize different exit codes, and understand the purpose of this essential command.

**Example:**
```bash
help exit
```

**Output (sample):**
```text
Built-in shell command 'exit'; output/behavior depends on the shell.
```

### 145. `suspend`
**संक्षिप्त जानकारी:** the Linux suspend command and learn how to suspend and resume the system, as well as manage power states effectively.

**Example:**
```bash
suspend --help
```

**Output (sample):**
```text
Usage/help information for `suspend` (illustrative; exact output varies by distribution/version).
```

---

<a id="cat-146-175"></a>
## 👤 User and Permission Management

**Commands 146–175 (30 commands)**

### 146. `useradd`
**संक्षिप्त जानकारी:** how to create new user accounts, assign passwords, and manage user account properties using the Linux useradd command with practical examples.

**Example:**
```bash
sudo useradd -m demo
```

**Output (sample):**
```text
No output on success.
```

### 147. `userdel`
**संक्षिप्त जानकारी:** how to use the Linux userdel command to delete user accounts, remove their home directories, and manage user permissions on your system.

**Example:**
```bash
sudo userdel -r demo
```

**Output (sample):**
```text
No output on success.
```

### 148. `usermod`
**संक्षिप्त जानकारी:** the Linux usermod command and learn how to modify user account properties, change a user's primary group, and disable user account expiration using practical examples.

**Example:**
```bash
sudo usermod -aG sudo demo
```

**Output (sample):**
```text
No output on success.
```

### 149. `groupadd`
**संक्षिप्त जानकारी:** the Linux groupadd command with practical examples, including creating new groups, adding users to groups, and modifying group properties. Enhance your user and permission management skills.

**Example:**
```bash
sudo groupadd developers
```

**Output (sample):**
```text
No output on success.
```

### 150. `groupdel`
**संक्षिप्त जानकारी:** the Linux groupdel command and learn how to delete groups effectively. This lab covers the purpose of groupdel, creating test groups, and deleting groups using practical examples.

**Example:**
```bash
sudo groupdel developers
```

**Output (sample):**
```text
No output on success.
```

### 151. `groupmod`
**संक्षिप्त जानकारी:** the Linux groupmod command with practical examples. Learn how to modify a group's name and GID, enabling effective user and permission management on your Linux system.

**Example:**
```bash
sudo groupmod -n dev developers
```

**Output (sample):**
```text
No output on success.
```

### 152. `passwd`
**संक्षिप्त जानकारी:** the Linux passwd command and learn how to change user passwords, reset forgotten passwords, and manage user permissions effectively.

**Example:**
```bash
passwd
```

**Output (sample):**
```text
passwd: password updated successfully
```

### 153. `chown`
**संक्षिप्त जानकारी:** the Linux chown command and learn how to change file ownership, including recursive ownership changes, with practical examples.

**Example:**
```bash
sudo chown user:user file.txt
```

**Output (sample):**
```text
No output on success.
```

### 154. `chmod`
**संक्षिप्त जानकारी:** the Linux chmod command with hands-on examples. Learn how to manage file permissions, change access rights, and recursively modify permissions for directories and files.

**Example:**
```bash
chmod 644 file.txt
```

**Output (sample):**
```text
No output on success.
```

### 155. `chgrp`
**संक्षिप्त जानकारी:** the chgrp command in Linux, learn how to change the group ownership of files and directories, and discover practical examples to enhance your user and permission management skills.

**Example:**
```bash
sudo chgrp developers file.txt
```

**Output (sample):**
```text
No output on success.
```

### 156. `umask`
**संक्षिप्त जानकारी:** the Linux umask command and learn how to modify file and directory permissions effectively. Discover practical examples to apply umask in various scenarios.

**Example:**
```bash
umask
```

**Output (sample):**
```text
0022
```

### 157. `sudo`
**संक्षिप्त जानकारी:** the power of the sudo command in Linux. Learn how to manage user permissions, secure your system, and execute commands with elevated privileges.

**Example:**
```bash
sudo -v
```

**Output (sample):**
```text
No output when credentials are accepted.
```

### 158. `su`
**संक्षिप्त जानकारी:** the Linux su command and learn how to switch users, manage privileges, and execute commands with elevated permissions.

**Example:**
```bash
su - demo
```

**Output (sample):**
```text
Interactive login shell for demo starts.
```

### 159. `id`
**संक्षिप्त जानकारी:** the Linux id command and learn how to use it to identify user and group information, including user ID, group ID, and supplementary groups. Discover practical examples and additional options to customize the...

**Example:**
```bash
id
```

**Output (sample):**
```text
uid=1000(user) gid=1000(user) groups=1000(user),27(sudo)
```

### 160. `who`
**संक्षिप्त जानकारी:** the Linux who command, learn how to use it, and discover practical examples to understand user sessions and system activity.

**Example:**
```bash
who
```

**Output (sample):**
```text
user  tty2  2026-08-21 10:30
```

### 161. `whoami`
**संक्षिप्त जानकारी:** the Linux whoami command and its practical applications. Learn how to use it to determine your current user identity, integrate it into shell scripts, and manage user permissions effectively.

**Example:**
```bash
whoami
```

**Output (sample):**
```text
user
```

### 162. `chfn`
**संक्षिप्त जानकारी:** the Linux chfn command, which allows you to modify user information such as the full name, office location, and phone number. Learn practical examples and advanced options to effectively manage user profiles.

**Example:**
```bash
chfn --help
```

**Output (sample):**
```text
Usage/help information for `chfn` (illustrative; exact output varies by distribution/version).
```

### 163. `chsh`
**संक्षिप्त जानकारी:** the Linux chsh command, learn how to change the default shell, and verify the changes with practical examples.

**Example:**
```bash
chsh --help
```

**Output (sample):**
```text
Usage/help information for `chsh` (illustrative; exact output varies by distribution/version).
```

### 164. `newgrp`
**संक्षिप्त जानकारी:** the Linux newgrp command and learn how to create, switch, and manage group permissions. Gain practical knowledge for effective user and permission management in your Linux environment.

**Example:**
```bash
newgrp developers
```

**Output (sample):**
```text
New shell starts with developers as the effective group.
```

### 165. `last`
**संक्षिप्त जानकारी:** the Linux last command, which displays information about the last users who have logged into the system. Learn how to use it effectively with practical examples.

**Example:**
```bash
last -n 2
```

**Output (sample):**
```text
user tty2 ... still logged in
```

### 166. `lastb`
**संक्षिप्त जानकारी:** the Linux lastb command, which displays information about failed login attempts. Learn how to analyze login failures and enhance system security.

**Example:**
```bash
sudo lastb -n 2
```

**Output (sample):**
```text
Failed login records ...
```

### 167. `finger`
**संक्षिप्त जानकारी:** the Linux finger command, which provides user information, and learn how to customize its output for practical use in user and permission management.

**Example:**
```bash
finger --help
```

**Output (sample):**
```text
Usage/help information for `finger` (illustrative; exact output varies by distribution/version).
```

### 168. `groups`
**संक्षिप्त जानकारी:** how to effectively manage user groups in Linux using the groups command. Explore practical examples of creating, assigning, and removing users from groups to enhance your system administration skills.

**Example:**
```bash
groups
```

**Output (sample):**
```text
user sudo developers
```

### 169. `gpasswd`
**संक्षिप्त जानकारी:** how to use the Linux gpasswd command to manage user group memberships. Add and remove users from groups, and explore practical examples to enhance your user and permission management skills.

**Example:**
```bash
gpasswd --help
```

**Output (sample):**
```text
Usage/help information for `gpasswd` (illustrative; exact output varies by distribution/version).
```

### 170. `pwconv`
**संक्षिप्त जानकारी:** the Linux pwconv command and learn how to create and manage user passwords effectively. Understand the purpose of pwconv and troubleshoot any password conversion issues.

**Example:**
```bash
pwconv --help
```

**Output (sample):**
```text
Usage/help information for `pwconv` (illustrative; exact output varies by distribution/version).
```

### 171. `pwunconv`
**संक्षिप्त जानकारी:** the pwunconv command in Linux, which secures user passwords by moving them from the shadow file to the password file. Learn practical scenarios for using pwunconv to manage user permissions and enhance system security.

**Example:**
```bash
pwunconv --help
```

**Output (sample):**
```text
Usage/help information for `pwunconv` (illustrative; exact output varies by distribution/version).
```

### 172. `grpconv`
**संक्षिप्त जानकारी:** the grpconv command in Linux, learn how to create and manage user groups, and synchronize group passwords with practical examples.

**Example:**
```bash
grpconv --help
```

**Output (sample):**
```text
Usage/help information for `grpconv` (illustrative; exact output varies by distribution/version).
```

### 173. `grpunconv`
**संक्षिप्त जानकारी:** the grpunconv command in Linux, learn its purpose and syntax, and discover practical examples for removing groups from the system.

**Example:**
```bash
grpunconv --help
```

**Output (sample):**
```text
Usage/help information for `grpunconv` (illustrative; exact output varies by distribution/version).
```

### 174. `newaliases`
**संक्षिप्त जानकारी:** the newaliases command in Linux, learn how to create and manage email aliases, and troubleshoot alias configuration for effective email management.

**Example:**
```bash
newaliases --help
```

**Output (sample):**
```text
Usage/help information for `newaliases` (illustrative; exact output varies by distribution/version).
```

### 175. `users`
**संक्षिप्त जानकारी:** the Linux users command and learn how to manage user accounts, understand user privileges and permissions, and implement password policy and user management.

**Example:**
```bash
users --help
```

**Output (sample):**
```text
Usage/help information for `users` (illustrative; exact output varies by distribution/version).
```

---

<a id="cat-176-243"></a>
## 🌐 Networking and Communication

**Commands 176–243 (68 commands)**

### 176. `ping`
**संक्षिप्त जानकारी:** the ping command in Linux, learn how to use it for local and remote network troubleshooting, and gain practical experience with various ping command options.

**Example:**
```bash
ping -c 4 8.8.8.8
```

**Output (sample):**
```text
4 packets transmitted, 4 received, 0% packet loss
```

### 177. `netstat`
**संक्षिप्त जानकारी:** the netstat command, a powerful network troubleshooting tool. Learn how to analyze network connections, statistics, and diagnose network issues on Linux systems.

**Example:**
```bash
ss -tuln  # modern replacement for netstat
```

**Output (sample):**
```text
LISTEN ... :22 ...
```

### 178. `ifconfig`
**संक्षिप्त जानकारी:** the ifconfig command in Linux, learn its syntax and options, and discover practical examples to configure network interfaces.

**Example:**
```bash
ip addr  # modern replacement for ifconfig
```

**Output (sample):**
```text
1: lo ...
2: eth0 ...
```

### 179. `ssh`
**संक्षिप्त जानकारी:** how to use the SSH command to securely connect to remote Linux servers, transfer files, and more. Explore practical examples and master the essential skills for remote system administration.

**Example:**
```bash
ssh user@server.example.com
```

**Output (sample):**
```text
user@server.example.com's password:
```

### 180. `scp`
**संक्षिप्त जानकारी:** how to use the scp command to securely copy files and directories between local and remote hosts in Linux. Explore practical examples and understand the command's key features.

**Example:**
```bash
scp file.txt user@server:/tmp/
```

**Output (sample):**
```text
file.txt 100% 12B ...
```

### 181. `ftp`
**संक्षिप्त जानकारी:** the Linux ftp command with practical examples, including connecting to an FTP server, transferring files and directories, and understanding the basics of File Transfer Protocol.

**Example:**
```bash
ftp ftp.example.com
```

**Output (sample):**
```text
Connected to ftp.example.com.
```

### 182. `wget`
**संक्षिप्त जानकारी:** how to use the powerful wget command to download files from the internet. Explore practical examples and automate file downloads with wget scripting.

**Example:**
```bash
wget https://example.com/file.txt
```

**Output (sample):**
```text
Saving to: 'file.txt'
file.txt 100%
```

### 183. `curl`
**संक्षिप्त जानकारी:** the versatile curl command in Linux, learn how to fetch web page content, download files, and more through practical examples.

**Example:**
```bash
curl -I https://example.com
```

**Output (sample):**
```text
HTTP/2 200
content-type: text/html
```

### 184. `traceroute`
**संक्षिप्त जानकारी:** the traceroute command in Linux, learn how to trace the network path to a destination, and troubleshoot network issues using practical examples.

**Example:**
```bash
traceroute example.com
```

**Output (sample):**
```text
1  router (192.168.1.1) ...
2  ...
```

### 185. `telnet`
**संक्षिप्त जानकारी:** the telnet command in Linux, learn its purpose, syntax, and practical examples for troubleshooting network connectivity and remote server access.

**Example:**
```bash
telnet example.com 80
```

**Output (sample):**
```text
Connected to example.com.
```

### 186. `nslookup`
**संक्षिप्त जानकारी:** the nslookup command in Linux, learn how to perform basic DNS lookups, and troubleshoot DNS issues effectively.

**Example:**
```bash
nslookup example.com
```

**Output (sample):**
```text
Name: example.com
Address: 93.184.216.34
```

### 187. `dig`
**संक्षिप्त जानकारी:** the powerful dig command in Linux, learn its syntax, and practice various use cases for DNS lookups and advanced network troubleshooting.

**Example:**
```bash
dig example.com A +short
```

**Output (sample):**
```text
93.184.216.34
```

### 188. `route`
**संक्षिप्त जानकारी:** the Linux route command and learn how to configure static and dynamic routing using practical examples. Gain a deeper understanding of network routing and management.

**Example:**
```bash
ip route
```

**Output (sample):**
```text
default via 192.168.1.1 dev eth0
```

### 189. `ip`
**संक्षिप्त जानकारी:** the powerful ip command in Linux, learn to manage network interfaces, and troubleshoot network issues effectively.

**Example:**
```bash
ip addr show
```

**Output (sample):**
```text
1: lo: <LOOPBACK> ...
2: eth0: <BROADCAST,MULTICAST,UP> ...
```

### 190. `nmap`
**संक्षिप्त जानकारी:** the powerful nmap command in Linux, learn its basic usage, and discover advanced techniques for network scanning and security analysis.

**Example:**
```bash
nmap -sV 192.168.1.10
```

**Output (sample):**
```text
PORT   STATE SERVICE
22/tcp open  ssh
```

### 191. `ifup`
**संक्षिप्त जानकारी:** how to use the ifup command to configure and troubleshoot network interfaces on Linux. Understand the purpose, syntax, and practical examples of this essential networking tool.

**Example:**
```bash
ifup --help
```

**Output (sample):**
```text
Usage/help information for `ifup` (illustrative; exact output varies by distribution/version).
```

### 192. `ifdown`
**संक्षिप्त जानकारी:** the ifdown command in Linux, learn how to disable network interfaces, and troubleshoot network issues effectively.

**Example:**
```bash
ifdown --help
```

**Output (sample):**
```text
Usage/help information for `ifdown` (illustrative; exact output varies by distribution/version).
```

### 193. `hostname`
**संक्षिप्त जानकारी:** the Linux hostname command and learn how to change the hostname temporarily and permanently, with practical examples to enhance your system administration skills.

**Example:**
```bash
hostname
```

**Output (sample):**
```text
linux-server
```

### 194. `hostnamectl`
**संक्षिप्त जानकारी:** the Linux hostnamectl command and learn how to display system hostname information, change the hostname temporarily and permanently with practical examples.

**Example:**
```bash
hostnamectl
```

**Output (sample):**
```text
Static hostname: linux-server
Operating System: Ubuntu ...
```

### 195. `arp`
**संक्षिप्त जानकारी:** the arp command in Linux, learn its purpose, syntax, and how to manage the ARP cache through practical examples.

**Example:**
```bash
ip neigh
```

**Output (sample):**
```text
192.168.1.1 dev eth0 lladdr aa:bb:cc:dd:ee:ff REACHABLE
```

### 196. `netcat`
**संक्षिप्त जानकारी:** the versatile Linux netcat (nc) command and learn how to use it for server-client communication, file transfers, and other practical networking tasks.

**Example:**
```bash
nc -vz example.com 80
```

**Output (sample):**
```text
Connection to example.com 80 port [tcp/http] succeeded!
```

### 197. `nmcli`
**संक्षिप्त जानकारी:** the power of the nmcli command in managing network interfaces, troubleshooting connectivity issues, and gaining a deeper understanding of Linux networking.

**Example:**
```bash
nmcli device status
```

**Output (sample):**
```text
DEVICE  TYPE      STATE      CONNECTION
eth0    ethernet  connected  Wired connection
```

### 198. `tcpdump`
**संक्षिप्त जानकारी:** how to use the powerful tcpdump command to capture and analyze network traffic on Linux systems. Discover practical examples and techniques for filtering and monitoring network data.

**Example:**
```bash
sudo tcpdump -i eth0 -c 3
```

**Output (sample):**
```text
IP 192.168.1.2.12345 > 8.8.8.8.53: ...
```

### 199. `ss`
**संक्षिप्त जानकारी:** the Linux ss command, learn its syntax, and discover practical examples to analyze network connections, socket statistics, and states.

**Example:**
```bash
ss -tuln
```

**Output (sample):**
```text
Netid State  Local Address:Port
LISTEN ... :22
```

### 200. `iwconfig`
**संक्षिप्त जानकारी:** the Linux iwconfig command, a powerful tool for configuring and troubleshooting wireless network interfaces. Learn how to set up wireless connections, manage network parameters, and diagnose connectivity issues.

**Example:**
```bash
iwconfig --help
```

**Output (sample):**
```text
Usage/help information for `iwconfig` (illustrative; exact output varies by distribution/version).
```

### 201. `ethtool`
**संक्षिप्त जानकारी:** the ethtool command in Linux, a powerful tool for retrieving and modifying network interface settings. Learn how to use ethtool to diagnose and troubleshoot network issues.

**Example:**
```bash
sudo ethtool eth0
```

**Output (sample):**
```text
Speed: 1000Mb/s
Duplex: full
```

### 202. `smbclient`
**संक्षिप्त जानकारी:** the smbclient command in Linux, learn how to connect to Windows shares, list files and directories, and perform practical operations.

**Example:**
```bash
smbclient -L //server -U user
```

**Output (sample):**
```text
Sharename  Type  Comment
```

### 203. `smbstatus`
**संक्षिप्त जानकारी:** the Linux smbstatus command, learn its purpose, options, and how to analyze active SMB connections and shared resources on your system.

**Example:**
```bash
smbstatus --help
```

**Output (sample):**
```text
Usage/help information for `smbstatus` (illustrative; exact output varies by distribution/version).
```

### 204. `mailq`
**संक्षिप्त जानकारी:** the Linux mailq command, learn how to interpret its output, and manage the mail queue effectively. Gain practical knowledge for efficient email server administration.

**Example:**
```bash
mailq
```

**Output (sample):**
```text
Mail queue is empty
```

### 205. `host`
**संक्षिप्त जानकारी:** the hostname command, manage hostnames with hostnamectl, and customize the hostname on Ubuntu 22.04 in this practical Linux networking lab.

**Example:**
```bash
host example.com
```

**Output (sample):**
```text
example.com has address 93.184.216.34
```

### 206. `arpwatch`
**संक्षिप्त जानकारी:** the arpwatch command in Linux, learn how to install and use it to monitor network activity, and gain practical experience with real-world examples.

**Example:**
```bash
arpwatch --help
```

**Output (sample):**
```text
Usage/help information for `arpwatch` (illustrative; exact output varies by distribution/version).
```

### 207. `iftop`
**संक्षिप्त जानकारी:** the iftop command in Linux, a powerful network monitoring tool that provides real-time analysis of network traffic. Learn how to use iftop for effective bandwidth monitoring and troubleshooting.

**Example:**
```bash
sudo iftop -i eth0
```

**Output (sample):**
```text
Interactive bandwidth monitor opens.
```

### 208. `iptables`
**संक्षिप्त जानकारी:** the powerful iptables firewall tool in Linux. Learn to manage firewall rules, implement advanced configurations, and secure your network with practical examples.

**Example:**
```bash
sudo iptables -L
```

**Output (sample):**
```text
Chain INPUT (policy ACCEPT)
Chain FORWARD (policy ACCEPT)
```

### 209. `iptables-save`
**संक्षिप्त जानकारी:** the iptables-save command, which allows you to backup and restore iptables firewall rules. Learn how to use iptables-save for effective firewall management and automation.

**Example:**
```bash
iptables-save --help
```

**Output (sample):**
```text
Usage/help information for `iptables-save` (illustrative; exact output varies by distribution/version).
```

### 210. `tracepath`
**संक्षिप्त जानकारी:** the tracepath command in Linux, learn how to trace the path to a remote host, and troubleshoot network issues using practical examples.

**Example:**
```bash
tracepath example.com
```

**Output (sample):**
```text
1?: [LOCALHOST] pmtu 1500
2: ...
```

### 211. `uuname`
**संक्षिप्त जानकारी:** the Linux uuname command and learn how to retrieve system information, combine it with other commands, and apply practical examples to enhance your Linux administration skills.

**Example:**
```bash
uuname --help
```

**Output (sample):**
```text
Usage/help information for `uuname` (illustrative; exact output varies by distribution/version).
```

### 212. `vnstat`
**संक्षिप्त जानकारी:** the powerful Linux vnstat command for monitoring network traffic. Learn how to install, configure, and generate reports to visualize your network data.

**Example:**
```bash
vnstat --help
```

**Output (sample):**
```text
Usage/help information for `vnstat` (illustrative; exact output varies by distribution/version).
```

### 213. `whois`
**संक्षिप्त जानकारी:** the whois command in Linux, learn its syntax, and discover practical examples to retrieve domain information and customize the output.

**Example:**
```bash
whois example.com
```

**Output (sample):**
```text
Domain Name: EXAMPLE.COM
```

### 214. `apachectl`
**संक्षिप्त जानकारी:** how to use the apachectl command to manage the Apache web server, including starting, stopping, restarting, and checking the server status.

**Example:**
```bash
apachectl --help
```

**Output (sample):**
```text
Usage/help information for `apachectl` (illustrative; exact output varies by distribution/version).
```

### 215. `httpd`
**संक्षिप्त जानकारी:** the Linux httpd command with practical examples, including installing Apache HTTP Server, starting, stopping, and restarting the server, and configuring virtual hosts.

**Example:**
```bash
httpd --help
```

**Output (sample):**
```text
Usage/help information for `httpd` (illustrative; exact output varies by distribution/version).
```

### 216. `nc(netcat)`
**संक्षिप्त जानकारी:** the powerful nc (netcat) command in Linux, learn how to use it for TCP and UDP server-client communication, and discover practical examples to enhance your networking skills.

**Example:**
```bash
nc(netcat) --help
```

**Output (sample):**
```text
Usage/help information for `nc(netcat)` (illustrative; exact output varies by distribution/version).
```

### 217. `lpr`
**संक्षिप्त जानकारी:** how to use the lpr command in Linux to print text files and PDF documents. Explore practical examples and understand the command's functionality.

**Example:**
```bash
lpr --help
```

**Output (sample):**
```text
Usage/help information for `lpr` (illustrative; exact output varies by distribution/version).
```

### 218. `lpq`
**संक्षिप्त जानकारी:** the lpq command in Linux, learn how to check the print queue status, and manage print jobs effectively.

**Example:**
```bash
lpq --help
```

**Output (sample):**
```text
Usage/help information for `lpq` (illustrative; exact output varies by distribution/version).
```

### 219. `lprm`
**संक्षिप्त जानकारी:** the Linux lprm command for removing print jobs, including how to remove a specific job or all jobs. Learn practical examples to manage your print queue effectively.

**Example:**
```bash
lprm --help
```

**Output (sample):**
```text
Usage/help information for `lprm` (illustrative; exact output varies by distribution/version).
```

### 220. `lpd`
**संक्षिप्त जानकारी:** the lpd command, a powerful tool for managing print jobs in Linux. Learn how to configure the lpd daemon, control print queues, and troubleshoot printing issues with practical examples.

**Example:**
```bash
lpd --help
```

**Output (sample):**
```text
Usage/help information for `lpd` (illustrative; exact output varies by distribution/version).
```

### 221. `tftp`
**संक्षिप्त जानकारी:** the tftp command in Linux, learn how to configure a tftp server, and practice transferring files using the tftp client. Gain practical networking skills through hands-on examples.

**Example:**
```bash
tftp --help
```

**Output (sample):**
```text
Usage/help information for `tftp` (illustrative; exact output varies by distribution/version).
```

### 222. `ncftp`
**संक्षिप्त जानकारी:** how to use the ncftp command to connect to FTP servers, manage files and directories on the server, and perform various file transfer operations in a Linux environment.

**Example:**
```bash
ncftp --help
```

**Output (sample):**
```text
Usage/help information for `ncftp` (illustrative; exact output varies by distribution/version).
```

### 223. `ftpshut`
**संक्षिप्त जानकारी:** the ftpshut command in Linux, learn how to shut down the FTP server, and discover techniques for scheduling automatic FTP server shutdown.

**Example:**
```bash
ftpshut --help
```

**Output (sample):**
```text
Usage/help information for `ftpshut` (illustrative; exact output varies by distribution/version).
```

### 224. `ftpwho`
**संक्षिप्त जानकारी:** the ftpwho command in Linux, learn its options, and analyze its output to monitor FTP server connections and user activities.

**Example:**
```bash
ftpwho --help
```

**Output (sample):**
```text
Usage/help information for `ftpwho` (illustrative; exact output varies by distribution/version).
```

### 225. `ftpcount`
**संक्षिप्त जानकारी:** the ftpcount command in Linux, which allows you to monitor and count active FTP sessions on your system. Learn how to install, use, and interpret the output of this useful network utility.

**Example:**
```bash
ftpcount --help
```

**Output (sample):**
```text
Usage/help information for `ftpcount` (illustrative; exact output varies by distribution/version).
```

### 226. `uuto`
**संक्षिप्त जानकारी:** the uuto command in Linux, learn how to send and receive files securely, and discover practical use cases for this powerful communication tool.

**Example:**
```bash
uuto --help
```

**Output (sample):**
```text
Usage/help information for `uuto` (illustrative; exact output varies by distribution/version).
```

### 227. `uupick`
**संक्षिप्त जानकारी:** how to use the uupick command to extract files from UUENCODE encoded emails and automate the process with shell scripts. Gain practical networking and communication skills.

**Example:**
```bash
uupick --help
```

**Output (sample):**
```text
Usage/help information for `uupick` (illustrative; exact output varies by distribution/version).
```

### 228. `uucico`
**संक्षिप्त जानकारी:** the uucico command in Linux, learn how to configure it for file transfer, and execute remote connections and file transfers using practical examples.

**Example:**
```bash
uucico --help
```

**Output (sample):**
```text
Usage/help information for `uucico` (illustrative; exact output varies by distribution/version).
```

### 229. `uulog`
**संक्षिप्त जानकारी:** the Linux uulog command, learn its syntax, and discover practical examples for viewing, filtering, and searching system log entries.

**Example:**
```bash
uulog --help
```

**Output (sample):**
```text
Usage/help information for `uulog` (illustrative; exact output varies by distribution/version).
```

### 230. `dip`
**संक्षिप्त जानकारी:** the dip command in Linux, learn how to establish dial-up connections, and troubleshoot connectivity issues with practical examples.

**Example:**
```bash
dip --help
```

**Output (sample):**
```text
Usage/help information for `dip` (illustrative; exact output varies by distribution/version).
```

### 231. `minicom`
**संक्षिप्त जानकारी:** the Linux minicom command with practical examples. Learn how to install, configure, and use minicom to connect to serial devices, customize settings, and enhance your user experience.

**Example:**
```bash
minicom --help
```

**Output (sample):**
```text
Usage/help information for `minicom` (illustrative; exact output varies by distribution/version).
```

### 232. `mesg`
**संक्षिप्त जानकारी:** the Linux mesg command and learn how to send messages to terminal users, as well as restrict message receiving permissions. Gain practical knowledge for effective communication in a Linux environment.

**Example:**
```bash
mesg --help
```

**Output (sample):**
```text
Usage/help information for `mesg` (illustrative; exact output varies by distribution/version).
```

### 233. `wall`
**संक्षिप्त जानकारी:** the Linux wall command and its practical applications, including sending messages to all logged-in users and scheduling broadcast messages using cron.

**Example:**
```bash
wall --help
```

**Output (sample):**
```text
Usage/help information for `wall` (illustrative; exact output varies by distribution/version).
```

### 234. `write`
**संक्षिप्त जानकारी:** the Linux write command and its practical applications, including sending messages to specific users and broadcasting messages to all logged-in users on the same system.

**Example:**
```bash
write --help
```

**Output (sample):**
```text
Usage/help information for `write` (illustrative; exact output varies by distribution/version).
```

### 235. `talk`
**संक्षिप्त जानकारी:** the Linux talk command, learn how to send messages, and manage incoming requests. Gain practical networking and communication skills.

**Example:**
```bash
talk --help
```

**Output (sample):**
```text
Usage/help information for `talk` (illustrative; exact output varies by distribution/version).
```

### 236. `ytalk`
**संक्षिप्त जानकारी:** the Linux ytalk command, a tool for real-time text-based communication between users on the same system. Learn how to install, initiate, and utilize advanced features of ytalk for efficient collaboration and remote...

**Example:**
```bash
ytalk --help
```

**Output (sample):**
```text
Usage/help information for `ytalk` (illustrative; exact output varies by distribution/version).
```

### 237. `smbd`
**संक्षिप्त जानकारी:** the smbd command, a key component of the Samba server, and learn how to configure, manage, and secure Samba shares on your Linux system.

**Example:**
```bash
smbd --help
```

**Output (sample):**
```text
Usage/help information for `smbd` (illustrative; exact output varies by distribution/version).
```

### 238. `testparm`
**संक्षिप्त जानकारी:** the Linux testparm command, which verifies the syntax of Samba configuration files and analyzes Samba parameters. Learn practical examples to effectively manage and troubleshoot your Samba setup.

**Example:**
```bash
testparm --help
```

**Output (sample):**
```text
Usage/help information for `testparm` (illustrative; exact output varies by distribution/version).
```

### 239. `pppstats`
**संक्षिप्त जानकारी:** the pppstats command in Linux, learn how to monitor PPP interface statistics, and analyze PPP connection performance with practical examples.

**Example:**
```bash
pppstats --help
```

**Output (sample):**
```text
Usage/help information for `pppstats` (illustrative; exact output varies by distribution/version).
```

### 240. `cu`
**संक्षिप्त जानकारी:** the Linux cu command, a powerful tool for establishing remote connections and transferring files between systems. Learn practical examples and techniques to enhance your networking and communication skills.

**Example:**
```bash
cu --help
```

**Output (sample):**
```text
Usage/help information for `cu` (illustrative; exact output varies by distribution/version).
```

### 241. `getty`
**संक्षिप्त जानकारी:** the getty command, a crucial tool for managing virtual terminals in Linux. Learn its purpose, various options, and how to configure and manage virtual terminals effectively.

**Example:**
```bash
getty --help
```

**Output (sample):**
```text
Usage/help information for `getty` (illustrative; exact output varies by distribution/version).
```

### 242. `mingetty`
**संक्षिप्त जानकारी:** the Linux mingetty command and its practical applications, including automatic login configuration and customizing the login prompt. Enhance your Linux system management skills.

**Example:**
```bash
mingetty --help
```

**Output (sample):**
```text
Usage/help information for `mingetty` (illustrative; exact output varies by distribution/version).
```

### 243. `tty`
**संक्षिप्त जानकारी:** the Linux tty command and learn how to identify the current terminal device, manage terminal sessions, and apply practical examples to enhance your system administration skills.

**Example:**
```bash
tty --help
```

**Output (sample):**
```text
Usage/help information for `tty` (illustrative; exact output varies by distribution/version).
```

---

<a id="cat-244-286"></a>
## 💽 Disk and File System Utilities

**Commands 244–286 (43 commands)**

### 244. `mount`
**संक्षिप्त जानकारी:** the Linux mount command with practical examples. Learn how to mount local and remote file systems, including NFS, to effectively manage storage and access data on your Linux system.

**Example:**
```bash
mount | head -n 2
```

**Output (sample):**
```text
/dev/sda1 on / type ext4 (rw,relatime)
```

### 245. `umount`
**संक्षिप्त जानकारी:** the Linux umount command, learn how to unmount mounted file systems, and discover practical examples to manage your file system effectively.

**Example:**
```bash
sudo umount /mnt/usb
```

**Output (sample):**
```text
No output on success.
```

### 246. `fdisk`
**संक्षिप्त जानकारी:** how to use the fdisk command in Linux to create, delete, and resize partitions. Explore practical examples and understand the command's syntax and purpose.

**Example:**
```bash
sudo fdisk -l
```

**Output (sample):**
```text
Disk /dev/sda: 100 GiB
```

### 247. `mkfs`
**संक्षिप्त जानकारी:** the mkfs command in Linux, learn how to create file systems on partitions and format USB drives, and gain practical experience with hands-on examples.

**Example:**
```bash
sudo mkfs.ext4 /dev/sdb1
```

**Output (sample):**
```text
Creating filesystem with ...
Filesystem created.
```

### 248. `fsck`
**संक्षिप्त जानकारी:** the Linux fsck command, learn how to check filesystem integrity, and repair any issues using practical examples. Gain essential skills in disk and file system management.

**Example:**
```bash
sudo fsck -n /dev/sdb1
```

**Output (sample):**
```text
clean, ... files, ... blocks
```

### 249. `dd`
**संक्षिप्त जानकारी:** the powerful dd command in Linux, learn how to create backup images of USB drives, and restore them. Gain practical skills in disk and file system utilities.

**Example:**
```bash
dd if=/dev/zero of=test.img bs=1M count=10
```

**Output (sample):**
```text
10+0 records in
10+0 records out
```

### 250. `e2fsck`
**संक्षिप्त जानकारी:** the e2fsck command in Linux, learn how to check and repair corrupted Ext4 file systems, and perform dry runs to fix errors automatically.

**Example:**
```bash
sudo e2fsck -n /dev/sdb1
```

**Output (sample):**
```text
clean, ...
```

### 251. `tune2fs`
**संक्षिप्त जानकारी:** the tune2fs command, a powerful tool for managing ext2/ext3/ext4 file systems. Learn how to modify filesystem behavior, backup and restore metadata, and optimize disk performance.

**Example:**
```bash
sudo tune2fs -l /dev/sdb1 | head
```

**Output (sample):**
```text
tune2fs ...
Filesystem volume name ...
```

### 252. `hdparm`
**संक्षिप्त जानकारी:** the hdparm command in Linux, learn how to measure disk performance, and optimize disk configurations for improved system performance.

**Example:**
```bash
sudo hdparm -Tt /dev/sda
```

**Output (sample):**
```text
Timing cached reads: ... MB/sec
```

### 253. `fdformat`
**संक्षिप्त जानकारी:** the fdformat command in Linux, learn how to format a floppy disk, and troubleshoot any issues that may arise during the process.

**Example:**
```bash
fdformat --help
```

**Output (sample):**
```text
Usage/help information for `fdformat` (illustrative; exact output varies by distribution/version).
```

### 254. `parted`
**संक्षिप्त जानकारी:** the powerful parted command in Linux, learn to create, manage, resize, and delete partitions, and gain practical skills for disk and file system management.

**Example:**
```bash
sudo parted -l
```

**Output (sample):**
```text
Model: ...
Disk /dev/sda: 100GB
```

### 255. `blkid`
**संक्षिप्त जानकारी:** the blkid command in Linux, a powerful tool for identifying filesystem types and querying disk attributes. Learn practical examples to enhance your system management skills.

**Example:**
```bash
blkid /dev/sdb1
```

**Output (sample):**
```text
/dev/sdb1: UUID="..." TYPE="ext4"
```

### 256. `mkswap`
**संक्षिप्त जानकारी:** how to use the Linux mkswap command to create and manage swap files, which provide additional virtual memory for your system. Includes practical examples and step-by-step instructions.

**Example:**
```bash
sudo mkswap /swapfile
```

**Output (sample):**
```text
Setting up swapspace version 1 ...
```

### 257. `swapon`
**संक्षिप्त जानकारी:** how to effectively manage swap space in Linux using the swapon command. Explore practical examples for checking swap usage, creating, and enabling swap files.

**Example:**
```bash
swapon --show
```

**Output (sample):**
```text
NAME      TYPE SIZE USED PRIO
/swapfile file 2G 0B -2
```

### 258. `swapoff`
**संक्षिप्त जानकारी:** how to disable swap partitions and swap files using the swapoff command in Linux. Understand the purpose of swapoff and explore practical examples to manage swap space effectively.

**Example:**
```bash
sudo swapoff /swapfile
```

**Output (sample):**
```text
No output on success.
```

### 259. `losetup`
**संक्षिप्त जानकारी:** the Linux losetup command with practical examples. Learn how to create, attach, and detach loopback devices, a useful tool for working with disk images and file systems.

**Example:**
```bash
sudo losetup -a
```

**Output (sample):**
```text
/dev/loop0: []: (/path/disk.img)
```

### 260. `mkisofs`
**संक्षिप्त जानकारी:** the mkisofs command, a powerful tool for creating ISO images on Linux. Learn how to create basic ISO images, customize them with directories and files, and gain practical experience through hands-on examples.

**Example:**
```bash
mkisofs --help
```

**Output (sample):**
```text
Usage/help information for `mkisofs` (illustrative; exact output varies by distribution/version).
```

### 261. `eject`
**संक्षिप्त जानकारी:** the Linux eject command and learn how to use it to eject removable media devices and CD/DVD drives with practical examples.

**Example:**
```bash
eject /dev/cdrom
```

**Output (sample):**
```text
No output on success.
```

### 262. `lndir`
**संक्षिप्त जानकारी:** the lndir command in Linux, learn how to create symbolic links, and manage them effectively. Discover practical examples to enhance your file system management skills.

**Example:**
```bash
lndir --help
```

**Output (sample):**
```text
Usage/help information for `lndir` (illustrative; exact output varies by distribution/version).
```

### 263. `mdadm`
**संक्षिप्त जानकारी:** the power of the Linux mdadm command with this practical lab. Learn to create, manage, and monitor software RAID arrays, enhancing your system's storage and reliability.

**Example:**
```bash
sudo mdadm --detail --scan
```

**Output (sample):**
```text
ARRAY /dev/md0 metadata=1.2 name=...
```

### 264. `dumpe2fs`
**संक्षिप्त जानकारी:** the Linux dumpe2fs command, which provides detailed information about an Ext2/Ext3/Ext4 filesystem. Learn how to retrieve metadata, analyze statistics, and gain a deeper understanding of your file system.

**Example:**
```bash
dumpe2fs --help
```

**Output (sample):**
```text
Usage/help information for `dumpe2fs` (illustrative; exact output varies by distribution/version).
```

### 265. `sync`
**संक्षिप्त जानकारी:** the sync command in Linux, learn how to synchronize file system data, and verify the effectiveness of the sync command through practical examples.

**Example:**
```bash
sync
```

**Output (sample):**
```text
No output on success.
```

### 266. `badblocks`
**संक्षिप्त जानकारी:** the badblocks command in Linux, learn how to scan disks for bad blocks, and discover techniques to repair damaged areas on your storage devices.

**Example:**
```bash
sudo badblocks -nsv /dev/sdb
```

**Output (sample):**
```text
Checking blocks ...
Pass completed, 0 bad blocks found.
```

### 267. `mlabel`
**संक्षिप्त जानकारी:** the mlabel command in Linux, learn how to create and manage volume labels, and discover advanced options for disk and file system management.

**Example:**
```bash
mlabel --help
```

**Output (sample):**
```text
Usage/help information for `mlabel` (illustrative; exact output varies by distribution/version).
```

### 268. `mformat`
**संक्षिप्त जानकारी:** the mformat command in Linux, learn how to create and format floppy disks, and discover advanced options for various use cases.

**Example:**
```bash
mformat --help
```

**Output (sample):**
```text
Usage/help information for `mformat` (illustrative; exact output varies by distribution/version).
```

### 269. `mpartition`
**संक्षिप्त जानकारी:** how to use the mpartition command to create, resize, and delete partitions on Linux systems. Explore practical examples and understand the syntax and purpose of this essential disk management tool.

**Example:**
```bash
mpartition --help
```

**Output (sample):**
```text
Usage/help information for `mpartition` (illustrative; exact output varies by distribution/version).
```

### 270. `mdeltree`
**संक्षिप्त जानकारी:** the mdeltree command in Linux, a powerful tool for recursively removing directories and handling symbolic links and permissions. Gain practical experience through step-by-step examples.

**Example:**
```bash
mdeltree --help
```

**Output (sample):**
```text
Usage/help information for `mdeltree` (illustrative; exact output varies by distribution/version).
```

### 271. `mdu`
**संक्षिप्त जानकारी:** the mdu command in Linux, learn to measure disk usage, and exclude specific files and directories from the analysis.

**Example:**
```bash
mdu --help
```

**Output (sample):**
```text
Usage/help information for `mdu` (illustrative; exact output varies by distribution/version).
```

### 272. `mcd`
**संक्षिप्त जानकारी:** the mcd command in Linux, which allows you to create nested directories efficiently. Learn practical examples and how to combine mcd with other Linux commands for effective file management.

**Example:**
```bash
mcd --help
```

**Output (sample):**
```text
Usage/help information for `mcd` (illustrative; exact output varies by distribution/version).
```

### 273. `mmount`
**संक्षिप्त जानकारी:** the Linux mmount command, its syntax, and practical examples of mounting file systems. Learn how to effectively manage disk and file system utilities on your Linux system.

**Example:**
```bash
mmount --help
```

**Output (sample):**
```text
Usage/help information for `mmount` (illustrative; exact output varies by distribution/version).
```

### 274. `mbadblocks`
**संक्षिप्त जानकारी:** how to use the Linux mbadblocks command to identify, repair, and manage bad blocks on your file system. Gain practical experience with real-world examples.

**Example:**
```bash
mbadblocks --help
```

**Output (sample):**
```text
Usage/help information for `mbadblocks` (illustrative; exact output varies by distribution/version).
```

### 275. `fsck.minix`
**संक्षिप्त जानकारी:** the Linux fsck.minix command, learn how to check and repair Minix file systems, and discover practical examples of its usage.

**Example:**
```bash
fsck.minix --help
```

**Output (sample):**
```text
Usage/help information for `fsck.minix` (illustrative; exact output varies by distribution/version).
```

### 276. `mke2fs`
**संक्षिप्त जानकारी:** the mke2fs command in Linux, learn how to create Ext4 filesystems, and customize filesystem parameters for your storage needs.

**Example:**
```bash
sudo mke2fs -t ext4 /dev/sdb1
```

**Output (sample):**
```text
Creating filesystem with ...
```

### 277. `mkfs.ext2`
**संक्षिप्त जानकारी:** the mkfs.ext2 command, which is used to create an ext2 file system on a partition. Learn how to format an ext2 file system with custom parameters for your specific needs.

**Example:**
```bash
sudo mkfs.ext2 /dev/sdb1
```

**Output (sample):**
```text
Creating filesystem with ...
```

### 278. `mkfs.minix`
**संक्षिप्त जानकारी:** the Linux mkfs.minix command and learn how to create, mount, and interact with Minix file systems. This lab provides practical examples to help you manage disk and file system utilities.

**Example:**
```bash
mkfs.minix --help
```

**Output (sample):**
```text
Usage/help information for `mkfs.minix` (illustrative; exact options vary by distribution).
```

### 279. `mkfs.msdos`
**संक्षिप्त जानकारी:** the Linux mkfs.msdos command, learn how to create FAT32 file systems, and customize file system parameters for your storage needs.

**Example:**
```bash
sudo mkfs.msdos /dev/sdb1
```

**Output (sample):**
```text
mkfs.fat ...
```

### 280. `mkdosfs`
**संक्षिप्त जानकारी:** how to use the mkdosfs command to create a DOS filesystem on a partition or format a USB drive. This lab covers the basics of the mkdosfs command and provides practical examples.

**Example:**
```bash
sudo mkdosfs /dev/sdb1
```

**Output (sample):**
```text
mkfs.fat ...
```

### 281. `mkbootdisk`
**संक्षिप्त जानकारी:** how to use the mkbootdisk command to create a bootable USB drive for Linux systems. Explore practical examples and troubleshoot issues with the bootable USB drive.

**Example:**
```bash
mkbootdisk --help
```

**Output (sample):**
```text
Usage/help information for `mkbootdisk` (illustrative; exact output varies by distribution/version).
```

### 282. `mkinitrd`
**संक्षिप्त जानकारी:** the mkinitrd command in Linux, learn to create custom initramfs images, and troubleshoot kernel boot issues using practical examples.

**Example:**
```bash
mkinitrd --help
```

**Output (sample):**
```text
Usage/help information for `mkinitrd` (illustrative; exact output varies by distribution/version).
```

### 283. `sfdisk`
**संक्षिप्त जानकारी:** the sfdisk command in Linux, learn how to partition disks, and backup/restore partition tables with practical examples.

**Example:**
```bash
sfdisk --help
```

**Output (sample):**
```text
Usage/help information for `sfdisk` (illustrative; exact output varies by distribution/version).
```

### 284. `fsck.ext2`
**संक्षिप्त जानकारी:** the fsck.ext2 command in Linux, learn how to check and repair ext2 file systems, and perform forced file system checks with practical examples.

**Example:**
```bash
fsck.ext2 --help
```

**Output (sample):**
```text
Usage/help information for `fsck.ext2` (illustrative; exact output varies by distribution/version).
```

### 285. `symlinks`
**संक्षिप्त जानकारी:** the power of symbolic links in Linux, learn how they differ from hard links, and discover practical use cases to enhance your file management skills.

**Example:**
```bash
symlinks --help
```

**Output (sample):**
```text
Usage/help information for `symlinks` (illustrative; exact output varies by distribution/version).
```

### 286. `cfdisk`
**संक्षिप्त जानकारी:** the cfdisk command in Linux, a powerful tool for partitioning and managing disk drives. Learn how to create, delete, and modify disk partitions effectively.

**Example:**
```bash
cfdisk --help
```

**Output (sample):**
```text
Usage/help information for `cfdisk` (illustrative; exact output varies by distribution/version).
```

---

<a id="cat-287-309"></a>
## 📦 Compression and Archiving

**Commands 287–309 (23 commands)**

### 287. `tar`
**संक्षिप्त जानकारी:** the tar command in Linux, learn to create and extract archives, and compress and decompress data with practical examples.

**Example:**
```bash
tar -czf backup.tar.gz project/
```

**Output (sample):**
```text
No output on success.
```

### 288. `gzip`
**संक्षिप्त जानकारी:** the gzip command in Linux, learn how to compress and decompress files, and discover advanced techniques for efficient data compression.

**Example:**
```bash
gzip notes.txt
```

**Output (sample):**
```text
No output; notes.txt.gz is created.
```

### 289. `gunzip`
**संक्षिप्त जानकारी:** the gunzip command in Linux, learn how to decompress gzipped files, and recursively decompress directories with practical examples.

**Example:**
```bash
gunzip notes.txt.gz
```

**Output (sample):**
```text
No output; notes.txt is restored.
```

### 290. `zip`
**संक्षिप्त जानकारी:** the versatile zip command in Linux, learn how to create and extract zip archives, and discover techniques for compressing and encrypting files.

**Example:**
```bash
zip backup.zip notes.txt
```

**Output (sample):**
```text
adding: notes.txt (stored 0%)
```

### 291. `unzip`
**संक्षिप्त जानकारी:** how to use the unzip command in Linux to extract files from compressed ZIP archives, including password- protected ones.

**Example:**
```bash
unzip backup.zip
```

**Output (sample):**
```text
Archive: backup.zip
 extracting: notes.txt
```

### 292. `bzip2`
**संक्षिप्त जानकारी:** the bzip2 compression utility in Linux, learn how to compress and decompress files, and discover advanced bzip2 options and techniques.

**Example:**
```bash
bzip2 notes.txt
```

**Output (sample):**
```text
No output; notes.txt.bz2 is created.
```

### 293. `bunzip2`
**संक्षिप्त जानकारी:** how to use the Linux bunzip2 command to extract and decompress compressed files. Explore practical examples and understand the command's syntax and purpose.

**Example:**
```bash
bunzip2 notes.txt.bz2
```

**Output (sample):**
```text
No output; notes.txt is restored.
```

### 294. `compress`
**संक्षिप्त जानकारी:** the Linux compress command, learn how to compress and decompress files, and discover advanced options for efficient data compression.

**Example:**
```bash
compress --help
```

**Output (sample):**
```text
Usage/help information for `compress` (illustrative; exact output varies by distribution/version).
```

### 295. `uncompress`
**संक्षिप्त जानकारी:** how to use the uncompress command in Linux to decompress Gzipped files. Understand the purpose of the command and troubleshoot compression and decompression issues.

**Example:**
```bash
uncompress --help
```

**Output (sample):**
```text
Usage/help information for `uncompress` (illustrative; exact output varies by distribution/version).
```

### 296. `cpio`
**संक्षिप्त जानकारी:** the cpio command in Linux, learn its syntax, and practice creating and extracting archives with practical examples.

**Example:**
```bash
find . -print | cpio -ov > archive.cpio
```

**Output (sample):**
```text
1 block
```

### 297. `ar`
**संक्षिप्त जानकारी:** the Linux ar command for creating, managing, and manipulating static libraries. Learn how to build, extract, and list the contents of static libraries through practical examples.

**Example:**
```bash
ar rcs libdemo.a demo.o
```

**Output (sample):**
```text
No output on success.
```

### 298. `rar`
**संक्षिप्त जानकारी:** the rar command in Linux with practical examples. Learn how to install the rar package, create and extract rar archives, and manage them with advanced options.

**Example:**
```bash
rar --help
```

**Output (sample):**
```text
Usage/help information for `rar` (illustrative; exact output varies by distribution/version).
```

### 299. `unrar`
**संक्षिप्त जानकारी:** the Linux unrar command and learn how to extract single and multi- part RAR archives on Ubuntu 22.04. Gain practical experience with this essential file compression and archiving tool.

**Example:**
```bash
unrar --help
```

**Output (sample):**
```text
Usage/help information for `unrar` (illustrative; exact output varies by distribution/version).
```

### 300. `zcat`
**संक्षिप्त जानकारी:** the versatile zcat command in Linux, which allows you to decompress and view gzipped files without extracting them. Learn practical examples and how to combine zcat with other commands.

**Example:**
```bash
zcat notes.txt.gz
```

**Output (sample):**
```text
Hello Linux
```

### 301. `zless`
**संक्षिप्त जानकारी:** the zless command in Linux, a powerful tool for viewing compressed files. Learn its syntax, options, and practical examples to enhance your compression and archiving skills.

**Example:**
```bash
zless --help
```

**Output (sample):**
```text
Usage/help information for `zless` (illustrative; exact output varies by distribution/version).
```

### 302. `zdiff`
**संक्षिप्त जानकारी:** the zdiff command in Linux, a powerful tool for comparing compressed files. Learn its syntax, practical examples, and troubleshooting techniques to effectively manage compressed data.

**Example:**
```bash
zdiff --help
```

**Output (sample):**
```text
Usage/help information for `zdiff` (illustrative; exact output varies by distribution/version).
```

### 303. `zgrep`
**संक्षिप्त जानकारी:** the zgrep command in Linux, learn how to decompress and search compressed files, and combine zgrep with other commands for efficient data processing.

**Example:**
```bash
zgrep --help
```

**Output (sample):**
```text
Usage/help information for `zgrep` (illustrative; exact output varies by distribution/version).
```

### 304. `zipinfo`
**संक्षिप्त जानकारी:** the powerful zipinfo command in Linux, learn its options, and analyze the contents of zip files with practical examples.

**Example:**
```bash
zipinfo --help
```

**Output (sample):**
```text
Usage/help information for `zipinfo` (illustrative; exact output varies by distribution/version).
```

### 305. `bzcat`
**संक्षिप्त जानकारी:** the bzcat command in Linux, a powerful tool for decompressing gzipped files. Learn how to use bzcat with practical examples and combine it with other Linux commands.

**Example:**
```bash
bzcat notes.txt.bz2
```

**Output (sample):**
```text
Hello Linux
```

### 306. `bzdiff`
**संक्षिप्त जानकारी:** the bzdiff command in Linux, which allows you to compare compressed files. Learn how to use bzdiff for effective file comparison and discover advanced options to enhance your workflow.

**Example:**
```bash
bzdiff --help
```

**Output (sample):**
```text
Usage/help information for `bzdiff` (illustrative; exact output varies by distribution/version).
```

### 307. `bzgrep`
**संक्षिप्त जानकारी:** how to use the bzgrep command to search for patterns in compressed files, and combine it with other Linux commands for advanced searches.

**Example:**
```bash
bzgrep --help
```

**Output (sample):**
```text
Usage/help information for `bzgrep` (illustrative; exact output varies by distribution/version).
```

### 308. `bzless`
**संक्षिप्त जानकारी:** the bzless command, a powerful tool for navigating compressed text files. Learn how to utilize bzless options to efficiently view and navigate bzip2-compressed content.

**Example:**
```bash
bzless --help
```

**Output (sample):**
```text
Usage/help information for `bzless` (illustrative; exact output varies by distribution/version).
```

### 309. `bzmore`
**संक्षिप्त जानकारी:** the bzmore command in Linux, a tool for viewing compressed text files. Learn its functionality and practical examples to enhance your compression and archiving skills.

**Example:**
```bash
bzmore --help
```

**Output (sample):**
```text
Usage/help information for `bzmore` (illustrative; exact output varies by distribution/version).
```

---

<a id="cat-310-333"></a>
## ⚙️ Process Management

**Commands 310–333 (24 commands)**

### 310. `kill`
**संक्षिप्त जानकारी:** the Linux kill command, learn how to terminate processes, and discover advanced options for managing processes effectively.

**Example:**
```bash
kill 1234
```

**Output (sample):**
```text
No output on success.
```

### 311. `pkill`
**संक्षिप्त जानकारी:** the pkill command in Linux, learn how to terminate processes by name or ID, and gain practical experience with real-world examples.

**Example:**
```bash
pkill firefox
```

**Output (sample):**
```text
No output on success.
```

### 312. `killall`
**संक्षिप्त जानकारी:** the Linux killall command, learn how to kill processes by name or user, and gain practical experience with real- world examples.

**Example:**
```bash
killall firefox
```

**Output (sample):**
```text
No output on success.
```

### 313. `nice`
**संक्षिप्त जानकारी:** the Linux nice command and learn how to adjust process priority for optimal system performance. Discover practical examples to enhance your process management skills.

**Example:**
```bash
nice -n 10 ./job.sh
```

**Output (sample):**
```text
Command runs with adjusted priority.
```

### 314. `renice`
**संक्षिप्त जानकारी:** the Linux renice command to adjust process priority, with practical examples showcasing its usage and benefits in process management.

**Example:**
```bash
renice 10 -p 1234
```

**Output (sample):**
```text
1234 (process ID) old priority 0, new priority 10
```

### 315. `jobs`
**संक्षिप्त जानकारी:** the Linux jobs command, learn to manage background processes, and discover practical examples to enhance your process management skills.

**Example:**
```bash
jobs
```

**Output (sample):**
```text
[1]+  Running  ./script.sh &
```

### 316. `fg`
**संक्षिप्त जानकारी:** the Linux fg command and learn how to bring background processes to the foreground, manage multiple background processes, and optimize your workflow with practical examples.

**Example:**
```bash
fg %1
```

**Output (sample):**
```text
./script.sh
```

### 317. `bg`
**संक्षिप्त जानकारी:** the Linux bg command, learn how to suspend and move foreground processes to the background, and manage background processes effectively.

**Example:**
```bash
bg %1
```

**Output (sample):**
```text
[1]+ ./script.sh &
```

### 318. `pgrep`
**संक्षिप्त जानकारी:** the pgrep command in Linux, a powerful tool for searching and monitoring processes by name. Learn practical examples to enhance your process management skills.

**Example:**
```bash
pgrep sshd
```

**Output (sample):**
```text
790
```

### 319. `nohup`
**संक्षिप्त जानकारी:** how to use the nohup command to run long-running processes in the background, even after you log out of your terminal. Explore practical examples and understand the purpose of this powerful Linux tool.

**Example:**
```bash
nohup ./backup.sh > backup.log 2>&1 &
```

**Output (sample):**
```text
nohup: ignoring input and appending output to 'nohup.out'
```

### 320. `disown`
**संक्षिप्त जानकारी:** the disown command in Linux, learn how to detach running processes from the shell, and manage their output effectively.

**Example:**
```bash
disown --help
```

**Output (sample):**
```text
Usage/help information for `disown` (illustrative; exact output varies by distribution/version).
```

### 321. `screen`
**संक्षिप्त जानकारी:** the powerful screen command in Linux, learn to create and manage multiple terminal sessions, and discover practical examples to boost your process management skills.

**Example:**
```bash
screen --help
```

**Output (sample):**
```text
Usage/help information for `screen` (illustrative; exact output varies by distribution/version).
```

### 322. `tmux`
**संक्षिप्त जानकारी:** the powerful tmux command-line tool for managing and controlling multiple terminal sessions on a Linux system. Learn how to navigate, manage, and customize tmux for enhanced productivity.

**Example:**
```bash
tmux new -s work
```

**Output (sample):**
```text
Interactive tmux session opens.
```

### 323. `strace`
**संक्षिप्त जानकारी:** the powerful strace command in Linux, learn how to trace system calls, and debug processes effectively with practical examples.

**Example:**
```bash
strace -e openat ls
```

**Output (sample):**
```text
openat(...)
...
```

### 324. `ltrace`
**संक्षिप्त जानकारी:** the ltrace command in Linux, which allows you to trace system calls and library calls, helping you identify potential issues and optimize application performance.

**Example:**
```bash
ltrace ls
```

**Output (sample):**
```text
libc calls ...
```

### 325. `skill`
**संक्षिप्त जानकारी:** the Linux skill command and its practical applications in process management. Learn to manage files, use redirection and pipes, and automate tasks with shell scripting.

**Example:**
```bash
skill --help
```

**Output (sample):**
```text
Usage/help information for `skill` (illustrative; exact output varies by distribution/version).
```

### 326. `psnice`
**संक्षिप्त जानकारी:** the psnice command in Linux, learn how to adjust process priority, and discover practical use cases for managing system processes efficiently.

**Example:**
```bash
psnice --help
```

**Output (sample):**
```text
Usage/help information for `psnice` (illustrative; exact output varies by distribution/version).
```

### 327. `at`
**संक्षिप्त जानकारी:** the Linux file system, manage files and directories, and understand permissions through practical examples.

**Example:**
```bash
at --help
```

**Output (sample):**
```text
Usage/help information for `at` (illustrative; exact output varies by distribution/version).
```

### 328. `batch`
**संक्षिप्त जानकारी:** the power of the Linux batch command through practical examples. Automate repetitive tasks, utilize conditional statements, and leverage loops to streamline your workflow.

**Example:**
```bash
batch --help
```

**Output (sample):**
```text
Usage/help information for `batch` (illustrative; exact output varies by distribution/version).
```

### 329. `atd`
**संक्षिप्त जानकारी:** the Linux atd command for scheduling one-time tasks, learn how to monitor and control scheduled tasks, and gain practical experience with real- world examples.

**Example:**
```bash
atd --help
```

**Output (sample):**
```text
Usage/help information for `atd` (illustrative; exact output varies by distribution/version).
```

### 330. `atq`
**संक्षिप्त जानकारी:** the atq command in Linux, which allows you to list and manage scheduled jobs. Learn how to view, remove, and work with cron jobs effectively.

**Example:**
```bash
atq --help
```

**Output (sample):**
```text
Usage/help information for `atq` (illustrative; exact output varies by distribution/version).
```

### 331. `atrm`
**संक्षिप्त जानकारी:** the atrm command in Linux, which allows you to remove scheduled tasks. Learn how to troubleshoot and manage your system's scheduled tasks effectively.

**Example:**
```bash
atrm --help
```

**Output (sample):**
```text
Usage/help information for `atrm` (illustrative; exact output varies by distribution/version).
```

### 332. `chrt`
**संक्षिप्त जानकारी:** the Linux chrt command, which allows you to adjust the real-time priority and scheduling policies of processes, with practical examples to enhance your process management skills.

**Example:**
```bash
chrt --help
```

**Output (sample):**
```text
Usage/help information for `chrt` (illustrative; exact output varies by distribution/version).
```

### 333. `setsid`
**संक्षिप्त जानकारी:** the setsid command in Linux, learn how to detach processes from the current session, and run background processes effectively.

**Example:**
```bash
setsid --help
```

**Output (sample):**
```text
Usage/help information for `setsid` (illustrative; exact output varies by distribution/version).
```

---

<a id="cat-334-491"></a>
## 🛠️ System Configuration and Settings

**Commands 334–491 (158 commands)**

### 334. `crontab`
**संक्षिप्त जानकारी:** the Linux crontab command and learn how to schedule recurring tasks. Discover practical examples to enhance your system management skills.

**Example:**
```bash
crontab -l
```

**Output (sample):**
```text
0 2 * * * /home/user/backup.sh
```

### 335. `systemctl`
**संक्षिप्त जानकारी:** the systemctl command, a powerful tool for managing system services in Linux. Learn how to start, stop, enable, and disable services, as well as configure automatic service startup.

**Example:**
```bash
systemctl status ssh
```

**Output (sample):**
```text
● ssh.service - OpenBSD Secure Shell server
   Active: active (running)
```

### 336. `service`
**संक्षिप्त जानकारी:** the Linux service command, learn how to manage system services, and troubleshoot service issues with practical examples.

**Example:**
```bash
sudo service ssh status
```

**Output (sample):**
```text
● ssh.service - OpenBSD Secure Shell server
   Active: active (running)
```

### 337. `chkconfig`
**संक्षिप्त जानकारी:** the chkconfig command in Linux, learn how to configure service startup behavior, and manage service startup levels with practical examples.

**Example:**
```bash
chkconfig --help
```

**Output (sample):**
```text
Usage/help information for `chkconfig` (illustrative; exact output varies by distribution/version).
```

### 338. `update-rc.d`
**संक्षिप्त जानकारी:** how to use the update-rc.d command to configure services to start automatically at boot, manage service startup priorities, and gain practical experience with real-world examples.

**Example:**
```bash
update-rc.d --help
```

**Output (sample):**
```text
Usage/help information for `update-rc.d` (illustrative; exact output varies by distribution/version).
```

### 339. `timedatectl`
**संक्षिप्त जानकारी:** the timedatectl command in Linux, learn how to manage system date and time, configure time zone and NTP settings, and gain practical experience through hands-on examples.

**Example:**
```bash
timedatectl
```

**Output (sample):**
```text
Local time: Fri 2026-08-21 ...
Time zone: Asia/Kathmandu
```

### 340. `locale`
**संक्षिप्त जानकारी:** the Linux locale command and its practical applications. Learn how to understand locales, examine available locales, and change the system locale to observe its impact.

**Example:**
```bash
locale
```

**Output (sample):**
```text
LANG=en_US.UTF-8
LC_TIME=en_US.UTF-8
```

### 341. `localectl`
**संक्षिप्त जानकारी:** the localectl command in Linux, which allows you to manage system locale settings, customize keyboard layouts, and configure keymaps effectively.

**Example:**
```bash
localectl status
```

**Output (sample):**
```text
System Locale: LANG=en_US.UTF-8
```

### 342. `ulimit`
**संक्षिप्त जानकारी:** the ulimit command in Linux, learn to adjust resource limits for processes, and discover practical examples to optimize system performance.

**Example:**
```bash
ulimit -a | head -n 3
```

**Output (sample):**
```text
core file size 0
max locked memory ...
```

### 343. `alias`
**संक्षिप्त जानकारी:** the power of the Linux alias command and learn how to create, manage, and persist custom command shortcuts for improved productivity and efficiency.

**Example:**
```bash
alias ll='ls -la'; ll
```

**Output (sample):**
```text
total ...
```

### 344. `unalias`
**संक्षिप्त जानकारी:** how to use the unalias command in Linux to temporarily disable aliases and manage them effectively in the terminal.

**Example:**
```bash
unalias ll
```

**Output (sample):**
```text
No output on success.
```

### 345. `export`
**संक्षिप्त जानकारी:** the power of the Linux export command with practical examples. Learn how to set environment variables, understand its purpose, and apply it effectively in your system configuration and settings.

**Example:**
```bash
export APP_ENV=production; echo $APP_ENV
```

**Output (sample):**
```text
production
```

### 346. `set`
**संक्षिप्त जानकारी:** the Linux set command, learn how to modify shell variables, manage environment variables, and apply practical examples to enhance your system configuration and settings.

**Example:**
```bash
set | head -n 2
```

**Output (sample):**
```text
BASH=/usr/bin/bash
BASH_VERSION=...
```

### 347. `unset`
**संक्षिप्त जानकारी:** the unset command in Linux, learn how to unset environment variables and shell functions, and apply practical examples to enhance your system configuration and settings.

**Example:**
```bash
unset APP_ENV
```

**Output (sample):**
```text
No output on success.
```

### 348. `env`
**संक्षिप्त जानकारी:** the env command in Linux, learn how to modify environment variables, and execute commands with custom environments for improved system configuration and settings.

**Example:**
```bash
env | grep APP_ENV
```

**Output (sample):**
```text
APP_ENV=production
```

### 349. `sysctl`
**संक्षिप्त जानकारी:** the sysctl command in Linux, learn how to modify kernel parameters, and persist configuration changes across reboots. Gain practical knowledge for system administration and optimization.

**Example:**
```bash
sysctl net.ipv4.ip_forward
```

**Output (sample):**
```text
net.ipv4.ip_forward = 0
```

### 350. `modprobe`
**संक्षिप्त जानकारी:** how to use the modprobe command to load and remove kernel modules in Linux, with practical examples to enhance your system configuration and settings.

**Example:**
```bash
sudo modprobe loop
```

**Output (sample):**
```text
No output on success.
```

### 351. `lsmod`
**संक्षिप्त जानकारी:** the Linux lsmod command, which displays information about loaded kernel modules. Learn how to load and unload kernel modules, and understand the purpose and output of the lsmod command.

**Example:**
```bash
lsmod | head
```

**Output (sample):**
```text
Module  Size  Used by
loop ...
```

### 352. `insmod`
**संक्षिप्त जानकारी:** the insmod command in Linux, learn how to compile and insert kernel modules, and gain practical experience with real-world examples.

**Example:**
```bash
insmod --help
```

**Output (sample):**
```text
Usage/help information for `insmod` (illustrative; exact options vary by distribution).
```

### 353. `rmmod`
**संक्षिप्त जानकारी:** the Linux rmmod command and learn how to remove kernel modules effectively. Discover practical scenarios and examples to enhance your system configuration and settings.

**Example:**
```bash
rmmod --help
```

**Output (sample):**
```text
Usage/help information for `rmmod` (illustrative; exact options vary by distribution).
```

### 354. `depmod`
**संक्षिप्त जानकारी:** the purpose of the depmod command, understand the dependency tree of kernel modules, and troubleshoot module dependencies using practical examples.

**Example:**
```bash
depmod --help
```

**Output (sample):**
```text
Usage/help information for `depmod` (illustrative; exact output varies by distribution/version).
```

### 355. `lspci`
**संक्षिप्त जानकारी:** the lspci command in Linux, learn its purpose, understand its options and flags, and identify PCI devices on your system with practical examples.

**Example:**
```bash
lspci | head -n 2
```

**Output (sample):**
```text
00:00.0 Host bridge: ...
00:02.0 VGA compatible controller: ...
```

### 356. `hwclock`
**संक्षिप्त जानकारी:** the Linux hwclock command, learn how to synchronize system time with hardware clock, and adjust the hardware clock manually for effective system time management.

**Example:**
```bash
sudo hwclock --show
```

**Output (sample):**
```text
2026-08-21 11:57:00.123456+05:45
```

### 357. `setserial`
**संक्षिप्त जानकारी:** the Linux setserial command and learn how to configure serial port settings, identify port information, and troubleshoot serial communication issues.

**Example:**
```bash
setserial --help
```

**Output (sample):**
```text
Usage/help information for `setserial` (illustrative; exact output varies by distribution/version).
```

### 358. `edquota`
**संक्षिप्त जानकारी:** the Linux edquota command and learn how to manage user disk quotas, enable disk quota on a filesystem, and understand the concept of disk quota.

**Example:**
```bash
edquota --help
```

**Output (sample):**
```text
Usage/help information for `edquota` (illustrative; exact output varies by distribution/version).
```

### 359. `quota`
**संक्षिप्त जानकारी:** the Linux quota command and learn how to set, monitor, and manage disk quota usage for users on your system. Gain practical knowledge for effective storage management.

**Example:**
```bash
quota --help
```

**Output (sample):**
```text
Usage/help information for `quota` (illustrative; exact output varies by distribution/version).
```

### 360. `quotaon`
**संक्षिप्त जानकारी:** the Linux quotaon command for managing disk quotas. Learn how to enable, monitor, and manage user disk quotas on your file system.

**Example:**
```bash
quotaon --help
```

**Output (sample):**
```text
Usage/help information for `quotaon` (illustrative; exact output varies by distribution/version).
```

### 361. `quotaoff`
**संक्षिप्त जानकारी:** how to disable disk quotas on a Linux file system using the quotaoff command. Understand the basics of disk quotas and their practical applications.

**Example:**
```bash
quotaoff --help
```

**Output (sample):**
```text
Usage/help information for `quotaoff` (illustrative; exact output varies by distribution/version).
```

### 362. `quotacheck`
**संक्षिप्त जानकारी:** the Linux quotacheck command with practical examples. Learn how to install the quota package, enable quota on a filesystem, and use the quotacheck command to check quota information.

**Example:**
```bash
quotacheck --help
```

**Output (sample):**
```text
Usage/help information for `quotacheck` (illustrative; exact output varies by distribution/version).
```

### 363. `repquota`
**संक्षिप्त जानकारी:** the repquota command in Linux, learn how to retrieve disk quota information for users, and manage disk quota limits for multiple users.

**Example:**
```bash
repquota --help
```

**Output (sample):**
```text
Usage/help information for `repquota` (illustrative; exact output varies by distribution/version).
```

### 364. `chroot`
**संक्षिप्त जानकारी:** the chroot command in Linux, learn how to create a chroot environment, and manage processes and file systems within the isolated environment.

**Example:**
```bash
chroot --help
```

**Output (sample):**
```text
Usage/help information for `chroot` (illustrative; exact output varies by distribution/version).
```

### 365. `dircolors`
**संक्षिप्त जानकारी:** the Linux dircolors command and learn how to customize directory and file colors, manage configuration files, and enhance your command-line experience.

**Example:**
```bash
dircolors --help
```

**Output (sample):**
```text
Usage/help information for `dircolors` (illustrative; exact output varies by distribution/version).
```

### 366. `loadkeys`
**संक्षिप्त जानकारी:** the Linux loadkeys command and learn how to change and customize your keyboard layout. Discover practical examples to enhance your system configuration and settings.

**Example:**
```bash
loadkeys --help
```

**Output (sample):**
```text
Usage/help information for `loadkeys` (illustrative; exact output varies by distribution/version).
```

### 367. `modinfo`
**संक्षिप्त जानकारी:** the Linux modinfo command, which provides detailed information about kernel modules. Learn how to use modinfo to troubleshoot module issues and optimize system configuration.

**Example:**
```bash
modinfo --help
```

**Output (sample):**
```text
Usage/help information for `modinfo` (illustrative; exact output varies by distribution/version).
```

### 368. `setleds`
**संक्षिप्त जानकारी:** how to use the setleds command to modify keyboard LED states, and automate LED state changes with shell scripts for efficient system configuration.

**Example:**
```bash
setleds --help
```

**Output (sample):**
```text
Usage/help information for `setleds` (illustrative; exact output varies by distribution/version).
```

### 369. `showkey`
**संक्षिप्त जानकारी:** the Linux showkey command, learn how to capture keyboard input, and analyze the output for system configuration and settings.

**Example:**
```bash
showkey --help
```

**Output (sample):**
```text
Usage/help information for `showkey` (illustrative; exact output varies by distribution/version).
```

### 370. `stty`
**संक्षिप्त जानकारी:** the stty command in Linux, learn how to modify terminal settings, and discover practical examples to enhance your system configuration skills.

**Example:**
```bash
stty --help
```

**Output (sample):**
```text
Usage/help information for `stty` (illustrative; exact output varies by distribution/version).
```

### 371. `zdump`
**संक्षिप्त जानकारी:** the Linux zdump command, which displays time zone information. Learn its syntax, understand timezone data, and see practical examples of its usage.

**Example:**
```bash
zdump --help
```

**Output (sample):**
```text
Usage/help information for `zdump` (illustrative; exact output varies by distribution/version).
```

### 372. `cron`
**संक्षिप्त जानकारी:** the powerful cron service in Linux, learn how to schedule and manage cron jobs, and configure notifications and logging for effective system maintenance.

**Example:**
```bash
cron --help
```

**Output (sample):**
```text
Usage/help information for `cron` (illustrative; exact output varies by distribution/version).
```

### 373. `aumix`
**संक्षिप्त जानकारी:** how to use the aumix command to adjust audio settings on your Ubuntu 22.04 system, including controlling master volume, muting and unmuting audio channels.

**Example:**
```bash
aumix --help
```

**Output (sample):**
```text
Usage/help information for `aumix` (illustrative; exact output varies by distribution/version).
```

### 374. `clock`
**संक्षिप्त जानकारी:** the Linux clock command and learn how to display the current date and time, as well as set the system clock using practical examples.

**Example:**
```bash
clock --help
```

**Output (sample):**
```text
Usage/help information for `clock` (illustrative; exact output varies by distribution/version).
```

### 375. `lilo`
**संक्षिप्त जानकारी:** the lilo command, a powerful Linux boot loader, through practical examples. Learn how to configure lilo, troubleshoot issues, and enhance your system's boot process.

**Example:**
```bash
lilo --help
```

**Output (sample):**
```text
Usage/help information for `lilo` (illustrative; exact output varies by distribution/version).
```

### 376. `ntsysv`
**संक्षिप्त जानकारी:** the ntsysv command in Linux, a powerful tool for configuring and managing system services. Learn how to use ntsysv to control runlevels and enable/disable services for efficient system administration.

**Example:**
```bash
ntsysv --help
```

**Output (sample):**
```text
Usage/help information for `ntsysv` (illustrative; exact output varies by distribution/version).
```

### 377. `rdate`
**संक्षिप्त जानकारी:** the Linux rdate command and learn how to synchronize your system time with remote NTP servers. Automate time synchronization using cron for reliable and consistent timekeeping.

**Example:**
```bash
rdate --help
```

**Output (sample):**
```text
Usage/help information for `rdate` (illustrative; exact output varies by distribution/version).
```

### 378. `resize`
**संक्षिप्त जानकारी:** how to resize partitions and LVM volumes using the Linux resize command. Explore practical examples and step-by- step instructions to effectively manage storage space on your Linux system.

**Example:**
```bash
resize --help
```

**Output (sample):**
```text
Usage/help information for `resize` (illustrative; exact output varies by distribution/version).
```

### 379. `sndconfig`
**संक्षिप्त जानकारी:** the sndconfig command in Linux, learn how to configure sound card settings, and troubleshoot sound issues effectively.

**Example:**
```bash
sndconfig --help
```

**Output (sample):**
```text
Usage/help information for `sndconfig` (illustrative; exact output varies by distribution/version).
```

### 380. `setconsole`
**संक्षिप्त जानकारी:** the setconsole command in Linux, which allows you to modify the system console device and redirect console output to a file. Learn how to effectively manage your Linux system's console settings.

**Example:**
```bash
setconsole --help
```

**Output (sample):**
```text
Usage/help information for `setconsole` (illustrative; exact output varies by distribution/version).
```

### 381. `apmd`
**संक्षिप्त जानकारी:** the Linux apmd command and learn how to monitor battery status, configure automated power management, and optimize your system's power efficiency.

**Example:**
```bash
apmd --help
```

**Output (sample):**
```text
Usage/help information for `apmd` (illustrative; exact output varies by distribution/version).
```

### 382. `fbset`
**संक्षिप्त जानकारी:** the fbset command in Linux, learn how to adjust screen resolution and depth, and customize display settings for optimal performance. Package Management

**Example:**
```bash
fbset --help
```

**Output (sample):**
```text
Usage/help information for `fbset` (illustrative; exact output varies by distribution/version).
```

### 383. `rpm`
**संक्षिप्त जानकारी:** the powerful rpm command in Linux, learn how to install, manage, query, and verify RPM packages, and gain practical experience through hands-on examples.

**Example:**
```bash
rpm --help
```

**Output (sample):**
```text
Usage/help information for `rpm` (illustrative; exact output varies by distribution/version).
```

### 384. `apt-get`
**संक्षिप्त जानकारी:** how to effectively use the apt-get command in Linux for package management, including installing, updating, removing, and cleaning up packages.

**Example:**
```bash
sudo apt-get update
```

**Output (sample):**
```text
Reading package lists... Done
```

### 385. `dpkg`
**संक्षिप्त जानकारी:** the dpkg command in Linux, learn to install and manage packages, and troubleshoot package installation issues. Gain practical experience in package management using this essential Linux tool.

**Example:**
```bash
dpkg -l | head -n 3
```

**Output (sample):**
```text
Desired=Unknown/Install/Remove/Purge
|| Status=Not/Inst/Conf-files...
```

### 386. `yum`
**संक्षिप्त जानकारी:** the powerful yum package manager in Linux. Learn how to install, update, and remove packages using practical examples. Enhance your system management skills with this comprehensive lab.

**Example:**
```bash
yum --help
```

**Output (sample):**
```text
Usage/help information for `yum` (illustrative; exact output varies by distribution/version).
```

### 387. `apt`
**संक्षिप्त जानकारी:** the apt command in Linux, learn how to install, update, search, and remove packages using practical examples.

**Example:**
```bash
sudo apt update
```

**Output (sample):**
```text
Hit:1 http://archive.ubuntu.com/ubuntu ...
Reading package lists... Done
```

### 388. `aptitude`
**संक्षिप्त जानकारी:** the aptitude package manager in Linux, learn how to search, install, upgrade, and remove packages, and gain practical experience with real-world examples.

**Example:**
```bash
aptitude --help
```

**Output (sample):**
```text
Usage/help information for `aptitude` (illustrative; exact output varies by distribution/version).
```

### 389. `pacman`
**संक्षिप्त जानकारी:** the pacman package manager in Linux, learn how to install, update, search, and remove packages using practical examples.

**Example:**
```bash
pacman --help
```

**Output (sample):**
```text
Usage/help information for `pacman` (illustrative; exact output varies by distribution/version).
```

### 390. `zypper`
**संक्षिप्त जानकारी:** the zypper command, a powerful package management tool for SUSE-based Linux distributions. Learn how to install, update, search, and remove packages using zypper with practical examples.

**Example:**
```bash
zypper --help
```

**Output (sample):**
```text
Usage/help information for `zypper` (illustrative; exact output varies by distribution/version).
```

### 391. `emerge`
**संक्षिप्त जानकारी:** the powerful emerge command in Linux, learn how to install packages, update and upgrade your system with practical examples.

**Example:**
```bash
emerge --help
```

**Output (sample):**
```text
Usage/help information for `emerge` (illustrative; exact output varies by distribution/version).
```

### 392. `dnf`
**संक्षिप्त जानकारी:** the powerful dnf command in Linux, learn how to install, update, manage packages and dependencies, and leverage package groups for efficient package management. Scripting and Programming

**Example:**
```bash
dnf --help
```

**Output (sample):**
```text
Usage/help information for `dnf` (illustrative; exact output varies by distribution/version).
```

### 393. `snap`
**संक्षिप्त जानकारी:** the power of the Snap package manager in Linux. Learn how to install, update, and manage Snap packages through practical examples, enhancing your Linux package management skills.

**Example:**
```bash
snap list
```

**Output (sample):**
```text
Name  Version  Rev  Tracking  Publisher
```

### 394. `flatpak`
**संक्षिप्त जानकारी:** the Flatpak package management tool for Linux, learn how to install and manage Flatpak applications, and customize Flatpak environments for your specific needs.

**Example:**
```bash
flatpak list
```

**Output (sample):**
```text
Name  Application ID  Version
```

### 395. `bash`
**संक्षिप्त जानकारी:** the power of Linux bash commands with practical examples. Learn essential file system navigation, file and directory manipulation, and data searching and filtering techniques.

**Example:**
```bash
bash --version | head -n 1
```

**Output (sample):**
```text
GNU bash, version 5.x
```

### 396. `sh`
**संक्षिप्त जानकारी:** the power of the Linux sh command through practical examples. Learn shell scripting basics, utilize variables and parameters, and implement conditional statements and loops to automate tasks efficiently.

**Example:**
```bash
sh -c 'echo hello'
```

**Output (sample):**
```text
hello
```

### 397. `perl`
**संक्षिप्त जानकारी:** how to use Perl programming language in Linux, including executing Perl scripts and practical examples for file manipulation.

**Example:**
```bash
perl -e 'print 2+3'
```

**Output (sample):**
```text
5
```

### 398. `python`
**संक्षिप्त जानकारी:** Python's built-in functions, string manipulation, and file/directory management in Linux through practical examples.

**Example:**
```bash
python3 -c 'print(2+3)'
```

**Output (sample):**
```text
5
```

### 399. `gcc`
**संक्षिप्त जानकारी:** the GCC compiler, learn to compile C programs, and discover optimization flags for efficient code.

**Example:**
```bash
gcc --version | head -n 1
```

**Output (sample):**
```text
gcc (Ubuntu ...) 13.x
```

### 400. `g++`
**संक्षिप्त जानकारी:** the basics of the g++ command, compile a simple C++ program, and explore compiler flags and optimization techniques in this practical Linux programming lab.

**Example:**
```bash
g++ --version | head -n 1
```

**Output (sample):**
```text
g++ (Ubuntu ...) 13.x
```

### 401. `make`
**संक्षिप्त जानकारी:** the power of the make command in Linux, learn its syntax, and apply it to compile C programs with practical examples.

**Example:**
```bash
make
```

**Output (sample):**
```text
gcc ... -o app
```

### 402. `cmake`
**संक्षिप्त जानकारी:** how to use the CMake tool to build and manage C++ projects on Linux. This lab covers installing CMake, creating a simple C++ project, and understanding different build configurations.

**Example:**
```bash
cmake -S . -B build
```

**Output (sample):**
```text
-- The C compiler identification is GNU ...
-- Configuring done
```

### 403. `automake`
**संक्षिप्त जानकारी:** the automake command in Linux, a tool for generating Makefiles. Learn how to create a basic automake project, customize configuration, and apply practical examples.

**Example:**
```bash
automake --help
```

**Output (sample):**
```text
Usage/help information for `automake` (illustrative; exact output varies by distribution/version).
```

### 404. `autoconf`
**संक्षिप्त जानकारी:** how to use the autoconf command to configure and build C programs, from simple to complex projects, with practical examples.

**Example:**
```bash
autoconf --help
```

**Output (sample):**
```text
Usage/help information for `autoconf` (illustrative; exact output varies by distribution/version).
```

### 405. `gdb`
**संक्षिप्त जानकारी:** the power of the gdb debugger in Linux. Learn how to debug simple and multithreaded C programs, uncover bugs, and enhance your programming skills.

**Example:**
```bash
gdb ./app
```

**Output (sample):**
```text
GNU gdb ...
(gdb)
```

### 406. `ldd`
**संक्षिप्त जानकारी:** the ldd command in Linux, learn how to identify dynamic dependencies of binaries, and troubleshoot missing dependencies for effective software management.

**Example:**
```bash
ldd /bin/ls
```

**Output (sample):**
```text
linux-vdso.so.1 => ...
libc.so.6 => ...
```

### 407. `objdump`
**संक्षिप्त जानकारी:** the powerful objdump command in Linux, learn its syntax, options, and analyze the output on a simple C program.

**Example:**
```bash
objdump -h app | head
```

**Output (sample):**
```text
Sections:
Idx Name Size ...
```

### 408. `nm`
**संक्षिप्त जानकारी:** the Linux nm command, which displays symbol information for object files. Learn how to use nm to view executable symbols, filter results, and gain practical insights.

**Example:**
```bash
nm app | head
```

**Output (sample):**
```text
000000... T main
```

### 409. `readelf`
**संक्षिप्त जानकारी:** the readelf command in Linux, learn how to analyze ELF file headers and sections, and gain practical experience with real-world examples.

**Example:**
```bash
readelf -h app | head
```

**Output (sample):**
```text
ELF Header:
  Class: ELF64
```

### 410. `strings`
**संक्षिप्त जानकारी:** the Linux strings command and learn how to extract strings from binary, compressed, and encrypted files. Gain practical experience with real- world examples.

**Example:**
```bash
strings app | head
```

**Output (sample):**
```text
Hello Linux
```

### 411. `ctags`
**संक्षिप्त जानकारी:** the power of the ctags command in Linux, learn how to generate tags for C/C++ projects, and navigate source code efficiently.

**Example:**
```bash
ctags --help
```

**Output (sample):**
```text
Usage/help information for `ctags` (illustrative; exact output varies by distribution/version).
```

### 412. `cscope`
**संक्षिप्त जानकारी:** the cscope command in Linux, a powerful tool for source code navigation and analysis. Learn how to install, understand the basics, and perform efficient code searches and navigation.

**Example:**
```bash
cscope --help
```

**Output (sample):**
```text
Usage/help information for `cscope` (illustrative; exact output varies by distribution/version).
```

### 413. `diff3`
**संक्षिप्त जानकारी:** the diff3 command in Linux, learn how to merge conflicting files, and resolve conflicts in a three-way merge with practical examples.

**Example:**
```bash
diff3 --help
```

**Output (sample):**
```text
Usage/help information for `diff3` (illustrative; exact output varies by distribution/version).
```

### 414. `svn`
**संक्षिप्त जानकारी:** the power of the SVN command- line tool on Ubuntu 22.04. Learn how to install Subversion, initialize a local repository, and manage changes through commit, update, and revert operations.

**Example:**
```bash
svn status
```

**Output (sample):**
```text
M       file.txt
```

### 415. `git`
**संक्षिप्त जानकारी:** the essential git commands for version control, including initializing a repository, adding and committing files, and managing branches. Gain practical experience with hands-on examples.

**Example:**
```bash
git status
```

**Output (sample):**
```text
On branch main
nothing to commit, working tree clean
```

### 416. `cvs`
**संक्षिप्त जानकारी:** the Concurrent Versions System (CVS) command in Linux, learn how to create a repository, check out projects, and commit changes, with practical examples.

**Example:**
```bash
cvs --help
```

**Output (sample):**
```text
Usage/help information for `cvs` (illustrative; exact output varies by distribution/version).
```

### 417. `aclocal`
**संक्षिप्त जानकारी:** the aclocal command in Linux, learn how to generate the aclocal.m4 file, and integrate it with Autoconf for effective build automation.

**Example:**
```bash
aclocal --help
```

**Output (sample):**
```text
Usage/help information for `aclocal` (illustrative; exact output varies by distribution/version).
```

### 418. `autoheader`
**संक्षिप्त जानकारी:** the autoheader command in Linux, learn its purpose, and discover practical examples to generate configuration header files.

**Example:**
```bash
autoheader --help
```

**Output (sample):**
```text
Usage/help information for `autoheader` (illustrative; exact output varies by distribution/version).
```

### 419. `autoreconf`
**संक्षिप्त जानकारी:** the autoreconf command in Linux, learn its purpose, and apply it to a sample project. Gain hands-on experience in automating the build process for your software projects. Backup and Compression

**Example:**
```bash
autoreconf --help
```

**Output (sample):**
```text
Usage/help information for `autoreconf` (illustrative; exact output varies by distribution/version).
```

### 420. `bison`
**संक्षिप्त जानकारी:** the bison command, a powerful tool for generating parsers in Linux. Learn how to create custom parsers, handle syntax errors, and apply bison in practical scenarios.

**Example:**
```bash
bison --help
```

**Output (sample):**
```text
Usage/help information for `bison` (illustrative; exact output varies by distribution/version).
```

### 421. `expect`
**संक्षिप्त जानकारी:** the power of the expect command in Linux. Learn to automate SSH login, handle prompts, and write responsive scripts for various tasks.

**Example:**
```bash
expect --help
```

**Output (sample):**
```text
Usage/help information for `expect` (illustrative; exact output varies by distribution/version).
```

### 422. `bzip2recover`
**संक्षिप्त जानकारी:** the bzip2recover command, a powerful tool for recovering corrupted bzip2 files. Learn how to use it effectively with practical examples and advanced options.

**Example:**
```bash
bzip2recover --help
```

**Output (sample):**
```text
Usage/help information for `bzip2recover` (illustrative; exact output varies by distribution/version).
```

### 423. `uuencode`
**संक्षिप्त जानकारी:** the uuencode command in Linux, learn how to encode and decode files, and discover practical use cases for this versatile tool in backup and compression workflows.

**Example:**
```bash
uuencode --help
```

**Output (sample):**
```text
Usage/help information for `uuencode` (illustrative; exact output varies by distribution/version).
```

### 424. `uudecode`
**संक्षिप्त जानकारी:** how to use the uudecode command in Linux to decode uuencoded files. Explore practical examples and understand the purpose of this useful tool for backup and compression tasks.

**Example:**
```bash
uudecode --help
```

**Output (sample):**
```text
Usage/help information for `uudecode` (illustrative; exact output varies by distribution/version).
```

### 425. `gzexe`
**संक्षिप्त जानकारी:** the gzexe command in Linux, learn how to compress and decompress executable files, and discover practical examples of its usage.

**Example:**
```bash
gzexe --help
```

**Output (sample):**
```text
Usage/help information for `gzexe` (illustrative; exact output varies by distribution/version).
```

### 426. `sum`
**संक्षिप्त जानकारी:** the Linux sum command with practical examples, including basic summation operations and handling floating-point numbers. Gain proficiency in file checksum calculations and data verification.

**Example:**
```bash
sum --help
```

**Output (sample):**
```text
Usage/help information for `sum` (illustrative; exact output varies by distribution/version).
```

### 427. `md5sum`
**संक्षिप्त जानकारी:** the md5sum command in Linux, learn how to generate and verify MD5 checksums for files, and ensure data integrity with practical examples.

**Example:**
```bash
md5sum --help
```

**Output (sample):**
```text
Usage/help information for `md5sum` (illustrative; exact output varies by distribution/version).
```

### 428. `dump`
**संक्षिप्त जानकारी:** the Linux dump command for full system backups. Learn how to perform a complete system backup and restore data from the dump file, with practical examples. Miscellaneous Utilities

**Example:**
```bash
dump --help
```

**Output (sample):**
```text
Usage/help information for `dump` (illustrative; exact output varies by distribution/version).
```

### 429. `restore`
**संक्षिप्त जानकारी:** how to use the Linux restore command to recover specific files or entire directory structures from backup archives. Explore practical examples and understand the purpose and usage of this essential backup and...

**Example:**
```bash
restore --help
```

**Output (sample):**
```text
Usage/help information for `restore` (illustrative; exact output varies by distribution/version).
```

### 430. `rmt`
**संक्षिप्त जानकारी:** the rmt command in Linux, learn how to backup and restore files, and automate backups using cron jobs. Enhance your system administration skills with practical examples.

**Example:**
```bash
rmt --help
```

**Output (sample):**
```text
Usage/help information for `rmt` (illustrative; exact output varies by distribution/version).
```

### 431. `man`
**संक्षिप्त जानकारी:** the powerful Linux man command, learn how to navigate man pages, and perform targeted searches to effectively utilize system documentation.

**Example:**
```bash
man ls
```

**Output (sample):**
```text
Interactive manual page for ls opens.
```

### 432. `info`
**संक्षिप्त जानकारी:** the Linux info command, its purpose, options, and practical examples to retrieve information about Linux commands and utilities.

**Example:**
```bash
info coreutils 'ls invocation'
```

**Output (sample):**
```text
GNU Info documentation opens.
```

### 433. `whatis`
**संक्षिप्त जानकारी:** the Linux whatis command, its purpose, syntax, and practical use cases. Learn how to effectively utilize this utility to quickly retrieve information about commands and system components.

**Example:**
```bash
whatis ls
```

**Output (sample):**
```text
ls (1) - list directory contents
```

### 434. `apropos`
**संक्षिप्त जानकारी:** the Linux apropos command, a powerful tool for searching man pages and finding relevant system commands. Learn how to perform basic searches, customize with regular expressions, and discover practical use cases.

**Example:**
```bash
apropos network
```

**Output (sample):**
```text
ip (8) - show/manipulate routing...
ss (8) - another utility...
```

### 435. `yes`
**संक्षिप्त जानकारी:** the versatile Linux yes command and learn how to use it to generate repeated output, combine it with other commands, and automate various tasks.

**Example:**
```bash
yes | head -n 3
```

**Output (sample):**
```text
y
y
y
```

### 436. `sleep`
**संक्षिप्त जानकारी:** the Linux sleep command and its practical applications. Learn how to use sleep with time intervals and combine it with other commands for efficient task automation.

**Example:**
```bash
sleep 2
```

**Output (sample):**
```text
No output; waits for 2 seconds.
```

### 437. `bc`
**संक्षिप्त जानकारी:** the versatile Linux bc command and learn how to perform basic arithmetic operations, advanced calculations, and functions using practical examples.

**Example:**
```bash
echo '10/2' | bc
```

**Output (sample):**
```text
5
```

### 438. `clear`
**संक्षिप्त जानकारी:** the clear command in Linux, learn how to clear the terminal screen, and automate the process with a Bash script. Enhance your command-line skills and improve your workflow.

**Example:**
```bash
clear
```

**Output (sample):**
```text
Terminal screen is cleared.
```

### 439. `reset`
**संक्षिप्त जानकारी:** the Linux reset command and learn how to restore the terminal to a known state, troubleshoot terminal issues, and more with practical examples.

**Example:**
```bash
reset
```

**Output (sample):**
```text
Terminal is reset.
```

### 440. `echo`
**संक्षिप्त जानकारी:** the versatile echo command in Linux, learn its basic syntax, and discover practical examples for printing text, using variable substitution, and formatting output.

**Example:**
```bash
echo 'Hello Linux'
```

**Output (sample):**
```text
Hello Linux
```

### 441. `printf`
**संक्षिप्त जानकारी:** the power of the printf command in Linux. Learn how to format output, print variables, and evaluate expressions using practical examples.

**Example:**
```bash
printf 'Name: %s\n' Prakash
```

**Output (sample):**
```text
Name: Prakash
```

### 442. `seq`
**संक्षिप्त जानकारी:** the versatile seq command in Linux, learn how to generate numeric sequences, and customize them with step size and formatting.

**Example:**
```bash
seq 1 5
```

**Output (sample):**
```text
1
2
3
4
5
```

### 443. `history`
**संक्षिप्त जानकारी:** the powerful Linux history command and learn how to effectively manage and analyze command history for improved productivity and troubleshooting.

**Example:**
```bash
history | tail -n 3
```

**Output (sample):**
```text
498  ls
499  pwd
500  history
```

### 444. `xargs`
**संक्षिप्त जानकारी:** the power of the xargs command in Linux, learn how to execute commands with arguments, and combine it with other utilities for efficient workflows.

**Example:**
```bash
printf 'a\nb\n' | xargs -n1 echo
```

**Output (sample):**
```text
a
b
```

### 445. `factor`
**संक्षिप्त जानकारी:** the Linux factor command, its purpose, syntax, and practical examples to gain a deeper understanding of this useful miscellaneous utility.

**Example:**
```bash
factor 12
```

**Output (sample):**
```text
12: 2 2 3
```

### 446. `units`
**संक्षिप्त जानकारी:** the versatile Linux units command and learn how to convert between different time units and perform arithmetic operations with practical examples.

**Example:**
```bash
units '1 meter' 'centimeter'
```

**Output (sample):**
```text
100 centimeter
```

### 447. `script`
**संक्षिप्त जानकारी:** the power of shell scripting with this hands-on lab. Learn to write and execute simple scripts, use variables and command substitution, and implement conditional statements and loops for more complex tasks.

**Example:**
```bash
script session.log
```

**Output (sample):**
```text
Script started, file is session.log
```

### 448. `scriptreplay`
**संक्षिप्त जानकारी:** the scriptreplay command in Linux, which allows you to record and replay terminal sessions, with practical examples to enhance your system administration skills.

**Example:**
```bash
scriptreplay timing.txt typescript
```

**Output (sample):**
```text
Recorded terminal session is replayed.
```

### 449. `xdg-open`
**संक्षिप्त जानकारी:** the versatile xdg-open command in Linux, which allows you to open files and directories with their default applications, and customize the default associations.

**Example:**
```bash
xdg-open https://example.com
```

**Output (sample):**
```text
Default browser opens.
```

### 450. `poweroff`
**संक्षिप्त जानकारी:** how to safely shut down your Linux system using the poweroff command, including practical examples and automating system shutdown with cron.

**Example:**
```bash
sudo poweroff
```

**Output (sample):**
```text
System powers off.
```

### 451. `access`
**संक्षिप्त जानकारी:** the Linux access command and learn how to manage file permissions and ownership. Discover practical examples to enhance your Linux skills.

**Example:**
```bash
access file.txt
```

**Output (sample):**
```text
0  # accessible
```

### 452. `accton`
**संक्षिप्त जानकारी:** the Linux accton command and learn how to manage network interface configuration, troubleshoot network issues, and more with practical examples.

**Example:**
```bash
accton --help
```

**Output (sample):**
```text
Usage/help information for `accton` (illustrative; exact output varies by distribution/version).
```

### 453. `acpi`
**संक्षिप्त जानकारी:** the Linux acpi command and its practical applications, including monitoring battery status and customizing acpi behavior. Gain a comprehensive understanding of this versatile utility.

**Example:**
```bash
acpi -b
```

**Output (sample):**
```text
Battery 0: Full, 100%
```

### 454. `acpid`
**संक्षिप्त जानकारी:** the Linux acpid command, learn how to configure it to monitor power events, and create custom event handlers for practical applications.

**Example:**
```bash
acpid --help
```

**Output (sample):**
```text
Usage/help information for `acpid` (illustrative; exact output varies by distribution/version).
```

### 455. `addr2line`
**संक्षिप्त जानकारी:** the addr2line command in Linux, a powerful tool for resolving addresses to function names and source file locations. Learn its basic syntax, options, and practical use cases.

**Example:**
```bash
addr2line -e app 0x401136
```

**Output (sample):**
```text
main at main.c:10
```

### 456. `agetty`
**संक्षिप्त जानकारी:** the agetty command in Linux, learn how to configure it for serial console access, and manage user login processes effectively.

**Example:**
```bash
agetty --help
```

**Output (sample):**
```text
Usage/help information for `agetty` (illustrative; exact output varies by distribution/version).
```

### 457. `amixer`
**संक्षिप्त जानकारी:** the amixer command, a powerful Linux utility for adjusting sound card mixer settings. Learn how to control master volume, manage specific sound channels, and apply practical examples to enhance your audio experience.

**Example:**
```bash
amixer get Master
```

**Output (sample):**
```text
Mono: Playback 80 [80%] [on]
```

### 458. `aplay`
**संक्षिप्त जानकारी:** the aplay command in Linux, learn how to install required packages, play audio files, and discover various command options and flags for audio manipulation.

**Example:**
```bash
aplay --list-devices
```

**Output (sample):**
```text
card 0: ...
```

### 459. `aplaymidi`
**संक्षिप्त जानकारी:** the aplaymidi command, a powerful Linux utility for playing MIDI files. Learn how to use it for basic playback, as well as advanced options for controlling MIDI devices.

**Example:**
```bash
aplaymidi --help
```

**Output (sample):**
```text
Usage/help information for `aplaymidi` (illustrative; exact output varies by distribution/version).
```

### 460. `autoupdate`
**संक्षिप्त जानकारी:** the power of automatic updates on Linux systems. Learn how to configure and manage automatic updates using the command line, ensuring your system stays secure and up-to-date.

**Example:**
```bash
autoupdate --help
```

**Output (sample):**
```text
Usage/help information for `autoupdate` (illustrative; exact output varies by distribution/version).
```

### 461. `banner`
**संक्षिप्त जानकारी:** the versatile banner command in Linux, learn how to display custom messages, and customize the appearance of your banners for various use cases.

**Example:**
```bash
banner --help
```

**Output (sample):**
```text
Usage/help information for `banner` (illustrative; exact output varies by distribution/version).
```

### 462. `biff`
**संक्षिप्त जानकारी:** the biff command in Linux, learn how to configure it to receive notifications, and customize the notification settings for enhanced productivity.

**Example:**
```bash
biff --help
```

**Output (sample):**
```text
Usage/help information for `biff` (illustrative; exact output varies by distribution/version).
```

### 463. `bzcmp`
**संक्षिप्त जानकारी:** the bzcmp command in Linux, which allows you to compare compressed files. Learn how to use this utility effectively with practical examples.

**Example:**
```bash
bzcmp --help
```

**Output (sample):**
```text
Usage/help information for `bzcmp` (illustrative; exact output varies by distribution/version).
```

### 464. `case`
**संक्षिप्त जानकारी:** the case command in Linux, learn its syntax and usage, and apply it to automate file management and backup operations.

**Example:**
```bash
help case
```

**Output (sample):**
```text
Built-in shell command 'case'; output/behavior depends on the shell.
```

### 465. `cc`
**संक्षिप्त जानकारी:** the versatile Linux cc command, learn its syntax, and compile C programs with practical examples. Discover compiler flags and optimization options to enhance your programming workflow.

**Example:**
```bash
cc --help
```

**Output (sample):**
```text
Usage/help information for `cc` (illustrative; exact output varies by distribution/version).
```

### 466. `chvt`
**संक्षिप्त जानकारी:** the chvt command in Linux, which allows you to switch between virtual terminals. Learn practical examples and automate virtual terminal switching for enhanced productivity.

**Example:**
```bash
chvt --help
```

**Output (sample):**
```text
Usage/help information for `chvt` (illustrative; exact output varies by distribution/version).
```

### 467. `cpp`
**संक्षिप्त जानकारी:** the power of C++ programming in Linux, from compiling and running code to managing files and directories. Dive into practical examples and master essential Linux utilities for efficient C++ development.

**Example:**
```bash
cpp file.c | head
```

**Output (sample):**
```text
# 1 "file.c"
```

### 468. `cupsd`
**संक्षिप्त जानकारी:** the CUPS printing system and learn how to manage printers using the cupsd command. Configure printer settings and gain practical experience with this essential Linux utility.

**Example:**
```bash
cupsd --help
```

**Output (sample):**
```text
Usage/help information for `cupsd` (illustrative; exact output varies by distribution/version).
```

### 469. `dc`
**संक्षिप्त जानकारी:** the powerful dc command in Linux, a versatile calculator tool. Learn to perform basic arithmetic operations, handle advanced calculations, and leverage dc's capabilities for various computing tasks.

**Example:**
```bash
echo '10 2 / p' | dc
```

**Output (sample):**
```text
5
```

### 470. `dir`
**संक्षिप्त जानकारी:** the Linux dir command and its practical applications for managing directories and files. Learn various options to customize directory listings and effectively navigate the file system.

**Example:**
```bash
dir
```

**Output (sample):**
```text
file.txt  notes.txt
```

### 471. `disable`
**संक्षिप्त जानकारी:** the Linux disable command and learn how to disable services using practical examples. Understand the purpose and verify the disabled status of services.

**Example:**
```bash
disable --help
```

**Output (sample):**
```text
Usage/help information for `disable` (illustrative; exact output varies by distribution/version).
```

### 472. `domainname`
**संक्षिप्त जानकारी:** the Linux domainname command and learn how to set, display, and manage domain names across network interfaces with practical examples.

**Example:**
```bash
domainname --help
```

**Output (sample):**
```text
Usage/help information for `domainname` (illustrative; exact output varies by distribution/version).
```

### 473. `dos2unix`
**संक्षिप्त जानकारी:** how to use the dos2unix command to convert text files from DOS to Unix format. Explore practical examples and automate the conversion process with shell scripts.

**Example:**
```bash
dos2unix file.txt
```

**Output (sample):**
```text
dos2unix: converting file file.txt to Unix format...
```

### 474. `dosfsck`
**संक्षिप्त जानकारी:** the Linux dosfsck command with practical examples. Learn how to check and repair errors on a FAT32 file system, and perform a thorough filesystem check and repair on a USB drive.

**Example:**
```bash
dosfsck --help
```

**Output (sample):**
```text
Usage/help information for `dosfsck` (illustrative; exact output varies by distribution/version).
```

### 475. `exec`
**संक्षिप्त जानकारी:** the Linux exec command and its practical applications, including understanding the exec system call, executing external commands, and redirecting input/output.

**Example:**
```bash
help exec
```

**Output (sample):**
```text
Built-in shell command 'exec'; output/behavior depends on the shell.
```

### 476. `fc`
**संक्षिप्त जानकारी:** the fc command in Linux, which allows you to edit and reexecute previous commands. Learn how to customize its behavior for improved productivity.

**Example:**
```bash
fc --help
```

**Output (sample):**
```text
Usage/help information for `fc` (illustrative; exact output varies by distribution/version).
```

### 477. `fc-cache`
**संक्षिप्त जानकारी:** the Linux fc-cache command and learn how to manage font caches effectively. Discover practical examples to update and troubleshoot font cache issues on your system.

**Example:**
```bash
fc-cache -f
```

**Output (sample):**
```text
No output on success.
```

### 478. `fc-list`
**संक्षिप्त जानकारी:** the fc-list command in Linux, which allows you to list all available fonts on your system, filter by family, style, and other attributes. Gain practical knowledge for font management and customization.

**Example:**
```bash
fc-list | head -n 2
```

**Output (sample):**
```text
/usr/share/fonts/...: DejaVu Sans
```

### 479. `getent`
**संक्षिप्त जानकारी:** the versatile getent command in Linux, learn how to retrieve user and group information, and discover practical examples to enhance your system administration skills.

**Example:**
```bash
getent passwd root
```

**Output (sample):**
```text
root:x:0:0:root:/root:/bin/bash
```

### 480. `gs`
**संक्षिप्त जानकारी:** the versatile gs command in Linux, learn to convert PDF files to various image formats, and optimize PDF files by reducing file size.

**Example:**
```bash
gs --help
```

**Output (sample):**
```text
Usage/help information for `gs` (illustrative; exact output varies by distribution/version).
```

### 481. `hash`
**संक्षिप्त जानकारी:** the Linux hash command and learn how to calculate hashes of files and directories, as well as verify file integrity using hash checksums.

**Example:**
```bash
hash --help
```

**Output (sample):**
```text
Usage/help information for `hash` (illustrative; exact output varies by distribution/version).
```

### 482. `hexdump`
**संक्षिप्त जानकारी:** the Linux hexdump command, a powerful tool for viewing and manipulating binary data. Learn how to use hexdump to analyze file contents, customize output, and gain insights into data structures.

**Example:**
```bash
hexdump -C hello.txt
```

**Output (sample):**
```text
00000000  48 65 6c 6c 6f 0a  |Hello.|
```

### 483. `hostid`
**संक्षिप्त जानकारी:** the Linux hostid command, learn how to retrieve the unique host identifier, and discover practical applications for this versatile utility.

**Example:**
```bash
hostid
```

**Output (sample):**
```text
a1b2c3d4
```

### 484. `iconv`
**संक्षिप्त जानकारी:** the powerful iconv command in Linux, which enables seamless encoding conversion and handling of multilingual text. Learn practical examples to enhance your text processing capabilities.

**Example:**
```bash
iconv -f UTF-8 -t UTF-16 file.txt > file16.txt
```

**Output (sample):**
```text
No output on success.
```

### 485. `import`
**संक्षिप्त जानकारी:** the import command in Linux, learn how to import data from CSV files and Excel spreadsheets into database tables, and gain practical experience with this versatile utility.

**Example:**
```bash
import --help
```

**Output (sample):**
```text
Usage/help information for `import` (illustrative; exact output varies by distribution/version).
```

### 486. `install`
**संक्षिप्त जानकारी:** how to install Linux packages using various commands like apt-get, apt, and Snap. Explore practical examples and gain proficiency in package management on your Linux system.

**Example:**
```bash
sudo apt install curl
```

**Output (sample):**
```text
Reading package lists...
Setting up curl ...
```

### 487. `ipcrm`
**संक्षिप्त जानकारी:** the Linux ipcrm command, which allows you to remove shared memory segments, message queues, and semaphores. Learn the command syntax, options, and practical examples to effectively manage IPC objects on your system.

**Example:**
```bash
ipcrm --help
```

**Output (sample):**
```text
Usage/help information for `ipcrm` (illustrative; exact output varies by distribution/version).
```

### 488. `ipcs`
**संक्षिप्त जानकारी:** the Linux ipcs command, its purpose, and practical examples to analyze IPC resources and identify potential issues on your system.

**Example:**
```bash
ipcs --help
```

**Output (sample):**
```text
Usage/help information for `ipcs` (illustrative; exact output varies by distribution/version).
```

### 489. `pinky`
**संक्षिप्त जानकारी:** the pinky command in Linux, learn its options and flags, and discover practical use cases to enhance your system management skills.

**Example:**
```bash
pinky --help
```

**Output (sample):**
```text
Usage/help information for `pinky` (illustrative; exact output varies by distribution/version).
```

### 490. `ranlib`
**संक्षिप्त जानकारी:** the Linux ranlib command, learn how to create and manage static libraries, and discover practical examples to enhance your system administration skills.

**Example:**
```bash
ranlib libdemo.a
```

**Output (sample):**
```text
No output on success.
```

### 491. `rev`
**संक्षिप्त जानकारी:** the Linux rev command and learn how to reverse text in files, reverse lines, and apply practical examples to enhance your command-line skills.

**Example:**
```bash
rev --help
```

**Output (sample):**
```text
Usage/help information for `rev` (illustrative; exact output varies by distribution/version).
```

---

## ⚠️ महत्वपूर्ण नोटहरू

1. सबै 491 commands लाई PDF को numbering अनुसार समेटिएको छ।
2. केही commands पुराना/legacy, package-dependent, distro-specific वा विशेष hardware/service का लागि मात्र उपलब्ध हुन सक्छन्।
3. `ifconfig`, `netstat` जस्ता केही पुराना networking utilities को modern विकल्पका रूपमा `ip` र `ss` प्रयोग गरिन्छ।
4. `Example` र `Output` हरू अभ्यासका लागि representative हुन्; आफ्नो system मा command चलाउँदा output फरक आउन सक्छ।
5. Destructive commands (`dd`, `mkfs`, `fdisk`, `parted`, `rm -rf`, firewall changes आदि) वास्तविक disk/server मा चलाउनु अघि command दोहोर्‍याएर verify गर्नुहोस्।

## 📖 Source
संलग्न `linux.pdf` — **Linux Commands Cheat Sheet: A clean and minimal guide to 491 Linux commands**.
