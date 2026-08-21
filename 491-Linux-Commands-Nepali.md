<a id="top"></a>
# 🐧 Linux 491 Commands — नेपालीमा Category-wise Quick Guide

> 📄 **स्रोत:** संलग्न `linux.pdf` मा रहेका 491 Linux commands को सूची र category structure लाई आधार बनाइएको हो। तलका **Example** र **Output** सिकाइका लागि तयार गरिएका representative/illustrative नमूना हुन् — तपाईंको आफ्नै Linux distribution, version, user, file, hardware वा configuration अनुसार वास्तविक output फरक हुन सक्छ।

## 📌 कसरी प्रयोग गर्ने

| चिन्ह | अर्थ |
|---|---|
| 🔤 `Command` | टर्मिनलमा टाइप गरी चलाउने वास्तविक command |
| 💡 **संक्षिप्त जानकारी** | command ले के गर्छ भन्ने एक-लाइने सजिलो व्याख्या |
| 🧪 **Example** | प्रयोग गर्ने practical syntax |
| 🖥️ **Output** | चलाउँदा देखिने सामान्य/illustrative परिणाम |

> ⚠️ **ध्यान दिनुहोस्:** `sudo`, `rm`, `dd`, `mkfs`, partition, firewall, र user-management जस्ता commands production system मा चलाउनुअघि राम्ररी बुझेर मात्र सावधानीपूर्वक प्रयोग गर्नुहोस्। यी command हरूले data नष्ट गर्न वा system बिगार्न सक्छन्।

## 💡 प्रयोगको सुझाव
यो document निकै लामो (491 commands) भएकोले, हरेक category **collapsible (थिच्दा खुल्ने/बन्द हुने)** बनाइएको छ। तल दिइएको सूचीबाट चाहिएको category मा क्लिक गर्नुहोस् — त्यो section खुल्ला हुनेछ। `Ctrl+F` (वा `Cmd+F`) प्रयोग गरेर कुनै specific command पनि छिट्टै खोज्न सक्नुहुन्छ।

## 📚 Categories — यहाँबाट सिधै जानुहोस्

| # | Category | Commands |
|---|---|---|
| 1 | [📁 Basic File and Directory Operations](#cat-1-52) | **52** |
| 2 | [📝 Text Processing and Editing](#cat-53-96) | **44** |
| 3 | [📊 System Monitoring and Management](#cat-97-145) | **49** |
| 4 | [👤 User and Permission Management](#cat-146-175) | **30** |
| 5 | [🌐 Networking and Communication](#cat-176-243) | **68** |
| 6 | [💽 Disk and File System Utilities](#cat-244-286) | **43** |
| 7 | [📦 Compression and Archiving](#cat-287-309) | **23** |
| 8 | [⚙️ Process Management](#cat-310-333) | **24** |
| 9 | [🛠️ System Configuration and Settings](#cat-334-491) | **158** |
| | **कुल (Total)** | **491** |

---

<a id="cat-1-52"></a>
<details>
<summary><h2 style="display:inline;">📁 Basic File and Directory Operations</h2> &nbsp; <em>Commands 1–52 (52 commands)</em></summary>

### 1. `ls`
**संक्षिप्त जानकारी:** हालको directory भित्रका file र folder हरूको सूची देखाउँछ।

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
**संक्षिप्त जानकारी:** एक directory बाट अर्को directory मा जान प्रयोग हुन्छ।

**Example:**
```bash
cd /var/log
```

**Output (sample):**
```text
No output; the working directory changes.
```

### 3. `pwd`
**संक्षिप्त जानकारी:** अहिले काम गरिरहेको directory को पूरा path देखाउँछ।

**Example:**
```bash
pwd
```

**Output (sample):**
```text
/home/user
```

### 4. `mkdir`
**संक्षिप्त जानकारी:** नयाँ directory बनाउन प्रयोग हुन्छ।

**Example:**
```bash
mkdir projects
```

**Output (sample):**
```text
No output; directory 'projects' is created.
```

### 5. `touch`
**संक्षिप्त जानकारी:** नयाँ खाली file बनाउन वा file को timestamp अद्यावधिक गर्न प्रयोग हुन्छ।

**Example:**
```bash
touch notes.txt
```

**Output (sample):**
```text
No output; 'notes.txt' is created if it does not exist.
```

### 6. `cp`
**संक्षिप्त जानकारी:** file वा directory को प्रतिलिपि बनाउन प्रयोग हुन्छ।

**Example:**
```bash
cp file.txt backup.txt
```

**Output (sample):**
```text
No output; 'backup.txt' is created.
```

### 7. `mv`
**संक्षिप्त जानकारी:** file/folder सार्न वा नाम परिवर्तन गर्न प्रयोग हुन्छ।

**Example:**
```bash
mv old.txt new.txt
```

**Output (sample):**
```text
No output; the file is renamed.
```

### 8. `rm`
**संक्षिप्त जानकारी:** file वा directory हटाउन प्रयोग हुन्छ।

**Example:**
```bash
rm old.txt
```

**Output (sample):**
```text
No output when the file is removed successfully.
```

### 9. `ln`
**संक्षिप्त जानकारी:** file हरूको बीचमा hard वा symbolic (soft) link बनाउँछ।

**Example:**
```bash
ln -s /var/log/syslog syslog.link
```

**Output (sample):**
```text
No output; a symbolic link is created.
```

### 10. `cat`
**संक्षिप्त जानकारी:** file को सामग्री terminal मा देखाउँछ।

**Example:**
```bash
cat hello.txt
```

**Output (sample):**
```text
Hello Linux
```

### 11. `less`
**संक्षिप्त जानकारी:** ठूलो file लाई सजिलै scroll गरेर पढ्न प्रयोग हुन्छ।

**Example:**
```bash
less hello.txt
```

**Output (sample):**
```text
Interactive pager opens; press q to quit.
```

### 12. `more`
**संक्षिप्त जानकारी:** ठूलो text file लाई page अनुसार पढ्न मद्दत गर्छ।

**Example:**
```bash
more hello.txt
```

**Output (sample):**
```text
Hello Linux
```

### 13. `tree`
**संक्षिप्त जानकारी:** directory structure लाई tree (hierarchical) रूपमा देखाउँछ।

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
**संक्षिप्त जानकारी:** file वा directory ले प्रयोग गरेको disk space देखाउँछ।

**Example:**
```bash
du -sh .
```

**Output (sample):**
```text
12M	.
```

### 15. `df`
**संक्षिप्त जानकारी:** disk मा कति space प्रयोग/बाँकी छ देखाउँछ।

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
**संक्षिप्त जानकारी:** file को size, permission, timestamp जस्ता विवरण देखाउँछ।

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
**संक्षिप्त जानकारी:** निर्धारित स्थानमा file वा directory खोज्छ।

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
**संक्षिप्त जानकारी:** नामको आधारमा file छिटो खोज्छ।

**Example:**
```bash
locate notes.txt
```

**Output (sample):**
```text
/home/user/notes.txt
```

### 19. `updatedb`
**संक्षिप्त जानकारी:** locate command ले प्रयोग गर्ने file-name database अद्यावधिक गर्छ।

**Example:**
```bash
sudo updatedb
```

**Output (sample):**
```text
No output on success.
```

### 20. `which`
**संक्षिप्त जानकारी:** PATH भित्र भएको executable command को पूरा path देखाउँछ।

**Example:**
```bash
which bash
```

**Output (sample):**
```text
/usr/bin/bash
```

### 21. `whereis`
**संक्षिप्त जानकारी:** binary, source code, र man page फाइलहरूको स्थान खोज्छ।

**Example:**
```bash
whereis bash
```

**Output (sample):**
```text
bash: /usr/bin/bash /usr/share/man/man1/bash.1.gz
```

### 22. `file`
**संक्षिप्त जानकारी:** दिइएको file को प्रकार (type) पहिचान गर्छ।

**Example:**
```bash
file hello.txt
```

**Output (sample):**
```text
hello.txt: ASCII text
```

### 23. `od`
**संक्षिप्त जानकारी:** file लाई octal, hex वा अन्य format मा dump गर्छ।

**Example:**
```bash
od -An -tc hello.txt
```

**Output (sample):**
```text
 H e l l o \n
```

### 24. `mktemp`
**संक्षिप्त जानकारी:** सुरक्षित रूपमा unique temporary file वा directory बनाउँछ।

**Example:**
```bash
mktemp
```

**Output (sample):**
```text
/tmp/tmp.XYZ123
```

### 25. `basename`
**संक्षिप्त जानकारी:** path बाट directory भाग हटाई फाइलको नाम मात्र देखाउँछ।

**Example:**
```bash
basename /home/user/file.txt
```

**Output (sample):**
```text
file.txt
```

### 26. `dirname`
**संक्षिप्त जानकारी:** path बाट फाइलको नाम हटाई directory भाग मात्र देखाउँछ।

**Example:**
```bash
dirname /home/user/file.txt
```

**Output (sample):**
```text
/home/user
```

### 27. `dirs`
**संक्षिप्त जानकारी:** directory stack (pushd/popd ले प्रयोग गर्ने) देखाउँछ।

**Example:**
```bash
dirs
```

**Output (sample):**
```text
~ /var/log
```

### 28. `mc`
**संक्षिप्त जानकारी:** Midnight Commander, dual-pane text-based file manager सुरु गर्छ।

**Example:**
```bash
mc --help
```

**Output (sample):**
```text
Usage/help information for `mc` (illustrative; exact output varies by distribution/version).
```

### 29. `readlink`
**संक्षिप्त जानकारी:** symbolic link ले point गरेको वास्तविक path देखाउँछ।

**Example:**
```bash
readlink -f syslog.link
```

**Output (sample):**
```text
/var/log/syslog
```

### 30. `rename`
**संक्षिप्त जानकारी:** pattern प्रयोग गरी धेरै files एकैचोटि rename गर्छ।

**Example:**
```bash
rename 's/\.txt$/.bak/' *.txt
```

**Output (sample):**
```text
No output on success.
```

### 31. `rmdir`
**संक्षिप्त जानकारी:** खाली directory हटाउँछ।

**Example:**
```bash
rmdir emptydir
```

**Output (sample):**
```text
No output on success.
```

### 32. `shred`
**संक्षिप्त जानकारी:** file लाई बारम्बार overwrite गरी secure रूपमा मेट्छ।

**Example:**
```bash
shred -n 1 -z secret.txt
```

**Output (sample):**
```text
No output on success.
```

### 33. `chattr`
**संक्षिप्त जानकारी:** ext file system मा file attributes (जस्तै immutable) परिवर्तन गर्छ।

**Example:**
```bash
sudo chattr +i important.txt
```

**Output (sample):**
```text
No output on success.
```

### 34. `lsattr`
**संक्षिप्त जानकारी:** ext file system मा file attributes देखाउँछ।

**Example:**
```bash
lsattr important.txt
```

**Output (sample):**
```text
----i--------- important.txt
```

### 35. `cksum`
**संक्षिप्त जानकारी:** file को checksum र byte count निकाल्छ।

**Example:**
```bash
cksum hello.txt
```

**Output (sample):**
```text
123456789 12 hello.txt
```

### 36. `cmp`
**संक्षिप्त जानकारी:** दुई files लाई byte-by-byte तुलना गर्छ।

**Example:**
```bash
cmp file1.txt file2.txt
```

**Output (sample):**
```text
No output if the files are identical.
```

### 37. `mtools`
**संक्षिप्त जानकारी:** DOS file systems लाई सिधै access गर्ने utilities को सेट।

**Example:**
```bash
mtools --help
```

**Output (sample):**
```text
Usage/help information for `mtools` (illustrative; exact output varies by distribution/version).
```

### 38. `mcopy`
**संक्षिप्त जानकारी:** MS-DOS र Unix file systems बीच file copy गर्छ।

**Example:**
```bash
mcopy --help
```

**Output (sample):**
```text
Usage/help information for `mcopy` (illustrative; exact output varies by distribution/version).
```

### 39. `mdel`
**संक्षिप्त जानकारी:** MS-DOS file system बाट file मेट्छ।

**Example:**
```bash
mdel --help
```

**Output (sample):**
```text
Usage/help information for `mdel` (illustrative; exact output varies by distribution/version).
```

### 40. `mdir`
**संक्षिप्त जानकारी:** MS-DOS file system को directory सूची देखाउँछ।

**Example:**
```bash
mdir --help
```

**Output (sample):**
```text
Usage/help information for `mdir` (illustrative; exact output varies by distribution/version).
```

### 41. `mmove`
**संक्षिप्त जानकारी:** MS-DOS file system मा file/directory सार्छ वा rename गर्छ।

**Example:**
```bash
mmove --help
```

**Output (sample):**
```text
Usage/help information for `mmove` (illustrative; exact output varies by distribution/version).
```

### 42. `mread`
**संक्षिप्त जानकारी:** MS-DOS file पढ्छ (mcopy को alias)।

**Example:**
```bash
mread --help
```

**Output (sample):**
```text
Usage/help information for `mread` (illustrative; exact output varies by distribution/version).
```

### 43. `mren`
**संक्षिप्त जानकारी:** MS-DOS file system मा file rename गर्छ।

**Example:**
```bash
mren --help
```

**Output (sample):**
```text
Usage/help information for `mren` (illustrative; exact output varies by distribution/version).
```

### 44. `mshowfat`
**संक्षिप्त जानकारी:** MS-DOS file को FAT cluster मानचित्र देखाउँछ।

**Example:**
```bash
mshowfat --help
```

**Output (sample):**
```text
Usage/help information for `mshowfat` (illustrative; exact output varies by distribution/version).
```

### 45. `mtype`
**संक्षिप्त जानकारी:** MS-DOS file को सामग्री terminal मा देखाउँछ।

**Example:**
```bash
mtype --help
```

**Output (sample):**
```text
Usage/help information for `mtype` (illustrative; exact output varies by distribution/version).
```

### 46. `mattrib`
**संक्षिप्त जानकारी:** MS-DOS file attributes परिवर्तन गर्छ।

**Example:**
```bash
mattrib --help
```

**Output (sample):**
```text
Usage/help information for `mattrib` (illustrative; exact output varies by distribution/version).
```

### 47. `mmd`
**संक्षिप्त जानकारी:** MS-DOS file system मा नयाँ directory बनाउँछ।

**Example:**
```bash
mmd --help
```

**Output (sample):**
```text
Usage/help information for `mmd` (illustrative; exact output varies by distribution/version).
```

### 48. `mrd`
**संक्षिप्त जानकारी:** MS-DOS file system बाट directory हटाउँछ।

**Example:**
```bash
mrd --help
```

**Output (sample):**
```text
Usage/help information for `mrd` (illustrative; exact output varies by distribution/version).
```

### 49. `mzip`
**संक्षिप्त जानकारी:** Zip drive (MS-DOS) व्यवस्थापन गर्छ।

**Example:**
```bash
mzip --help
```

**Output (sample):**
```text
Usage/help information for `mzip` (illustrative; exact output varies by distribution/version).
```

### 50. `mtoolstest`
**संक्षिप्त जानकारी:** mtools को configuration जाँच गर्छ।

**Example:**
```bash
mtoolstest --help
```

**Output (sample):**
```text
Usage/help information for `mtoolstest` (illustrative; exact output varies by distribution/version).
```

### 51. `tee`
**संक्षिप्त जानकारी:** output screen मा देखाउँदै file मा पनि लेख्छ।

**Example:**
```bash
echo 'Hello' | tee hello.txt
```

**Output (sample):**
```text
Hello
```

### 52. `read`
**संक्षिप्त जानकारी:** shell मा user input (एक लाइन) पढ्छ (built-in)।

**Example:**
```bash
read name; echo "Hello $name"
```

**Output (sample):**
```text
Hello Prakash
```

---

<p align="right"><a href="#top">⬆️ सूचीमा फर्कने</a></p>

</details>

---

<a id="cat-53-96"></a>
<details>
<summary><h2 style="display:inline;">📝 Text Processing and Editing</h2> &nbsp; <em>Commands 53–96 (44 commands)</em></summary>

### 53. `grep`
**संक्षिप्त जानकारी:** file वा command output भित्र चाहिएको text खोज्छ।

**Example:**
```bash
grep 'error' app.log
```

**Output (sample):**
```text
2026-08-21 error: connection failed
```

### 54. `sed`
**संक्षिप्त जानकारी:** text खोजेर परिवर्तन, हटाउने वा replace गर्ने काम गर्छ।

**Example:**
```bash
sed 's/Linux/Ubuntu/g' file.txt
```

**Output (sample):**
```text
Ubuntu is powerful.
```

### 55. `awk`
**संक्षिप्त जानकारी:** text/data लाई field अनुसार पढेर processing गर्न प्रयोग हुन्छ।

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
**संक्षिप्त जानकारी:** line बाट आवश्यक column वा character निकाल्छ।

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
**संक्षिप्त जानकारी:** धेरै file का lines लाई एउटै output मा जोड्छ।

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
**संक्षिप्त जानकारी:** text का lines लाई क्रमबद्ध गर्छ।

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
**संक्षिप्त जानकारी:** लगातार दोहोरिएका lines हटाउँछ।

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
**संक्षिप्त जानकारी:** characters लाई परिवर्तन वा रूपान्तरण गर्छ।

**Example:**
```bash
echo 'hello' | tr 'a-z' 'A-Z'
```

**Output (sample):**
```text
HELLO
```

### 61. `head`
**संक्षिप्त जानकारी:** file को सुरुका केही lines देखाउँछ।

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
**संक्षिप्त जानकारी:** file को अन्तिम केही lines देखाउँछ।

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
**संक्षिप्त जानकारी:** line, word र character को संख्या गन्छ।

**Example:**
```bash
wc -l file.txt
```

**Output (sample):**
```text
10 file.txt
```

### 64. `diff`
**संक्षिप्त जानकारी:** दुई file बीचको फरक देखाउँछ।

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
**संक्षिप्त जानकारी:** diff file प्रयोग गरी original file मा परिवर्तन लागू गर्छ।

**Example:**
```bash
patch < changes.patch
```

**Output (sample):**
```text
patching file file.txt
```

### 66. `split`
**संक्षिप्त जानकारी:** ठूलो file लाई साना टुक्रामा विभाजन गर्छ।

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
**संक्षिप्त जानकारी:** common field को आधारमा दुई sorted files जोड्छ।

**Example:**
```bash
join users.txt departments.txt
```

**Output (sample):**
```text
101 Alice IT
```

### 68. `fmt`
**संक्षिप्त जानकारी:** text लाई तोकिएको width मा सफा गरी format गर्छ।

**Example:**
```bash
fmt -w 40 notes.txt
```

**Output (sample):**
```text
Wrapped text output ...
```

### 69. `fold`
**संक्षिप्त जानकारी:** लामो लाइनहरूलाई तोकिएको width मा wrap गर्छ।

**Example:**
```bash
fold -w 20 file.txt
```

**Output (sample):**
```text
Long line wrapped at 20 columns.
```

### 70. `expand`
**संक्षिप्त जानकारी:** tabs लाई spaces मा परिवर्तन गर्छ।

**Example:**
```bash
expand -t 4 file.txt
```

**Output (sample):**
```text
Tabs converted to spaces.
```

### 71. `col`
**संक्षिप्त जानकारी:** terminal control characters (जस्तै backspace) filter गर्छ।

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
**संक्षिप्त जानकारी:** निर्दिष्ट column range हटाउँछ।

**Example:**
```bash
printf 'abcdef\n' | colrm 3 4
```

**Output (sample):**
```text
abef
```

### 73. `comm`
**संक्षिप्त जानकारी:** दुई sorted files बीच common/unique लाइनहरू तुलना गर्छ।

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
**संक्षिप्त जानकारी:** context (pattern) अनुसार file विभाजन गर्छ।

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
**संक्षिप्त जानकारी:** text file मा spelling जाँच गर्छ (interactive)।

**Example:**
```bash
ispell --help
```

**Output (sample):**
```text
Usage/help information for `ispell` (illustrative; exact output varies by distribution/version).
```

### 76. `spell`
**संक्षिप्त जानकारी:** file मा हिज्जे (spelling) त्रुटि खोज्छ।

**Example:**
```bash
spell --help
```

**Output (sample):**
```text
Usage/help information for `spell` (illustrative; exact output varies by distribution/version).
```

### 77. `diffstat`
**संक्षिप्त जानकारी:** diff output को सारांश (statistics) देखाउँछ।

**Example:**
```bash
diffstat --help
```

**Output (sample):**
```text
Usage/help information for `diffstat` (illustrative; exact output varies by distribution/version).
```

### 78. `expr`
**संक्षिप्त जानकारी:** shell मा गणितीय/logical expression मूल्याङ्कन गर्छ।

**Example:**
```bash
expr 10 + 5
```

**Output (sample):**
```text
15
```

### 79. `aspell`
**संक्षिप्त जानकारी:** अर्को spell-checker, spelling त्रुटि पत्ता लगाउँछ।

**Example:**
```bash
aspell check notes.txt
```

**Output (sample):**
```text
Interactive spell checker opens.
```

### 80. `emacs`
**संक्षिप्त जानकारी:** शक्तिशाली, extensible text editor।

**Example:**
```bash
emacs --help
```

**Output (sample):**
```text
Usage/help information for `emacs` (illustrative; exact output varies by distribution/version).
```

### 81. `gawk`
**संक्षिप्त जानकारी:** GNU AWK, pattern scanning र text processing language।

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
**संक्षिप्त जानकारी:** C source code लाई सफा गरी format गर्छ।

**Example:**
```bash
indent --help
```

**Output (sample):**
```text
Usage/help information for `indent` (illustrative; exact output varies by distribution/version).
```

### 83. `sdiff`
**संक्षिप्त जानकारी:** दुई files लाई side-by-side तुलना गर्छ।

**Example:**
```bash
sdiff file1.txt file2.txt
```

**Output (sample):**
```text
same line              same line
```

### 84. `tac`
**संक्षिप्त जानकारी:** file को लाइनहरूलाई उल्टो क्रममा देखाउँछ (cat उल्टो)।

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
**संक्षिप्त जानकारी:** spaces लाई tabs मा परिवर्तन गर्छ।

**Example:**
```bash
unexpand -a file.txt
```

**Output (sample):**
```text
Spaces converted to tabs.
```

### 86. `unix2dos`
**संक्षिप्त जानकारी:** Unix line ending (LF) लाई DOS format (CRLF) मा परिवर्तन गर्छ।

**Example:**
```bash
unix2dos file.txt
```

**Output (sample):**
```text
unix2dos: converting file file.txt to DOS format...
```

### 87. `vi`
**संक्षिप्त जानकारी:** classic modal text editor।

**Example:**
```bash
vi notes.txt
```

**Output (sample):**
```text
Interactive editor opens.
```

### 88. `ed`
**संक्षिप्त जानकारी:** line-based, सबैभन्दा पुरानो Unix text editor।

**Example:**
```bash
ed --help
```

**Output (sample):**
```text
Usage/help information for `ed` (illustrative; exact output varies by distribution/version).
```

### 89. `egrep`
**संक्षिप्त जानकारी:** extended regular expressions प्रयोग गरी grep गर्छ (grep -E)।

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
**संक्षिप्त जानकारी:** vi को line-editing mode; script-driven editing।

**Example:**
```bash
ex --help
```

**Output (sample):**
```text
Usage/help information for `ex` (illustrative; exact output varies by distribution/version).
```

### 91. `fgrep`
**संक्षिप्त जानकारी:** fixed string (regex बिना) खोज्ने grep (grep -F)।

**Example:**
```bash
fgrep 'hello.world' file.txt
```

**Output (sample):**
```text
hello.world
```

### 92. `jed`
**संक्षिप्त जानकारी:** programmer-friendly text editor।

**Example:**
```bash
jed --help
```

**Output (sample):**
```text
Usage/help information for `jed` (illustrative; exact output varies by distribution/version).
```

### 93. `joe`
**संक्षिप्त जानकारी:** Joe's Own Editor, सरल text editor।

**Example:**
```bash
joe --help
```

**Output (sample):**
```text
Usage/help information for `joe` (illustrative; exact output varies by distribution/version).
```

### 94. `look`
**संक्षिप्त जानकारी:** dictionary/sorted file बाट prefix मिल्ने शब्द खोज्छ।

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
**संक्षिप्त जानकारी:** सरल, beginner-friendly text editor (nano को पूर्वज)।

**Example:**
```bash
pico --help
```

**Output (sample):**
```text
Usage/help information for `pico` (illustrative; exact output varies by distribution/version).
```

### 96. `column`
**संक्षिप्त जानकारी:** text लाई columns मा राम्रोसँग format गर्छ।

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

<p align="right"><a href="#top">⬆️ सूचीमा फर्कने</a></p>

</details>

---

<a id="cat-97-145"></a>
<details>
<summary><h2 style="display:inline;">📊 System Monitoring and Management</h2> &nbsp; <em>Commands 97–145 (49 commands)</em></summary>

### 97. `top`
**संक्षिप्त जानकारी:** CPU, memory र process को live अवस्था देखाउँछ।

**Example:**
```bash
top
```

**Output (sample):**
```text
Interactive process monitor opens.
```

### 98. `ps`
**संक्षिप्त जानकारी:** चलिरहेका process हरूको विवरण देखाउँछ।

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
**संक्षिप्त जानकारी:** RAM र swap memory को प्रयोग देखाउँछ।

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
**संक्षिप्त जानकारी:** Linux kernel तथा system सम्बन्धी जानकारी देखाउँछ।

**Example:**
```bash
uname -a
```

**Output (sample):**
```text
Linux host 6.x.x-generic x86_64 GNU/Linux
```

### 101. `uptime`
**संक्षिप्त जानकारी:** system कति समयदेखि चलिरहेको छ र load कति छ देखाउँछ।

**Example:**
```bash
uptime
```

**Output (sample):**
```text
11:57:00 up 3 days, 2:10, 1 user, load average: 0.10, 0.08, 0.05
```

### 102. `lsof`
**संक्षिप्त जानकारी:** कुन process ले कुन file वा network resource प्रयोग गरिरहेको छ देखाउँछ।

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
**संक्षिप्त जानकारी:** virtual memory, process, र CPU statistics देखाउँछ।

**Example:**
```bash
vmstat 1 2
```

**Output (sample):**
```text
procs ... memory ... swap ... io ... cpu ...
```

### 104. `iostat`
**संक्षिप्त जानकारी:** CPU र disk I/O statistics देखाउँछ।

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
**संक्षिप्त जानकारी:** kernel बाट आएका system/hardware messages देखाउँछ।

**Example:**
```bash
dmesg | tail -n 3
```

**Output (sample):**
```text
[...] kernel: device event ...
```

### 106. `htop`
**संक्षिप्त जानकारी:** process monitoring का लागि interactive interface दिन्छ।

**Example:**
```bash
htop
```

**Output (sample):**
```text
Interactive process monitor opens.
```

### 107. `lshw`
**संक्षिप्त जानकारी:** hardware को विस्तृत जानकारी देखाउँछ।

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
**संक्षिप्त जानकारी:** USB devices को जानकारी देखाउँछ।

**Example:**
```bash
lsusb
```

**Output (sample):**
```text
Bus 001 Device 002: ID 1234:5678 USB Device
```

### 109. `lsblk`
**संक्षिप्त जानकारी:** disk र partition को संरचना देखाउँछ।

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
**संक्षिप्त जानकारी:** प्रत्येक processor/core को उपयोग तथ्याङ्क देखाउँछ।

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
**संक्षिप्त जानकारी:** प्रोग्रामको नामबाट running process ID (PID) पत्ता लगाउँछ।

**Example:**
```bash
pidof sshd
```

**Output (sample):**
```text
812 790
```

### 112. `sar`
**संक्षिप्त जानकारी:** system activity (CPU, memory, I/O) को historical तथ्याङ्क संकलन/देखाउँछ।

**Example:**
```bash
sar --help
```

**Output (sample):**
```text
Usage/help information for `sar` (illustrative; exact output varies by distribution/version).
```

### 113. `procinfo`
**संक्षिप्त जानकारी:** /proc बाट system information देखाउने legacy tool।

**Example:**
```bash
procinfo --help
```

**Output (sample):**
```text
Usage/help information for `procinfo` (illustrative; exact output varies by distribution/version).
```

### 114. `pstree`
**संक्षिप्त जानकारी:** processes लाई tree (parent-child) रूपमा देखाउँछ।

**Example:**
```bash
pstree -p | head
```

**Output (sample):**
```text
systemd(1)-+-sshd(790)---bash(812)
```

### 115. `tload`
**संक्षिप्त जानकारी:** system load average को ASCII graphical प्रदर्शन देखाउँछ।

**Example:**
```bash
tload --help
```

**Output (sample):**
```text
Usage/help information for `tload` (illustrative; exact output varies by distribution/version).
```

### 116. `logrotate`
**संक्षिप्त जानकारी:** log files लाई automatically rotate, compress र delete गर्छ।

**Example:**
```bash
logrotate --help
```

**Output (sample):**
```text
Usage/help information for `logrotate` (illustrative; exact output varies by distribution/version).
```

### 117. `watch`
**संक्षिप्त जानकारी:** निर्दिष्ट command लाई नियमित अन्तरालमा दोहोर्‍याएर चलाउँछ।

**Example:**
```bash
watch -n 2 'df -h /'
```

**Output (sample):**
```text
Repeated command output every 2 seconds.
```

### 118. `time`
**संक्षिप्त जानकारी:** कुनै command execute हुन लागेको समय मापन गर्छ।

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
**संक्षिप्त जानकारी:** हालको system date र time देखाउँछ।

**Example:**
```bash
date '+%Y-%m-%d'
```

**Output (sample):**
```text
2026-08-21
```

### 120. `cal`
**संक्षिप्त जानकारी:** महिना/वर्षको calendar देखाउँछ।

**Example:**
```bash
cal 2026
```

**Output (sample):**
```text
2026 calendar displayed.
```

### 121. `arch`
**संक्षिप्त जानकारी:** system को hardware architecture (जस्तै x86_64) देखाउँछ।

**Example:**
```bash
arch
```

**Output (sample):**
```text
x86_64
```

### 122. `dmidecode`
**संक्षिप्त जानकारी:** BIOS/hardware DMI table बाट hardware जानकारी देखाउँछ।

**Example:**
```bash
dmidecode --help
```

**Output (sample):**
```text
Usage/help information for `dmidecode` (illustrative; exact output varies by distribution/version).
```

### 123. `dstat`
**संक्षिप्त जानकारी:** CPU, disk, network लगायत system resources को combined real-time तथ्याङ्क देखाउँछ।

**Example:**
```bash
dstat --help
```

**Output (sample):**
```text
Usage/help information for `dstat` (illustrative; exact output varies by distribution/version).
```

### 124. `iotop`
**संक्षिप्त जानकारी:** प्रत्येक process ले प्रयोग गरेको disk I/O देखाउँछ (top जस्तै)।

**Example:**
```bash
iotop --help
```

**Output (sample):**
```text
Usage/help information for `iotop` (illustrative; exact output varies by distribution/version).
```

### 125. `journalctl`
**संक्षिप्त जानकारी:** systemd का system र service logs हेर्न प्रयोग हुन्छ।

**Example:**
```bash
journalctl -n 5
```

**Output (sample):**
```text
Recent systemd journal entries ...
```

### 126. `pmap`
**संक्षिप्त जानकारी:** process को memory map देखाउँछ।

**Example:**
```bash
pmap --help
```

**Output (sample):**
```text
Usage/help information for `pmap` (illustrative; exact output varies by distribution/version).
```

### 127. `adduser`
**संक्षिप्त जानकारी:** नयाँ user सजिलो तरिकाले सिर्जना गर्छ।

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
**संक्षिप्त जानकारी:** user को password aging/expiry policy परिवर्तन गर्छ।

**Example:**
```bash
chage --help
```

**Output (sample):**
```text
Usage/help information for `chage` (illustrative; exact output varies by distribution/version).
```

### 129. `chpasswd`
**संक्षिप्त जानकारी:** file बाट batch मा धेरै users को password परिवर्तन गर्छ।

**Example:**
```bash
chpasswd --help
```

**Output (sample):**
```text
Usage/help information for `chpasswd` (illustrative; exact output varies by distribution/version).
```

### 130. `grpck`
**संक्षिप्त जानकारी:** /etc/group र /etc/gshadow फाइलको integrity जाँच गर्छ।

**Example:**
```bash
grpck --help
```

**Output (sample):**
```text
Usage/help information for `grpck` (illustrative; exact output varies by distribution/version).
```

### 131. `vlock`
**संक्षिप्त जानकारी:** virtual console लाई lock गर्छ।

**Example:**
```bash
vlock --help
```

**Output (sample):**
```text
Usage/help information for `vlock` (illustrative; exact output varies by distribution/version).
```

### 132. `logout`
**संक्षिप्त जानकारी:** हालको login shell session बाट logout गर्छ (built-in)।

**Example:**
```bash
help logout
```

**Output (sample):**
```text
Built-in shell command 'logout'; output/behavior depends on the shell.
```

### 133. `login`
**संक्षिप्त जानकारी:** system मा login गर्न प्रयोग हुने program।

**Example:**
```bash
login --help
```

**Output (sample):**
```text
Usage/help information for `login` (illustrative; exact output varies by distribution/version).
```

### 134. `logname`
**संक्षिप्त जानकारी:** हाल login गरेको user को नाम देखाउँछ।

**Example:**
```bash
logname --help
```

**Output (sample):**
```text
Usage/help information for `logname` (illustrative; exact output varies by distribution/version).
```

### 135. `rlogin`
**संक्षिप्त जानकारी:** remote host मा login गर्छ (legacy, असुरक्षित)।

**Example:**
```bash
rlogin --help
```

**Output (sample):**
```text
Usage/help information for `rlogin` (illustrative; exact output varies by distribution/version).
```

### 136. `rsh`
**संक्षिप्त जानकारी:** remote host मा command चलाउँछ (legacy, असुरक्षित)।

**Example:**
```bash
rsh --help
```

**Output (sample):**
```text
Usage/help information for `rsh` (illustrative; exact output varies by distribution/version).
```

### 137. `sliplogin`
**संक्षिप्त जानकारी:** SLIP connection सेटअप गर्छ (legacy networking)।

**Example:**
```bash
sliplogin --help
```

**Output (sample):**
```text
Usage/help information for `sliplogin` (illustrative; exact output varies by distribution/version).
```

### 138. `swatch`
**संक्षिप्त जानकारी:** log files लाई real-time monitor गरी pattern अनुसार alert दिन्छ।

**Example:**
```bash
swatch --help
```

**Output (sample):**
```text
Usage/help information for `swatch` (illustrative; exact output varies by distribution/version).
```

### 139. `w`
**संक्षिप्त जानकारी:** हाल login भएका users र उनीहरूको activity देखाउँछ।

**Example:**
```bash
w --help
```

**Output (sample):**
```text
Usage/help information for `w` (illustrative; exact output varies by distribution/version).
```

### 140. `rwho`
**संक्षिप्त जानकारी:** network मा login भएका users देखाउँछ (legacy)।

**Example:**
```bash
rwho --help
```

**Output (sample):**
```text
Usage/help information for `rwho` (illustrative; exact output varies by distribution/version).
```

### 141. `shutdown`
**संक्षिप्त जानकारी:** system shutdown/restart schedule गर्न प्रयोग हुन्छ।

**Example:**
```bash
shutdown --help
```

**Output (sample):**
```text
Usage/help information for `shutdown` (illustrative; exact options vary by distribution).
```

### 142. `halt`
**संक्षिप्त जानकारी:** system लाई तुरुन्त बन्द (shutdown) गर्छ।

**Example:**
```bash
halt --help
```

**Output (sample):**
```text
Usage/help information for `halt` (illustrative; exact options vary by distribution).
```

### 143. `reboot`
**संक्षिप्त जानकारी:** system restart गर्छ।

**Example:**
```bash
reboot --help
```

**Output (sample):**
```text
Usage/help information for `reboot` (illustrative; exact options vary by distribution).
```

### 144. `exit`
**संक्षिप्त जानकारी:** हालको shell वा script बाट बाहिरिन्छ।

**Example:**
```bash
help exit
```

**Output (sample):**
```text
Built-in shell command 'exit'; output/behavior depends on the shell.
```

### 145. `suspend`
**संक्षिप्त जानकारी:** shell लाई suspend (pause) गर्छ।

**Example:**
```bash
suspend --help
```

**Output (sample):**
```text
Usage/help information for `suspend` (illustrative; exact output varies by distribution/version).
```

---

<p align="right"><a href="#top">⬆️ सूचीमा फर्कने</a></p>

</details>

---

<a id="cat-146-175"></a>
<details>
<summary><h2 style="display:inline;">👤 User and Permission Management</h2> &nbsp; <em>Commands 146–175 (30 commands)</em></summary>

### 146. `useradd`
**संक्षिप्त जानकारी:** नयाँ user account सिर्जना गर्छ।

**Example:**
```bash
sudo useradd -m demo
```

**Output (sample):**
```text
No output on success.
```

### 147. `userdel`
**संक्षिप्त जानकारी:** user account हटाउँछ।

**Example:**
```bash
sudo userdel -r demo
```

**Output (sample):**
```text
No output on success.
```

### 148. `usermod`
**संक्षिप्त जानकारी:** अवस्थित user को account settings परिवर्तन गर्छ।

**Example:**
```bash
sudo usermod -aG sudo demo
```

**Output (sample):**
```text
No output on success.
```

### 149. `groupadd`
**संक्षिप्त जानकारी:** नयाँ group बनाउँछ।

**Example:**
```bash
sudo groupadd developers
```

**Output (sample):**
```text
No output on success.
```

### 150. `groupdel`
**संक्षिप्त जानकारी:** group हटाउँछ।

**Example:**
```bash
sudo groupdel developers
```

**Output (sample):**
```text
No output on success.
```

### 151. `groupmod`
**संक्षिप्त जानकारी:** group को configuration वा नाम परिवर्तन गर्छ।

**Example:**
```bash
sudo groupmod -n dev developers
```

**Output (sample):**
```text
No output on success.
```

### 152. `passwd`
**संक्षिप्त जानकारी:** user को password परिवर्तन गर्न प्रयोग हुन्छ।

**Example:**
```bash
passwd
```

**Output (sample):**
```text
passwd: password updated successfully
```

### 153. `chown`
**संक्षिप्त जानकारी:** file वा directory को owner/group परिवर्तन गर्छ।

**Example:**
```bash
sudo chown user:user file.txt
```

**Output (sample):**
```text
No output on success.
```

### 154. `chmod`
**संक्षिप्त जानकारी:** file वा directory को permission परिवर्तन गर्छ।

**Example:**
```bash
chmod 644 file.txt
```

**Output (sample):**
```text
No output on success.
```

### 155. `chgrp`
**संक्षिप्त जानकारी:** file वा directory को group परिवर्तन गर्छ।

**Example:**
```bash
sudo chgrp developers file.txt
```

**Output (sample):**
```text
No output on success.
```

### 156. `umask`
**संक्षिप्त जानकारी:** नयाँ file/folder को default permission mask देखाउँछ वा सेट गर्छ।

**Example:**
```bash
umask
```

**Output (sample):**
```text
0022
```

### 157. `sudo`
**संक्षिप्त जानकारी:** administrator अधिकारमा command चलाउन प्रयोग हुन्छ।

**Example:**
```bash
sudo -v
```

**Output (sample):**
```text
No output when credentials are accepted.
```

### 158. `su`
**संक्षिप्त जानकारी:** अर्को user को account मा switch गर्न प्रयोग हुन्छ।

**Example:**
```bash
su - demo
```

**Output (sample):**
```text
Interactive login shell for demo starts.
```

### 159. `id`
**संक्षिप्त जानकारी:** हालको user को UID, GID र groups देखाउँछ।

**Example:**
```bash
id
```

**Output (sample):**
```text
uid=1000(user) gid=1000(user) groups=1000(user),27(sudo)
```

### 160. `who`
**संक्षिप्त जानकारी:** हाल system मा login भएका users देखाउँछ।

**Example:**
```bash
who
```

**Output (sample):**
```text
user  tty2  2026-08-21 10:30
```

### 161. `whoami`
**संक्षिप्त जानकारी:** हाल login भएको user को नाम देखाउँछ।

**Example:**
```bash
whoami
```

**Output (sample):**
```text
user
```

### 162. `chfn`
**संक्षिप्त जानकारी:** user को finger जानकारी (पूरा नाम आदि) परिवर्तन गर्छ।

**Example:**
```bash
chfn --help
```

**Output (sample):**
```text
Usage/help information for `chfn` (illustrative; exact output varies by distribution/version).
```

### 163. `chsh`
**संक्षिप्त जानकारी:** user को default login shell परिवर्तन गर्छ।

**Example:**
```bash
chsh --help
```

**Output (sample):**
```text
Usage/help information for `chsh` (illustrative; exact output varies by distribution/version).
```

### 164. `newgrp`
**संक्षिप्त जानकारी:** हालको shell मा प्रभावकारी group परिवर्तन गर्छ।

**Example:**
```bash
newgrp developers
```

**Output (sample):**
```text
New shell starts with developers as the effective group.
```

### 165. `last`
**संक्षिप्त जानकारी:** अघिल्ला successful login हरूको इतिहास देखाउँछ।

**Example:**
```bash
last -n 2
```

**Output (sample):**
```text
user tty2 ... still logged in
```

### 166. `lastb`
**संक्षिप्त जानकारी:** असफल login प्रयासहरूको सूची देखाउँछ।

**Example:**
```bash
sudo lastb -n 2
```

**Output (sample):**
```text
Failed login records ...
```

### 167. `finger`
**संक्षिप्त जानकारी:** user बारे विस्तृत जानकारी देखाउँछ।

**Example:**
```bash
finger --help
```

**Output (sample):**
```text
Usage/help information for `finger` (illustrative; exact output varies by distribution/version).
```

### 168. `groups`
**संक्षिप्त जानकारी:** हालको user कुन-कुन group मा छ देखाउँछ।

**Example:**
```bash
groups
```

**Output (sample):**
```text
user sudo developers
```

### 169. `gpasswd`
**संक्षिप्त जानकारी:** group को password र सदस्यता व्यवस्थापन गर्छ।

**Example:**
```bash
gpasswd --help
```

**Output (sample):**
```text
Usage/help information for `gpasswd` (illustrative; exact output varies by distribution/version).
```

### 170. `pwconv`
**संक्षिप्त जानकारी:** /etc/passwd बाट shadow password मा convert गर्छ।

**Example:**
```bash
pwconv --help
```

**Output (sample):**
```text
Usage/help information for `pwconv` (illustrative; exact output varies by distribution/version).
```

### 171. `pwunconv`
**संक्षिप्त जानकारी:** shadow password लाई फिर्ता /etc/passwd मा convert गर्छ।

**Example:**
```bash
pwunconv --help
```

**Output (sample):**
```text
Usage/help information for `pwunconv` (illustrative; exact output varies by distribution/version).
```

### 172. `grpconv`
**संक्षिप्त जानकारी:** group password लाई shadow group मा convert गर्छ।

**Example:**
```bash
grpconv --help
```

**Output (sample):**
```text
Usage/help information for `grpconv` (illustrative; exact output varies by distribution/version).
```

### 173. `grpunconv`
**संक्षिप्त जानकारी:** shadow group लाई फिर्ता /etc/group मा convert गर्छ।

**Example:**
```bash
grpunconv --help
```

**Output (sample):**
```text
Usage/help information for `grpunconv` (illustrative; exact output varies by distribution/version).
```

### 174. `newaliases`
**संक्षिप्त जानकारी:** mail aliases database अद्यावधिक गर्छ।

**Example:**
```bash
newaliases --help
```

**Output (sample):**
```text
Usage/help information for `newaliases` (illustrative; exact output varies by distribution/version).
```

### 175. `users`
**संक्षिप्त जानकारी:** हाल login भएका सबै users को नाम देखाउँछ।

**Example:**
```bash
users --help
```

**Output (sample):**
```text
Usage/help information for `users` (illustrative; exact output varies by distribution/version).
```

---

<p align="right"><a href="#top">⬆️ सूचीमा फर्कने</a></p>

</details>

---

<a id="cat-176-243"></a>
<details>
<summary><h2 style="display:inline;">🌐 Networking and Communication</h2> &nbsp; <em>Commands 176–243 (68 commands)</em></summary>

### 176. `ping`
**संक्षिप्त जानकारी:** network host reachable छ कि छैन जाँच गर्छ।

**Example:**
```bash
ping -c 4 8.8.8.8
```

**Output (sample):**
```text
4 packets transmitted, 4 received, 0% packet loss
```

### 177. `netstat`
**संक्षिप्त जानकारी:** network connections, routing table, र port statistics देखाउँछ (legacy; ip/ss बाट replace भएको)।

**Example:**
```bash
ss -tuln  # modern replacement for netstat
```

**Output (sample):**
```text
LISTEN ... :22 ...
```

### 178. `ifconfig`
**संक्षिप्त जानकारी:** network interfaces configure/देखाउने पुरानो command (ip को सट्टा प्रयोग हुन्छ)।

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
**संक्षिप्त जानकारी:** remote Linux server मा सुरक्षित रूपमा login गर्न प्रयोग हुन्छ।

**Example:**
```bash
ssh user@server.example.com
```

**Output (sample):**
```text
user@server.example.com's password:
```

### 180. `scp`
**संक्षिप्त जानकारी:** SSH प्रयोग गरेर file सुरक्षित रूपमा copy गर्छ।

**Example:**
```bash
scp file.txt user@server:/tmp/
```

**Output (sample):**
```text
file.txt 100% 12B ...
```

### 181. `ftp`
**संक्षिप्त जानकारी:** FTP server सँग file transfer गर्न प्रयोग हुन्छ।

**Example:**
```bash
ftp ftp.example.com
```

**Output (sample):**
```text
Connected to ftp.example.com.
```

### 182. `wget`
**संक्षिप्त जानकारी:** Internet बाट file download गर्न प्रयोग हुन्छ।

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
**संक्षिप्त जानकारी:** URL मार्फत data request/transfer गर्न प्रयोग हुन्छ।

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
**संक्षिप्त जानकारी:** network packet कुन-कुन route हुँदै गइरहेको छ देखाउँछ।

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
**संक्षिप्त जानकारी:** remote host मा unencrypted रूपमा connect गर्छ (legacy)।

**Example:**
```bash
telnet example.com 80
```

**Output (sample):**
```text
Connected to example.com.
```

### 186. `nslookup`
**संक्षिप्त जानकारी:** DNS बाट domain को जानकारी खोज्छ।

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
**संक्षिप्त जानकारी:** DNS query र record को विस्तृत जानकारी निकाल्छ।

**Example:**
```bash
dig example.com A +short
```

**Output (sample):**
```text
93.184.216.34
```

### 188. `route`
**संक्षिप्त जानकारी:** network routing table हेर्न वा व्यवस्थापन गर्न प्रयोग हुन्छ।

**Example:**
```bash
ip route
```

**Output (sample):**
```text
default via 192.168.1.1 dev eth0
```

### 189. `ip`
**संक्षिप्त जानकारी:** network interface, IP address र routing व्यवस्थापन गर्छ।

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
**संक्षिप्त जानकारी:** network host र खुला ports/services जाँच गर्न प्रयोग हुन्छ।

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
**संक्षिप्त जानकारी:** network interface लाई सक्रिय (up) गर्छ।

**Example:**
```bash
ifup --help
```

**Output (sample):**
```text
Usage/help information for `ifup` (illustrative; exact output varies by distribution/version).
```

### 192. `ifdown`
**संक्षिप्त जानकारी:** network interface लाई निष्क्रिय (down) गर्छ।

**Example:**
```bash
ifdown --help
```

**Output (sample):**
```text
Usage/help information for `ifdown` (illustrative; exact output varies by distribution/version).
```

### 193. `hostname`
**संक्षिप्त जानकारी:** system को hostname देखाउँछ।

**Example:**
```bash
hostname
```

**Output (sample):**
```text
linux-server
```

### 194. `hostnamectl`
**संक्षिप्त जानकारी:** system hostname र सम्बन्धित system information व्यवस्थापन गर्छ।

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
**संक्षिप्त जानकारी:** ARP table (IP-to-MAC mapping) देखाउँछ/परिवर्तन गर्छ।

**Example:**
```bash
ip neigh
```

**Output (sample):**
```text
192.168.1.1 dev eth0 lladdr aa:bb:cc:dd:ee:ff REACHABLE
```

### 196. `netcat`
**संक्षिप्त जानकारी:** network connection परीक्षण र data transfer का लागि प्रयोग हुन्छ।

**Example:**
```bash
nc -vz example.com 80
```

**Output (sample):**
```text
Connection to example.com 80 port [tcp/http] succeeded!
```

### 197. `nmcli`
**संक्षिप्त जानकारी:** NetworkManager मार्फत network configuration व्यवस्थापन गर्छ।

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
**संक्षिप्त जानकारी:** network packets capture र analyze गर्न प्रयोग हुन्छ।

**Example:**
```bash
sudo tcpdump -i eth0 -c 3
```

**Output (sample):**
```text
IP 192.168.1.2.12345 > 8.8.8.8.53: ...
```

### 199. `ss`
**संक्षिप्त जानकारी:** network connection र listening ports देखाउँछ।

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
**संक्षिप्त जानकारी:** wireless network interface configure गर्छ (legacy)।

**Example:**
```bash
iwconfig --help
```

**Output (sample):**
```text
Usage/help information for `iwconfig` (illustrative; exact output varies by distribution/version).
```

### 201. `ethtool`
**संक्षिप्त जानकारी:** Ethernet interface को speed, duplex आदि जानकारी/setting हेर्छ।

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
**संक्षिप्त जानकारी:** Samba/SMB (Windows) file share मा FTP-जस्तो access दिन्छ।

**Example:**
```bash
smbclient -L //server -U user
```

**Output (sample):**
```text
Sharename  Type  Comment
```

### 203. `smbstatus`
**संक्षिप्त जानकारी:** Samba server सँग हाल जोडिएका connections देखाउँछ।

**Example:**
```bash
smbstatus --help
```

**Output (sample):**
```text
Usage/help information for `smbstatus` (illustrative; exact output varies by distribution/version).
```

### 204. `mailq`
**संक्षिप्त जानकारी:** पठाउन बाँकी mail हरूको queue देखाउँछ।

**Example:**
```bash
mailq
```

**Output (sample):**
```text
Mail queue is empty
```

### 205. `host`
**संक्षिप्त जानकारी:** domain र DNS सम्बन्धी जानकारी छिटो देखाउँछ।

**Example:**
```bash
host example.com
```

**Output (sample):**
```text
example.com has address 93.184.216.34
```

### 206. `arpwatch`
**संक्षिप्त जानकारी:** network मा MAC-IP address परिवर्तनहरू monitor गर्छ।

**Example:**
```bash
arpwatch --help
```

**Output (sample):**
```text
Usage/help information for `arpwatch` (illustrative; exact output varies by distribution/version).
```

### 207. `iftop`
**संक्षिप्त जानकारी:** real-time network bandwidth usage देखाउँछ।

**Example:**
```bash
sudo iftop -i eth0
```

**Output (sample):**
```text
Interactive bandwidth monitor opens.
```

### 208. `iptables`
**संक्षिप्त जानकारी:** Linux firewall का packet filtering rules व्यवस्थापन गर्छ।

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
**संक्षिप्त जानकारी:** हालको iptables firewall rules लाई file मा save गर्छ।

**Example:**
```bash
iptables-save --help
```

**Output (sample):**
```text
Usage/help information for `iptables-save` (illustrative; exact output varies by distribution/version).
```

### 210. `tracepath`
**संक्षिप्त जानकारी:** destination सम्म जाने network path र MTU पत्ता लगाउँछ।

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
**संक्षिप्त जानकारी:** UUCP network मा जोडिएका systems को नाम देखाउँछ।

**Example:**
```bash
uuname --help
```

**Output (sample):**
```text
Usage/help information for `uuname` (illustrative; exact output varies by distribution/version).
```

### 212. `vnstat`
**संक्षिप्त जानकारी:** network traffic usage को historical तथ्याङ्क राख्छ।

**Example:**
```bash
vnstat --help
```

**Output (sample):**
```text
Usage/help information for `vnstat` (illustrative; exact output varies by distribution/version).
```

### 213. `whois`
**संक्षिप्त जानकारी:** domain/IP registration सम्बन्धी सार्वजनिक जानकारी खोज्छ।

**Example:**
```bash
whois example.com
```

**Output (sample):**
```text
Domain Name: EXAMPLE.COM
```

### 214. `apachectl`
**संक्षिप्त जानकारी:** Apache web server control गर्ने (start/stop/restart) command।

**Example:**
```bash
apachectl --help
```

**Output (sample):**
```text
Usage/help information for `apachectl` (illustrative; exact output varies by distribution/version).
```

### 215. `httpd`
**संक्षिप्त जानकारी:** Apache HTTP server daemon।

**Example:**
```bash
httpd --help
```

**Output (sample):**
```text
Usage/help information for `httpd` (illustrative; exact output varies by distribution/version).
```

### 216. `nc(netcat)`
**संक्षिप्त जानकारी:** TCP/UDP connections पढ्ने/लेख्ने networking Swiss-army-knife tool।

**Example:**
```bash
nc(netcat) --help
```

**Output (sample):**
```text
Usage/help information for `nc(netcat)` (illustrative; exact output varies by distribution/version).
```

### 217. `lpr`
**संक्षिप्त जानकारी:** print job लाई printer queue मा पठाउँछ।

**Example:**
```bash
lpr --help
```

**Output (sample):**
```text
Usage/help information for `lpr` (illustrative; exact output varies by distribution/version).
```

### 218. `lpq`
**संक्षिप्त जानकारी:** printer queue मा रहेका jobs देखाउँछ।

**Example:**
```bash
lpq --help
```

**Output (sample):**
```text
Usage/help information for `lpq` (illustrative; exact output varies by distribution/version).
```

### 219. `lprm`
**संक्षिप्त जानकारी:** print queue बाट job हटाउँछ।

**Example:**
```bash
lprm --help
```

**Output (sample):**
```text
Usage/help information for `lprm` (illustrative; exact output varies by distribution/version).
```

### 220. `lpd`
**संक्षिप्त जानकारी:** line printer daemon (printing service)।

**Example:**
```bash
lpd --help
```

**Output (sample):**
```text
Usage/help information for `lpd` (illustrative; exact output varies by distribution/version).
```

### 221. `tftp`
**संक्षिप्त जानकारी:** Trivial FTP प्रयोग गरी सरल file transfer गर्छ।

**Example:**
```bash
tftp --help
```

**Output (sample):**
```text
Usage/help information for `tftp` (illustrative; exact output varies by distribution/version).
```

### 222. `ncftp`
**संक्षिप्त जानकारी:** सुधारिएको interface भएको FTP client।

**Example:**
```bash
ncftp --help
```

**Output (sample):**
```text
Usage/help information for `ncftp` (illustrative; exact output varies by distribution/version).
```

### 223. `ftpshut`
**संक्षिप्त जानकारी:** FTP server लाई निर्धारित समयमा बन्द गर्छ।

**Example:**
```bash
ftpshut --help
```

**Output (sample):**
```text
Usage/help information for `ftpshut` (illustrative; exact output varies by distribution/version).
```

### 224. `ftpwho`
**संक्षिप्त जानकारी:** FTP server मा जोडिएका users देखाउँछ।

**Example:**
```bash
ftpwho --help
```

**Output (sample):**
```text
Usage/help information for `ftpwho` (illustrative; exact output varies by distribution/version).
```

### 225. `ftpcount`
**संक्षिप्त जानकारी:** FTP server मा हाल जोडिएका users को संख्या देखाउँछ।

**Example:**
```bash
ftpcount --help
```

**Output (sample):**
```text
Usage/help information for `ftpcount` (illustrative; exact output varies by distribution/version).
```

### 226. `uuto`
**संक्षिप्त जानकारी:** UUCP प्रयोग गरी अर्को system मा file पठाउँछ।

**Example:**
```bash
uuto --help
```

**Output (sample):**
```text
Usage/help information for `uuto` (illustrative; exact output varies by distribution/version).
```

### 227. `uupick`
**संक्षिप्त जानकारी:** UUCP बाट प्राप्त files स्वीकार गर्छ।

**Example:**
```bash
uupick --help
```

**Output (sample):**
```text
Usage/help information for `uupick` (illustrative; exact output varies by distribution/version).
```

### 228. `uucico`
**संक्षिप्त जानकारी:** UUCP file transfer daemon।

**Example:**
```bash
uucico --help
```

**Output (sample):**
```text
Usage/help information for `uucico` (illustrative; exact output varies by distribution/version).
```

### 229. `uulog`
**संक्षिप्त जानकारी:** UUCP transfer logs देखाउँछ।

**Example:**
```bash
uulog --help
```

**Output (sample):**
```text
Usage/help information for `uulog` (illustrative; exact output varies by distribution/version).
```

### 230. `dip`
**संक्षिप्त जानकारी:** dial-up IP connection सेटअप गर्छ (legacy)।

**Example:**
```bash
dip --help
```

**Output (sample):**
```text
Usage/help information for `dip` (illustrative; exact output varies by distribution/version).
```

### 231. `minicom`
**संक्षिप्त जानकारी:** serial communication/modem terminal program।

**Example:**
```bash
minicom --help
```

**Output (sample):**
```text
Usage/help information for `minicom` (illustrative; exact output varies by distribution/version).
```

### 232. `mesg`
**संक्षिप्त जानकारी:** अरू users ले आफ्नो terminal मा message पठाउन पाउने/नपाउने control गर्छ।

**Example:**
```bash
mesg --help
```

**Output (sample):**
```text
Usage/help information for `mesg` (illustrative; exact output varies by distribution/version).
```

### 233. `wall`
**संक्षिप्त जानकारी:** सबै logged-in users लाई broadcast message पठाउँछ।

**Example:**
```bash
wall --help
```

**Output (sample):**
```text
Usage/help information for `wall` (illustrative; exact output varies by distribution/version).
```

### 234. `write`
**संक्षिप्त जानकारी:** अर्को user को terminal मा सिधै message पठाउँछ।

**Example:**
```bash
write --help
```

**Output (sample):**
```text
Usage/help information for `write` (illustrative; exact output varies by distribution/version).
```

### 235. `talk`
**संक्षिप्त जानकारी:** अर्को user सँग real-time interactive chat गर्छ (legacy)।

**Example:**
```bash
talk --help
```

**Output (sample):**
```text
Usage/help information for `talk` (illustrative; exact output varies by distribution/version).
```

### 236. `ytalk`
**संक्षिप्त जानकारी:** talk को बढी features भएको संस्करण (multi-user chat)।

**Example:**
```bash
ytalk --help
```

**Output (sample):**
```text
Usage/help information for `ytalk` (illustrative; exact output varies by distribution/version).
```

### 237. `smbd`
**संक्षिप्त जानकारी:** Samba SMB/CIFS file sharing server daemon।

**Example:**
```bash
smbd --help
```

**Output (sample):**
```text
Usage/help information for `smbd` (illustrative; exact output varies by distribution/version).
```

### 238. `testparm`
**संक्षिप्त जानकारी:** Samba को smb.conf configuration file जाँच गर्छ।

**Example:**
```bash
testparm --help
```

**Output (sample):**
```text
Usage/help information for `testparm` (illustrative; exact output varies by distribution/version).
```

### 239. `pppstats`
**संक्षिप्त जानकारी:** PPP connection को तथ्याङ्क देखाउँछ।

**Example:**
```bash
pppstats --help
```

**Output (sample):**
```text
Usage/help information for `pppstats` (illustrative; exact output varies by distribution/version).
```

### 240. `cu`
**संक्षिप्त जानकारी:** अर्को system सँग serial line मार्फत connect गर्छ (call up)।

**Example:**
```bash
cu --help
```

**Output (sample):**
```text
Usage/help information for `cu` (illustrative; exact output varies by distribution/version).
```

### 241. `getty`
**संक्षिप्त जानकारी:** terminal line मा login prompt सुरु गर्छ।

**Example:**
```bash
getty --help
```

**Output (sample):**
```text
Usage/help information for `getty` (illustrative; exact output varies by distribution/version).
```

### 242. `mingetty`
**संक्षिप्त जानकारी:** virtual console का लागि हल्का getty।

**Example:**
```bash
mingetty --help
```

**Output (sample):**
```text
Usage/help information for `mingetty` (illustrative; exact output varies by distribution/version).
```

### 243. `tty`
**संक्षिप्त जानकारी:** हालको terminal device को नाम देखाउँछ।

**Example:**
```bash
tty --help
```

**Output (sample):**
```text
Usage/help information for `tty` (illustrative; exact output varies by distribution/version).
```

---

<p align="right"><a href="#top">⬆️ सूचीमा फर्कने</a></p>

</details>

---

<a id="cat-244-286"></a>
<details>
<summary><h2 style="display:inline;">💽 Disk and File System Utilities</h2> &nbsp; <em>Commands 244–286 (43 commands)</em></summary>

### 244. `mount`
**संक्षिप्त जानकारी:** filesystem वा storage device लाई directory मा जोड्छ।

**Example:**
```bash
mount | head -n 2
```

**Output (sample):**
```text
/dev/sda1 on / type ext4 (rw,relatime)
```

### 245. `umount`
**संक्षिप्त जानकारी:** mounted filesystem लाई सुरक्षित रूपमा detach गर्छ।

**Example:**
```bash
sudo umount /mnt/usb
```

**Output (sample):**
```text
No output on success.
```

### 246. `fdisk`
**संक्षिप्त जानकारी:** disk partition हेर्न र व्यवस्थापन गर्न प्रयोग हुन्छ।

**Example:**
```bash
sudo fdisk -l
```

**Output (sample):**
```text
Disk /dev/sda: 100 GiB
```

### 247. `mkfs`
**संक्षिप्त जानकारी:** partition मा नयाँ filesystem बनाउन प्रयोग हुन्छ।

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
**संक्षिप्त जानकारी:** filesystem मा error जाँच तथा repair गर्न प्रयोग हुन्छ।

**Example:**
```bash
sudo fsck -n /dev/sdb1
```

**Output (sample):**
```text
clean, ... files, ... blocks
```

### 249. `dd`
**संक्षिप्त जानकारी:** raw data copy/backup वा disk image बनाउन प्रयोग हुने शक्तिशाली command हो।

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
**संक्षिप्त जानकारी:** ext2/ext3/ext4 file system जाँच र मर्मत गर्छ।

**Example:**
```bash
sudo e2fsck -n /dev/sdb1
```

**Output (sample):**
```text
clean, ...
```

### 251. `tune2fs`
**संक्षिप्त जानकारी:** ext file system का tunable parameters परिवर्तन गर्छ।

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
**संक्षिप्त जानकारी:** hard disk drive parameters हेर्ने/परिवर्तन गर्ने command।

**Example:**
```bash
sudo hdparm -Tt /dev/sda
```

**Output (sample):**
```text
Timing cached reads: ... MB/sec
```

### 253. `fdformat`
**संक्षिप्त जानकारी:** floppy disk लाई low-level format गर्छ।

**Example:**
```bash
fdformat --help
```

**Output (sample):**
```text
Usage/help information for `fdformat` (illustrative; exact output varies by distribution/version).
```

### 254. `parted`
**संक्षिप्त जानकारी:** disk partition सिर्जना तथा व्यवस्थापन गर्न प्रयोग हुन्छ।

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
**संक्षिप्त जानकारी:** block device को UUID र filesystem type देखाउँछ।

**Example:**
```bash
blkid /dev/sdb1
```

**Output (sample):**
```text
/dev/sdb1: UUID="..." TYPE="ext4"
```

### 256. `mkswap`
**संक्षिप्त जानकारी:** disk/file लाई swap area का रूपमा तयार गर्छ।

**Example:**
```bash
sudo mkswap /swapfile
```

**Output (sample):**
```text
Setting up swapspace version 1 ...
```

### 257. `swapon`
**संक्षिप्त जानकारी:** swap space सक्रिय गर्छ।

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
**संक्षिप्त जानकारी:** swap space निष्क्रिय गर्छ।

**Example:**
```bash
sudo swapoff /swapfile
```

**Output (sample):**
```text
No output on success.
```

### 259. `losetup`
**संक्षिप्त जानकारी:** loop device सेटअप गर्छ (file लाई device जस्तै mount गर्न)।

**Example:**
```bash
sudo losetup -a
```

**Output (sample):**
```text
/dev/loop0: []: (/path/disk.img)
```

### 260. `mkisofs`
**संक्षिप्त जानकारी:** ISO 9660 CD/DVD image फाइल बनाउँछ।

**Example:**
```bash
mkisofs --help
```

**Output (sample):**
```text
Usage/help information for `mkisofs` (illustrative; exact output varies by distribution/version).
```

### 261. `eject`
**संक्षिप्त जानकारी:** removable media (CD/DVD/USB) निकाल्छ।

**Example:**
```bash
eject /dev/cdrom
```

**Output (sample):**
```text
No output on success.
```

### 262. `lndir`
**संक्षिप्त जानकारी:** directory tree को symbolic link mirror बनाउँछ।

**Example:**
```bash
lndir --help
```

**Output (sample):**
```text
Usage/help information for `lndir` (illustrative; exact output varies by distribution/version).
```

### 263. `mdadm`
**संक्षिप्त जानकारी:** software RAID arrays व्यवस्थापन गर्छ।

**Example:**
```bash
sudo mdadm --detail --scan
```

**Output (sample):**
```text
ARRAY /dev/md0 metadata=1.2 name=...
```

### 264. `dumpe2fs`
**संक्षिप्त जानकारी:** ext file system को विस्तृत जानकारी देखाउँछ।

**Example:**
```bash
dumpe2fs --help
```

**Output (sample):**
```text
Usage/help information for `dumpe2fs` (illustrative; exact output varies by distribution/version).
```

### 265. `sync`
**संक्षिप्त जानकारी:** memory मा buffered data लाई disk मा तुरुन्त लेख्छ।

**Example:**
```bash
sync
```

**Output (sample):**
```text
No output on success.
```

### 266. `badblocks`
**संक्षिप्त जानकारी:** disk मा खराब (bad) blocks खोज्छ।

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
**संक्षिप्त जानकारी:** MS-DOS file system को volume label सेट/देखाउँछ।

**Example:**
```bash
mlabel --help
```

**Output (sample):**
```text
Usage/help information for `mlabel` (illustrative; exact output varies by distribution/version).
```

### 268. `mformat`
**संक्षिप्त जानकारी:** device लाई MS-DOS file system जस्तो format गर्छ।

**Example:**
```bash
mformat --help
```

**Output (sample):**
```text
Usage/help information for `mformat` (illustrative; exact output varies by distribution/version).
```

### 269. `mpartition`
**संक्षिप्त जानकारी:** MS-DOS-style disk partition व्यवस्थापन गर्छ।

**Example:**
```bash
mpartition --help
```

**Output (sample):**
```text
Usage/help information for `mpartition` (illustrative; exact output varies by distribution/version).
```

### 270. `mdeltree`
**संक्षिप्त जानकारी:** MS-DOS directory tree सम्पूर्ण मेट्छ।

**Example:**
```bash
mdeltree --help
```

**Output (sample):**
```text
Usage/help information for `mdeltree` (illustrative; exact output varies by distribution/version).
```

### 271. `mdu`
**संक्षिप्त जानकारी:** MS-DOS file system मा disk usage देखाउँछ।

**Example:**
```bash
mdu --help
```

**Output (sample):**
```text
Usage/help information for `mdu` (illustrative; exact output varies by distribution/version).
```

### 272. `mcd`
**संक्षिप्त जानकारी:** MS-DOS file system भित्र directory परिवर्तन गर्छ।

**Example:**
```bash
mcd --help
```

**Output (sample):**
```text
Usage/help information for `mcd` (illustrative; exact output varies by distribution/version).
```

### 273. `mmount`
**संक्षिप्त जानकारी:** MS-DOS device mount गर्छ।

**Example:**
```bash
mmount --help
```

**Output (sample):**
```text
Usage/help information for `mmount` (illustrative; exact output varies by distribution/version).
```

### 274. `mbadblocks`
**संक्षिप्त जानकारी:** MS-DOS disk मा bad blocks पत्ता लगाउँछ।

**Example:**
```bash
mbadblocks --help
```

**Output (sample):**
```text
Usage/help information for `mbadblocks` (illustrative; exact output varies by distribution/version).
```

### 275. `fsck.minix`
**संक्षिप्त जानकारी:** Minix file system जाँच र मर्मत गर्छ।

**Example:**
```bash
fsck.minix --help
```

**Output (sample):**
```text
Usage/help information for `fsck.minix` (illustrative; exact output varies by distribution/version).
```

### 276. `mke2fs`
**संक्षिप्त जानकारी:** ext2/ext3/ext4 file system बनाउँछ (format गर्छ)।

**Example:**
```bash
sudo mke2fs -t ext4 /dev/sdb1
```

**Output (sample):**
```text
Creating filesystem with ...
```

### 277. `mkfs.ext2`
**संक्षिप्त जानकारी:** ext2 file system बनाउँछ।

**Example:**
```bash
sudo mkfs.ext2 /dev/sdb1
```

**Output (sample):**
```text
Creating filesystem with ...
```

### 278. `mkfs.minix`
**संक्षिप्त जानकारी:** Minix file system बनाउँछ।

**Example:**
```bash
mkfs.minix --help
```

**Output (sample):**
```text
Usage/help information for `mkfs.minix` (illustrative; exact options vary by distribution).
```

### 279. `mkfs.msdos`
**संक्षिप्त जानकारी:** MS-DOS (FAT) file system बनाउँछ।

**Example:**
```bash
sudo mkfs.msdos /dev/sdb1
```

**Output (sample):**
```text
mkfs.fat ...
```

### 280. `mkdosfs`
**संक्षिप्त जानकारी:** DOS FAT file system बनाउँछ (mkfs.msdos जस्तै)।

**Example:**
```bash
sudo mkdosfs /dev/sdb1
```

**Output (sample):**
```text
mkfs.fat ...
```

### 281. `mkbootdisk`
**संक्षिप्त जानकारी:** bootable floppy/USB disk बनाउँछ (legacy)।

**Example:**
```bash
mkbootdisk --help
```

**Output (sample):**
```text
Usage/help information for `mkbootdisk` (illustrative; exact output varies by distribution/version).
```

### 282. `mkinitrd`
**संक्षिप्त जानकारी:** boot-time initial RAM disk (initrd) बनाउँछ।

**Example:**
```bash
mkinitrd --help
```

**Output (sample):**
```text
Usage/help information for `mkinitrd` (illustrative; exact output varies by distribution/version).
```

### 283. `sfdisk`
**संक्षिप्त जानकारी:** script-based disk partitioning tool।

**Example:**
```bash
sfdisk --help
```

**Output (sample):**
```text
Usage/help information for `sfdisk` (illustrative; exact output varies by distribution/version).
```

### 284. `fsck.ext2`
**संक्षिप्त जानकारी:** ext2 file system जाँच गर्छ (e2fsck जस्तै)।

**Example:**
```bash
fsck.ext2 --help
```

**Output (sample):**
```text
Usage/help information for `fsck.ext2` (illustrative; exact output varies by distribution/version).
```

### 285. `symlinks`
**संक्षिप्त जानकारी:** directory मा भएका symbolic links जाँच/सफा गर्छ।

**Example:**
```bash
symlinks --help
```

**Output (sample):**
```text
Usage/help information for `symlinks` (illustrative; exact output varies by distribution/version).
```

### 286. `cfdisk`
**संक्षिप्त जानकारी:** curses-based user-friendly disk partitioning tool।

**Example:**
```bash
cfdisk --help
```

**Output (sample):**
```text
Usage/help information for `cfdisk` (illustrative; exact output varies by distribution/version).
```

---

<p align="right"><a href="#top">⬆️ सूचीमा फर्कने</a></p>

</details>

---

<a id="cat-287-309"></a>
<details>
<summary><h2 style="display:inline;">📦 Compression and Archiving</h2> &nbsp; <em>Commands 287–309 (23 commands)</em></summary>

### 287. `tar`
**संक्षिप्त जानकारी:** धेरै file/folder लाई archive बनाउन वा खोल्न प्रयोग हुन्छ।

**Example:**
```bash
tar -czf backup.tar.gz project/
```

**Output (sample):**
```text
No output on success.
```

### 288. `gzip`
**संक्षिप्त जानकारी:** file लाई gzip format मा compress गर्छ।

**Example:**
```bash
gzip notes.txt
```

**Output (sample):**
```text
No output; notes.txt.gz is created.
```

### 289. `gunzip`
**संक्षिप्त जानकारी:** gzip compressed file खोल्छ।

**Example:**
```bash
gunzip notes.txt.gz
```

**Output (sample):**
```text
No output; notes.txt is restored.
```

### 290. `zip`
**संक्षिप्त जानकारी:** file/folder लाई ZIP archive मा compress गर्छ।

**Example:**
```bash
zip backup.zip notes.txt
```

**Output (sample):**
```text
adding: notes.txt (stored 0%)
```

### 291. `unzip`
**संक्षिप्त जानकारी:** ZIP archive खोल्छ।

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
**संक्षिप्त जानकारी:** file लाई bzip2 format मा compress गर्छ।

**Example:**
```bash
bzip2 notes.txt
```

**Output (sample):**
```text
No output; notes.txt.bz2 is created.
```

### 293. `bunzip2`
**संक्षिप्त जानकारी:** bzip2 compressed file खोल्छ।

**Example:**
```bash
bunzip2 notes.txt.bz2
```

**Output (sample):**
```text
No output; notes.txt is restored.
```

### 294. `compress`
**संक्षिप्त जानकारी:** file लाई .Z format मा compress गर्छ (legacy)।

**Example:**
```bash
compress --help
```

**Output (sample):**
```text
Usage/help information for `compress` (illustrative; exact output varies by distribution/version).
```

### 295. `uncompress`
**संक्षिप्त जानकारी:** .Z compressed file लाई decompress गर्छ।

**Example:**
```bash
uncompress --help
```

**Output (sample):**
```text
Usage/help information for `uncompress` (illustrative; exact output varies by distribution/version).
```

### 296. `cpio`
**संक्षिप्त जानकारी:** archive file बनाउने वा extract गर्ने (copy in/out) tool।

**Example:**
```bash
find . -print | cpio -ov > archive.cpio
```

**Output (sample):**
```text
1 block
```

### 297. `ar`
**संक्षिप्त जानकारी:** static library (.a) archive बनाउने/व्यवस्थापन गर्ने tool।

**Example:**
```bash
ar rcs libdemo.a demo.o
```

**Output (sample):**
```text
No output on success.
```

### 298. `rar`
**संक्षिप्त जानकारी:** RAR format मा file compress गर्छ।

**Example:**
```bash
rar --help
```

**Output (sample):**
```text
Usage/help information for `rar` (illustrative; exact output varies by distribution/version).
```

### 299. `unrar`
**संक्षिप्त जानकारी:** RAR archive extract गर्छ।

**Example:**
```bash
unrar --help
```

**Output (sample):**
```text
Usage/help information for `unrar` (illustrative; exact output varies by distribution/version).
```

### 300. `zcat`
**संक्षिप्त जानकारी:** gzip compressed file को सामग्री (decompress नगरी) देखाउँछ।

**Example:**
```bash
zcat notes.txt.gz
```

**Output (sample):**
```text
Hello Linux
```

### 301. `zless`
**संक्षिप्त जानकारी:** gzip compressed file लाई pager (less) मार्फत हेर्छ।

**Example:**
```bash
zless --help
```

**Output (sample):**
```text
Usage/help information for `zless` (illustrative; exact output varies by distribution/version).
```

### 302. `zdiff`
**संक्षिप्त जानकारी:** दुई gzip compressed files तुलना गर्छ।

**Example:**
```bash
zdiff --help
```

**Output (sample):**
```text
Usage/help information for `zdiff` (illustrative; exact output varies by distribution/version).
```

### 303. `zgrep`
**संक्षिप्त जानकारी:** gzip compressed file भित्र pattern खोज्छ।

**Example:**
```bash
zgrep --help
```

**Output (sample):**
```text
Usage/help information for `zgrep` (illustrative; exact output varies by distribution/version).
```

### 304. `zipinfo`
**संक्षिप्त जानकारी:** zip archive को सामग्री बारे जानकारी देखाउँछ।

**Example:**
```bash
zipinfo --help
```

**Output (sample):**
```text
Usage/help information for `zipinfo` (illustrative; exact output varies by distribution/version).
```

### 305. `bzcat`
**संक्षिप्त जानकारी:** bzip2 compressed file को सामग्री देखाउँछ।

**Example:**
```bash
bzcat notes.txt.bz2
```

**Output (sample):**
```text
Hello Linux
```

### 306. `bzdiff`
**संक्षिप्त जानकारी:** दुई bzip2 compressed files तुलना गर्छ।

**Example:**
```bash
bzdiff --help
```

**Output (sample):**
```text
Usage/help information for `bzdiff` (illustrative; exact output varies by distribution/version).
```

### 307. `bzgrep`
**संक्षिप्त जानकारी:** bzip2 compressed file भित्र pattern खोज्छ।

**Example:**
```bash
bzgrep --help
```

**Output (sample):**
```text
Usage/help information for `bzgrep` (illustrative; exact output varies by distribution/version).
```

### 308. `bzless`
**संक्षिप्त जानकारी:** bzip2 compressed file लाई pager मार्फत हेर्छ।

**Example:**
```bash
bzless --help
```

**Output (sample):**
```text
Usage/help information for `bzless` (illustrative; exact output varies by distribution/version).
```

### 309. `bzmore`
**संक्षिप्त जानकारी:** bzip2 compressed file लाई page-by-page हेर्छ।

**Example:**
```bash
bzmore --help
```

**Output (sample):**
```text
Usage/help information for `bzmore` (illustrative; exact output varies by distribution/version).
```

---

<p align="right"><a href="#top">⬆️ सूचीमा फर्कने</a></p>

</details>

---

<a id="cat-310-333"></a>
<details>
<summary><h2 style="display:inline;">⚙️ Process Management</h2> &nbsp; <em>Commands 310–333 (24 commands)</em></summary>

### 310. `kill`
**संक्षिप्त जानकारी:** PID प्रयोग गरेर process बन्द गर्न signal पठाउँछ।

**Example:**
```bash
kill 1234
```

**Output (sample):**
```text
No output on success.
```

### 311. `pkill`
**संक्षिप्त जानकारी:** नाम वा pattern का आधारमा process बन्द गर्छ।

**Example:**
```bash
pkill firefox
```

**Output (sample):**
```text
No output on success.
```

### 312. `killall`
**संक्षिप्त जानकारी:** दिइएको नामका process हरू बन्द गर्छ।

**Example:**
```bash
killall firefox
```

**Output (sample):**
```text
No output on success.
```

### 313. `nice`
**संक्षिप्त जानकारी:** process को CPU scheduling priority सुरु गर्दा परिवर्तन गर्छ।

**Example:**
```bash
nice -n 10 ./job.sh
```

**Output (sample):**
```text
Command runs with adjusted priority.
```

### 314. `renice`
**संक्षिप्त जानकारी:** चलिरहेको process को priority परिवर्तन गर्छ।

**Example:**
```bash
renice 10 -p 1234
```

**Output (sample):**
```text
1234 (process ID) old priority 0, new priority 10
```

### 315. `jobs`
**संक्षिप्त जानकारी:** हालको shell का background jobs देखाउँछ।

**Example:**
```bash
jobs
```

**Output (sample):**
```text
[1]+  Running  ./script.sh &
```

### 316. `fg`
**संक्षिप्त जानकारी:** background job लाई foreground मा ल्याउँछ।

**Example:**
```bash
fg %1
```

**Output (sample):**
```text
./script.sh
```

### 317. `bg`
**संक्षिप्त जानकारी:** stopped job लाई background मा चलाउँछ।

**Example:**
```bash
bg %1
```

**Output (sample):**
```text
[1]+ ./script.sh &
```

### 318. `pgrep`
**संक्षिप्त जानकारी:** process को नाम/PID खोज्छ।

**Example:**
```bash
pgrep sshd
```

**Output (sample):**
```text
790
```

### 319. `nohup`
**संक्षिप्त जानकारी:** terminal बन्द भएपछि पनि command चलिरहने बनाउँछ।

**Example:**
```bash
nohup ./backup.sh > backup.log 2>&1 &
```

**Output (sample):**
```text
nohup: ignoring input and appending output to 'nohup.out'
```

### 320. `disown`
**संक्षिप्त जानकारी:** background job लाई shell को job list बाट हटाउँछ (terminal बन्द भए पनि चलिरहन्छ)।

**Example:**
```bash
disown --help
```

**Output (sample):**
```text
Usage/help information for `disown` (illustrative; exact output varies by distribution/version).
```

### 321. `screen`
**संक्षिप्त जानकारी:** एउटै terminal मा धेरै virtual sessions (multiplexing) व्यवस्थापन गर्छ।

**Example:**
```bash
screen --help
```

**Output (sample):**
```text
Usage/help information for `screen` (illustrative; exact output varies by distribution/version).
```

### 322. `tmux`
**संक्षिप्त जानकारी:** screen जस्तै terminal multiplexer; sessions detach/attach गर्न सकिन्छ।

**Example:**
```bash
tmux new -s work
```

**Output (sample):**
```text
Interactive tmux session opens.
```

### 323. `strace`
**संक्षिप्त जानकारी:** program ले गर्ने system calls trace गर्छ।

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
**संक्षिप्त जानकारी:** program ले प्रयोग गर्ने library calls trace गर्छ।

**Example:**
```bash
ltrace ls
```

**Output (sample):**
```text
libc calls ...
```

### 325. `skill`
**संक्षिप्त जानकारी:** निर्दिष्ट user/process हरूलाई signal पठाउँछ (kill जस्तै)।

**Example:**
```bash
skill --help
```

**Output (sample):**
```text
Usage/help information for `skill` (illustrative; exact output varies by distribution/version).
```

### 326. `psnice`
**संक्षिप्त जानकारी:** चलिरहेका processes को priority (nice value) परिवर्तन गर्छ।

**Example:**
```bash
psnice --help
```

**Output (sample):**
```text
Usage/help information for `psnice` (illustrative; exact output varies by distribution/version).
```

### 327. `at`
**संक्षिप्त जानकारी:** निर्धारित समयमा एकपटक चल्ने काम schedule गर्छ।

**Example:**
```bash
at --help
```

**Output (sample):**
```text
Usage/help information for `at` (illustrative; exact output varies by distribution/version).
```

### 328. `batch`
**संक्षिप्त जानकारी:** system load कम भएको बेला काम चलाउन schedule गर्छ।

**Example:**
```bash
batch --help
```

**Output (sample):**
```text
Usage/help information for `batch` (illustrative; exact output varies by distribution/version).
```

### 329. `atd`
**संक्षिप्त जानकारी:** at/batch जबहरू चलाउने background daemon।

**Example:**
```bash
atd --help
```

**Output (sample):**
```text
Usage/help information for `atd` (illustrative; exact output varies by distribution/version).
```

### 330. `atq`
**संक्षिप्त जानकारी:** schedule गरिएका (at) pending jobs को सूची देखाउँछ।

**Example:**
```bash
atq --help
```

**Output (sample):**
```text
Usage/help information for `atq` (illustrative; exact output varies by distribution/version).
```

### 331. `atrm`
**संक्षिप्त जानकारी:** schedule गरिएको at job रद्द गर्छ।

**Example:**
```bash
atrm --help
```

**Output (sample):**
```text
Usage/help information for `atrm` (illustrative; exact output varies by distribution/version).
```

### 332. `chrt`
**संक्षिप्त जानकारी:** process को real-time scheduling policy/priority परिवर्तन गर्छ।

**Example:**
```bash
chrt --help
```

**Output (sample):**
```text
Usage/help information for `chrt` (illustrative; exact output varies by distribution/version).
```

### 333. `setsid`
**संक्षिप्त जानकारी:** नयाँ session मा command चलाउँछ (controlling terminal बिना)।

**Example:**
```bash
setsid --help
```

**Output (sample):**
```text
Usage/help information for `setsid` (illustrative; exact output varies by distribution/version).
```

---

<p align="right"><a href="#top">⬆️ सूचीमा फर्कने</a></p>

</details>

---

<a id="cat-334-491"></a>
<details>
<summary><h2 style="display:inline;">🛠️ System Configuration and Settings</h2> &nbsp; <em>Commands 334–491 (158 commands)</em></summary>

### 334. `crontab`
**संक्षिप्त जानकारी:** निश्चित समयमा स्वचालित command/script चलाउने schedule बनाउँछ।

**Example:**
```bash
crontab -l
```

**Output (sample):**
```text
0 2 * * * /home/user/backup.sh
```

### 335. `systemctl`
**संक्षिप्त जानकारी:** systemd service सुरु, रोक, restart र status व्यवस्थापन गर्छ।

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
**संक्षिप्त जानकारी:** service व्यवस्थापनका लागि पुरानो/compatibility interface हो।

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
**संक्षिप्त जानकारी:** system services लाई boot-time मा on/off गर्ने legacy tool।

**Example:**
```bash
chkconfig --help
```

**Output (sample):**
```text
Usage/help information for `chkconfig` (illustrative; exact output varies by distribution/version).
```

### 338. `update-rc.d`
**संक्षिप्त जानकारी:** init script लाई runlevels मा install/remove गर्छ (Debian-based)।

**Example:**
```bash
update-rc.d --help
```

**Output (sample):**
```text
Usage/help information for `update-rc.d` (illustrative; exact output varies by distribution/version).
```

### 339. `timedatectl`
**संक्षिप्त जानकारी:** system date, time र timezone व्यवस्थापन गर्छ।

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
**संक्षिप्त जानकारी:** हालको language, character encoding र locale settings देखाउँछ।

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
**संक्षिप्त जानकारी:** system-wide locale र keyboard settings व्यवस्थापन गर्छ।

**Example:**
```bash
localectl status
```

**Output (sample):**
```text
System Locale: LANG=en_US.UTF-8
```

### 342. `ulimit`
**संक्षिप्त जानकारी:** shell/process का लागि resource limits (file size, memory आदि) सेट गर्छ (built-in)।

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
**संक्षिप्त जानकारी:** लामो command का लागि छोटो नाम बनाउँछ।

**Example:**
```bash
alias ll='ls -la'; ll
```

**Output (sample):**
```text
total ...
```

### 344. `unalias`
**संक्षिप्त जानकारी:** बनाइएको alias हटाउँछ।

**Example:**
```bash
unalias ll
```

**Output (sample):**
```text
No output on success.
```

### 345. `export`
**संक्षिप्त जानकारी:** environment variable लाई child processes मा उपलब्ध गराउँछ।

**Example:**
```bash
export APP_ENV=production; echo $APP_ENV
```

**Output (sample):**
```text
production
```

### 346. `set`
**संक्षिप्त जानकारी:** shell variables र settings हेर्न/सेट गर्न प्रयोग हुन्छ।

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
**संक्षिप्त जानकारी:** environment variable हटाउँछ।

**Example:**
```bash
unset APP_ENV
```

**Output (sample):**
```text
No output on success.
```

### 348. `env`
**संक्षिप्त जानकारी:** environment variables हेर्न वा environment सहित command चलाउन प्रयोग हुन्छ।

**Example:**
```bash
env | grep APP_ENV
```

**Output (sample):**
```text
APP_ENV=production
```

### 349. `sysctl`
**संक्षिप्त जानकारी:** kernel parameters हेर्न वा परिवर्तन गर्न प्रयोग हुन्छ।

**Example:**
```bash
sysctl net.ipv4.ip_forward
```

**Output (sample):**
```text
net.ipv4.ip_forward = 0
```

### 350. `modprobe`
**संक्षिप्त जानकारी:** kernel module load वा unload गर्न प्रयोग हुन्छ।

**Example:**
```bash
sudo modprobe loop
```

**Output (sample):**
```text
No output on success.
```

### 351. `lsmod`
**संक्षिप्त जानकारी:** हाल load भएका kernel modules देखाउँछ।

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
**संक्षिप्त जानकारी:** kernel module लाई सिधै insert (load) गर्छ।

**Example:**
```bash
insmod --help
```

**Output (sample):**
```text
Usage/help information for `insmod` (illustrative; exact options vary by distribution).
```

### 353. `rmmod`
**संक्षिप्त जानकारी:** loaded kernel module हटाउँछ।

**Example:**
```bash
rmmod --help
```

**Output (sample):**
```text
Usage/help information for `rmmod` (illustrative; exact options vary by distribution).
```

### 354. `depmod`
**संक्षिप्त जानकारी:** kernel modules बीचको dependency जानकारी generate गर्छ।

**Example:**
```bash
depmod --help
```

**Output (sample):**
```text
Usage/help information for `depmod` (illustrative; exact output varies by distribution/version).
```

### 355. `lspci`
**संक्षिप्त जानकारी:** PCI hardware devices को जानकारी देखाउँछ।

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
**संक्षिप्त जानकारी:** hardware (BIOS) clock हेर्ने/सेट गर्ने command।

**Example:**
```bash
sudo hwclock --show
```

**Output (sample):**
```text
2026-08-21 11:57:00.123456+05:45
```

### 357. `setserial`
**संक्षिप्त जानकारी:** serial port का parameters configure गर्छ।

**Example:**
```bash
setserial --help
```

**Output (sample):**
```text
Usage/help information for `setserial` (illustrative; exact output varies by distribution/version).
```

### 358. `edquota`
**संक्षिप्त जानकारी:** user/group disk quota edit गर्छ।

**Example:**
```bash
edquota --help
```

**Output (sample):**
```text
Usage/help information for `edquota` (illustrative; exact output varies by distribution/version).
```

### 359. `quota`
**संक्षिप्त जानकारी:** user/group को disk usage limit देखाउँछ।

**Example:**
```bash
quota --help
```

**Output (sample):**
```text
Usage/help information for `quota` (illustrative; exact output varies by distribution/version).
```

### 360. `quotaon`
**संक्षिप्त जानकारी:** file system मा disk quota सक्रिय गर्छ।

**Example:**
```bash
quotaon --help
```

**Output (sample):**
```text
Usage/help information for `quotaon` (illustrative; exact output varies by distribution/version).
```

### 361. `quotaoff`
**संक्षिप्त जानकारी:** file system मा disk quota निष्क्रिय गर्छ।

**Example:**
```bash
quotaoff --help
```

**Output (sample):**
```text
Usage/help information for `quotaoff` (illustrative; exact output varies by distribution/version).
```

### 362. `quotacheck`
**संक्षिप्त जानकारी:** file system स्क्यान गरी quota जानकारी अद्यावधिक गर्छ।

**Example:**
```bash
quotacheck --help
```

**Output (sample):**
```text
Usage/help information for `quotacheck` (illustrative; exact output varies by distribution/version).
```

### 363. `repquota`
**संक्षिप्त जानकारी:** file system का सबै users को quota सारांश देखाउँछ।

**Example:**
```bash
repquota --help
```

**Output (sample):**
```text
Usage/help information for `repquota` (illustrative; exact output varies by distribution/version).
```

### 364. `chroot`
**संक्षिप्त जानकारी:** निर्दिष्ट directory लाई root (/) बनाई त्यहीँभित्र command चलाउँछ।

**Example:**
```bash
chroot --help
```

**Output (sample):**
```text
Usage/help information for `chroot` (illustrative; exact output varies by distribution/version).
```

### 365. `dircolors`
**संक्षिप्त जानकारी:** `ls` मा प्रयोग हुने रङहरू (color scheme) सेटअप गर्छ।

**Example:**
```bash
dircolors --help
```

**Output (sample):**
```text
Usage/help information for `dircolors` (illustrative; exact output varies by distribution/version).
```

### 366. `loadkeys`
**संक्षिप्त जानकारी:** keyboard layout/keymap load गर्छ।

**Example:**
```bash
loadkeys --help
```

**Output (sample):**
```text
Usage/help information for `loadkeys` (illustrative; exact output varies by distribution/version).
```

### 367. `modinfo`
**संक्षिप्त जानकारी:** kernel module बारे जानकारी देखाउँछ।

**Example:**
```bash
modinfo --help
```

**Output (sample):**
```text
Usage/help information for `modinfo` (illustrative; exact output varies by distribution/version).
```

### 368. `setleds`
**संक्षिप्त जानकारी:** keyboard LEDs (Caps/Num/Scroll Lock) नियन्त्रण गर्छ।

**Example:**
```bash
setleds --help
```

**Output (sample):**
```text
Usage/help information for `setleds` (illustrative; exact output varies by distribution/version).
```

### 369. `showkey`
**संक्षिप्त जानकारी:** थिचिएको keyboard key को code देखाउँछ (debugging का लागि)।

**Example:**
```bash
showkey --help
```

**Output (sample):**
```text
Usage/help information for `showkey` (illustrative; exact output varies by distribution/version).
```

### 370. `stty`
**संक्षिप्त जानकारी:** terminal line settings हेर्ने/परिवर्तन गर्ने command।

**Example:**
```bash
stty --help
```

**Output (sample):**
```text
Usage/help information for `stty` (illustrative; exact output varies by distribution/version).
```

### 371. `zdump`
**संक्षिप्त जानकारी:** timezone जानकारी देखाउँछ।

**Example:**
```bash
zdump --help
```

**Output (sample):**
```text
Usage/help information for `zdump` (illustrative; exact output varies by distribution/version).
```

### 372. `cron`
**संक्षिप्त जानकारी:** निर्धारित समयमा दोहोरिने काम automatically चलाउने scheduling daemon।

**Example:**
```bash
cron --help
```

**Output (sample):**
```text
Usage/help information for `cron` (illustrative; exact output varies by distribution/version).
```

### 373. `aumix`
**संक्षिप्त जानकारी:** audio mixer levels समायोजन गर्ने command-line tool।

**Example:**
```bash
aumix --help
```

**Output (sample):**
```text
Usage/help information for `aumix` (illustrative; exact output varies by distribution/version).
```

### 374. `clock`
**संक्षिप्त जानकारी:** hardware clock सँग interact गर्छ (hwclock को पुरानो नाम)।

**Example:**
```bash
clock --help
```

**Output (sample):**
```text
Usage/help information for `clock` (illustrative; exact output varies by distribution/version).
```

### 375. `lilo`
**संक्षिप्त जानकारी:** पुरानो Linux boot loader install/configure गर्छ।

**Example:**
```bash
lilo --help
```

**Output (sample):**
```text
Usage/help information for `lilo` (illustrative; exact output varies by distribution/version).
```

### 376. `ntsysv`
**संक्षिप्त जानकारी:** services लाई on/off गर्ने text-based (Red Hat) tool।

**Example:**
```bash
ntsysv --help
```

**Output (sample):**
```text
Usage/help information for `ntsysv` (illustrative; exact output varies by distribution/version).
```

### 377. `rdate`
**संक्षिप्त जानकारी:** network server बाट system time सेट गर्छ।

**Example:**
```bash
rdate --help
```

**Output (sample):**
```text
Usage/help information for `rdate` (illustrative; exact output varies by distribution/version).
```

### 378. `resize`
**संक्षिप्त जानकारी:** terminal window को size (rows/columns) पत्ता लगाई सेट गर्छ।

**Example:**
```bash
resize --help
```

**Output (sample):**
```text
Usage/help information for `resize` (illustrative; exact output varies by distribution/version).
```

### 379. `sndconfig`
**संक्षिप्त जानकारी:** sound card configure गर्ने legacy tool (Red Hat)।

**Example:**
```bash
sndconfig --help
```

**Output (sample):**
```text
Usage/help information for `sndconfig` (illustrative; exact output varies by distribution/version).
```

### 380. `setconsole`
**संक्षिप्त जानकारी:** default console device सेट गर्छ।

**Example:**
```bash
setconsole --help
```

**Output (sample):**
```text
Usage/help information for `setconsole` (illustrative; exact output varies by distribution/version).
```

### 381. `apmd`
**संक्षिप्त जानकारी:** Advanced Power Management daemon (legacy power management)।

**Example:**
```bash
apmd --help
```

**Output (sample):**
```text
Usage/help information for `apmd` (illustrative; exact output varies by distribution/version).
```

### 382. `fbset`
**संक्षिप्त जानकारी:** framebuffer device को resolution/parameters सेट गर्छ।

**Example:**
```bash
fbset --help
```

**Output (sample):**
```text
Usage/help information for `fbset` (illustrative; exact output varies by distribution/version).
```

### 383. `rpm`
**संक्षिप्त जानकारी:** RPM package install/remove/query गर्ने package manager (Red Hat based)।

**Example:**
```bash
rpm --help
```

**Output (sample):**
```text
Usage/help information for `rpm` (illustrative; exact output varies by distribution/version).
```

### 384. `apt-get`
**संक्षिप्त जानकारी:** Ubuntu/Debian package management को command-line tool हो।

**Example:**
```bash
sudo apt-get update
```

**Output (sample):**
```text
Reading package lists... Done
```

### 385. `dpkg`
**संक्षिप्त जानकारी:** Debian package install, remove र जानकारी व्यवस्थापन गर्छ।

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
**संक्षिप्त जानकारी:** RPM-based systems (जस्तै CentOS) को package manager।

**Example:**
```bash
yum --help
```

**Output (sample):**
```text
Usage/help information for `yum` (illustrative; exact output varies by distribution/version).
```

### 387. `apt`
**संक्षिप्त जानकारी:** Ubuntu/Debian मा package install, update र manage गर्न प्रयोग हुन्छ।

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
**संक्षिप्त जानकारी:** Debian/Ubuntu को अर्को text-based package manager।

**Example:**
```bash
aptitude --help
```

**Output (sample):**
```text
Usage/help information for `aptitude` (illustrative; exact output varies by distribution/version).
```

### 389. `pacman`
**संक्षिप्त जानकारी:** Arch Linux को package manager।

**Example:**
```bash
pacman --help
```

**Output (sample):**
```text
Usage/help information for `pacman` (illustrative; exact output varies by distribution/version).
```

### 390. `zypper`
**संक्षिप्त जानकारी:** openSUSE को package manager।

**Example:**
```bash
zypper --help
```

**Output (sample):**
```text
Usage/help information for `zypper` (illustrative; exact output varies by distribution/version).
```

### 391. `emerge`
**संक्षिप्त जानकारी:** Gentoo Linux को Portage package manager command।

**Example:**
```bash
emerge --help
```

**Output (sample):**
```text
Usage/help information for `emerge` (illustrative; exact output varies by distribution/version).
```

### 392. `dnf`
**संक्षिप्त जानकारी:** yum को उत्तराधिकारी, आधुनिक RPM package manager।

**Example:**
```bash
dnf --help
```

**Output (sample):**
```text
Usage/help information for `dnf` (illustrative; exact output varies by distribution/version).
```

### 393. `snap`
**संक्षिप्त जानकारी:** Snap packages install/manage गर्ने universal package manager।

**Example:**
```bash
snap list
```

**Output (sample):**
```text
Name  Version  Rev  Tracking  Publisher
```

### 394. `flatpak`
**संक्षिप्त जानकारी:** sandboxed applications install/manage गर्ने package manager।

**Example:**
```bash
flatpak list
```

**Output (sample):**
```text
Name  Application ID  Version
```

### 395. `bash`
**संक्षिप्त जानकारी:** Bash shell चलाउन वा script execute गर्न प्रयोग हुन्छ।

**Example:**
```bash
bash --version | head -n 1
```

**Output (sample):**
```text
GNU bash, version 5.x
```

### 396. `sh`
**संक्षिप्त जानकारी:** POSIX shell चलाउन प्रयोग हुन्छ।

**Example:**
```bash
sh -c 'echo hello'
```

**Output (sample):**
```text
hello
```

### 397. `perl`
**संक्षिप्त जानकारी:** Perl scripting language interpreter चलाउँछ।

**Example:**
```bash
perl -e 'print 2+3'
```

**Output (sample):**
```text
5
```

### 398. `python`
**संक्षिप्त जानकारी:** Python program/script चलाउन प्रयोग हुन्छ।

**Example:**
```bash
python3 -c 'print(2+3)'
```

**Output (sample):**
```text
5
```

### 399. `gcc`
**संक्षिप्त जानकारी:** C program compile गर्न प्रयोग हुन्छ।

**Example:**
```bash
gcc --version | head -n 1
```

**Output (sample):**
```text
gcc (Ubuntu ...) 13.x
```

### 400. `g++`
**संक्षिप्त जानकारी:** C++ program compile गर्न प्रयोग हुन्छ।

**Example:**
```bash
g++ --version | head -n 1
```

**Output (sample):**
```text
g++ (Ubuntu ...) 13.x
```

### 401. `make`
**संक्षिप्त जानकारी:** Makefile अनुसार source code build/compile गर्छ।

**Example:**
```bash
make
```

**Output (sample):**
```text
gcc ... -o app
```

### 402. `cmake`
**संक्षिप्त जानकारी:** software project को build configuration तयार गर्छ।

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
**संक्षिप्त जानकारी:** Makefile.in generate गर्ने GNU build tool।

**Example:**
```bash
automake --help
```

**Output (sample):**
```text
Usage/help information for `automake` (illustrative; exact output varies by distribution/version).
```

### 404. `autoconf`
**संक्षिप्त जानकारी:** configure script generate गर्ने GNU build tool।

**Example:**
```bash
autoconf --help
```

**Output (sample):**
```text
Usage/help information for `autoconf` (illustrative; exact output varies by distribution/version).
```

### 405. `gdb`
**संक्षिप्त जानकारी:** program debugging गर्न प्रयोग हुन्छ।

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
**संक्षिप्त जानकारी:** executable ले चाहिने shared libraries देखाउँछ।

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
**संक्षिप्त जानकारी:** object files बाट विस्तृत जानकारी (disassembly आदि) देखाउँछ।

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
**संक्षिप्त जानकारी:** object file मा भएका symbols को सूची देखाउँछ।

**Example:**
```bash
nm app | head
```

**Output (sample):**
```text
000000... T main
```

### 409. `readelf`
**संक्षिप्त जानकारी:** ELF format file को detail जानकारी देखाउँछ।

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
**संक्षिप्त जानकारी:** binary file भित्रका printable text strings निकाल्छ।

**Example:**
```bash
strings app | head
```

**Output (sample):**
```text
Hello Linux
```

### 411. `ctags`
**संक्षिप्त जानकारी:** source code मा function/variable हरूको index (tag) बनाउँछ।

**Example:**
```bash
ctags --help
```

**Output (sample):**
```text
Usage/help information for `ctags` (illustrative; exact output varies by distribution/version).
```

### 412. `cscope`
**संक्षिप्त जानकारी:** C source code भित्र symbols browse/खोज्ने tool।

**Example:**
```bash
cscope --help
```

**Output (sample):**
```text
Usage/help information for `cscope` (illustrative; exact output varies by distribution/version).
```

### 413. `diff3`
**संक्षिप्त जानकारी:** तीनवटा files तुलना गर्छ (merge conflicts का लागि)।

**Example:**
```bash
diff3 --help
```

**Output (sample):**
```text
Usage/help information for `diff3` (illustrative; exact output varies by distribution/version).
```

### 414. `svn`
**संक्षिप्त जानकारी:** Subversion version control system client।

**Example:**
```bash
svn status
```

**Output (sample):**
```text
M       file.txt
```

### 415. `git`
**संक्षिप्त जानकारी:** source code version control व्यवस्थापन गर्न प्रयोग हुन्छ।

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
**संक्षिप्त जानकारी:** Concurrent Versions System, पुरानो version control tool।

**Example:**
```bash
cvs --help
```

**Output (sample):**
```text
Usage/help information for `cvs` (illustrative; exact output varies by distribution/version).
```

### 417. `aclocal`
**संक्षिप्त जानकारी:** autoconf का लागि M4 macros संकलन गर्छ।

**Example:**
```bash
aclocal --help
```

**Output (sample):**
```text
Usage/help information for `aclocal` (illustrative; exact output varies by distribution/version).
```

### 418. `autoheader`
**संक्षिप्त जानकारी:** configuration header template बनाउँछ।

**Example:**
```bash
autoheader --help
```

**Output (sample):**
```text
Usage/help information for `autoheader` (illustrative; exact output varies by distribution/version).
```

### 419. `autoreconf`
**संक्षिप्त जानकारी:** सबै autotools scripts पुनः generate गर्छ।

**Example:**
```bash
autoreconf --help
```

**Output (sample):**
```text
Usage/help information for `autoreconf` (illustrative; exact output varies by distribution/version).
```

### 420. `bison`
**संक्षिप्त जानकारी:** yacc-compatible parser generator।

**Example:**
```bash
bison --help
```

**Output (sample):**
```text
Usage/help information for `bison` (illustrative; exact output varies by distribution/version).
```

### 421. `expect`
**संक्षिप्त जानकारी:** interactive programs सँग automate गरी संवाद गर्ने scripting tool।

**Example:**
```bash
expect --help
```

**Output (sample):**
```text
Usage/help information for `expect` (illustrative; exact output varies by distribution/version).
```

### 422. `bzip2recover`
**संक्षिप्त जानकारी:** क्षतिग्रस्त (corrupted) bzip2 file मर्मत गर्न प्रयास गर्छ।

**Example:**
```bash
bzip2recover --help
```

**Output (sample):**
```text
Usage/help information for `bzip2recover` (illustrative; exact output varies by distribution/version).
```

### 423. `uuencode`
**संक्षिप्त जानकारी:** binary file लाई ASCII text मा encode गर्छ (email transfer का लागि)।

**Example:**
```bash
uuencode --help
```

**Output (sample):**
```text
Usage/help information for `uuencode` (illustrative; exact output varies by distribution/version).
```

### 424. `uudecode`
**संक्षिप्त जानकारी:** uuencode ले encode गरेको file फिर्ता binary मा decode गर्छ।

**Example:**
```bash
uudecode --help
```

**Output (sample):**
```text
Usage/help information for `uudecode` (illustrative; exact output varies by distribution/version).
```

### 425. `gzexe`
**संक्षिप्त जानकारी:** executable file लाई compress गर्छ (चलाउँदा auto-decompress हुन्छ)।

**Example:**
```bash
gzexe --help
```

**Output (sample):**
```text
Usage/help information for `gzexe` (illustrative; exact output varies by distribution/version).
```

### 426. `sum`
**संक्षिप्त जानकारी:** file को checksum गणना गर्छ (legacy)।

**Example:**
```bash
sum --help
```

**Output (sample):**
```text
Usage/help information for `sum` (illustrative; exact output varies by distribution/version).
```

### 427. `md5sum`
**संक्षिप्त जानकारी:** file को MD5 checksum गणना/verify गर्छ।

**Example:**
```bash
md5sum --help
```

**Output (sample):**
```text
Usage/help information for `md5sum` (illustrative; exact output varies by distribution/version).
```

### 428. `dump`
**संक्षिप्त जानकारी:** file system को backup लिन्छ (legacy)।

**Example:**
```bash
dump --help
```

**Output (sample):**
```text
Usage/help information for `dump` (illustrative; exact output varies by distribution/version).
```

### 429. `restore`
**संक्षिप्त जानकारी:** dump ले लिएको backup फिर्ता restore गर्छ।

**Example:**
```bash
restore --help
```

**Output (sample):**
```text
Usage/help information for `restore` (illustrative; exact output varies by distribution/version).
```

### 430. `rmt`
**संक्षिप्त जानकारी:** remote tape drive access गर्छ (backup का लागि)।

**Example:**
```bash
rmt --help
```

**Output (sample):**
```text
Usage/help information for `rmt` (illustrative; exact output varies by distribution/version).
```

### 431. `man`
**संक्षिप्त जानकारी:** command को विस्तृत manual/documentation हेर्न प्रयोग हुन्छ।

**Example:**
```bash
man ls
```

**Output (sample):**
```text
Interactive manual page for ls opens.
```

### 432. `info`
**संक्षिप्त जानकारी:** GNU programs को विस्तृत documentation हेर्न प्रयोग हुन्छ।

**Example:**
```bash
info coreutils 'ls invocation'
```

**Output (sample):**
```text
GNU Info documentation opens.
```

### 433. `whatis`
**संक्षिप्त जानकारी:** command को छोटो अर्थ/description देखाउँछ।

**Example:**
```bash
whatis ls
```

**Output (sample):**
```text
ls (1) - list directory contents
```

### 434. `apropos`
**संक्षिप्त जानकारी:** keyword का आधारमा सम्बन्धित manual pages खोज्छ।

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
**संक्षिप्त जानकारी:** दिइएको text लगातार output गर्छ।

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
**संक्षिप्त जानकारी:** निर्धारित समयसम्म command/script रोक्छ।

**Example:**
```bash
sleep 2
```

**Output (sample):**
```text
No output; waits for 2 seconds.
```

### 437. `bc`
**संक्षिप्त जानकारी:** terminal बाट arithmetic calculation गर्न प्रयोग हुन्छ।

**Example:**
```bash
echo '10/2' | bc
```

**Output (sample):**
```text
5
```

### 438. `clear`
**संक्षिप्त जानकारी:** terminal screen सफा गर्छ।

**Example:**
```bash
clear
```

**Output (sample):**
```text
Terminal screen is cleared.
```

### 439. `reset`
**संक्षिप्त जानकारी:** terminal को अवस्था reset गर्छ।

**Example:**
```bash
reset
```

**Output (sample):**
```text
Terminal is reset.
```

### 440. `echo`
**संक्षिप्त जानकारी:** दिइएको text वा variable को value terminal मा देखाउँछ।

**Example:**
```bash
echo 'Hello Linux'
```

**Output (sample):**
```text
Hello Linux
```

### 441. `printf`
**संक्षिप्त जानकारी:** format मिलाएर text/output देखाउँछ।

**Example:**
```bash
printf 'Name: %s\n' Prakash
```

**Output (sample):**
```text
Name: Prakash
```

### 442. `seq`
**संक्षिप्त जानकारी:** क्रमिक संख्याहरू output गर्छ।

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
**संक्षिप्त जानकारी:** पहिले चलाएका shell commands को इतिहास देखाउँछ।

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
**संक्षिप्त जानकारी:** input लाई command का arguments मा रूपान्तरण गर्छ।

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
**संक्षिप्त जानकारी:** संख्याको prime factors निकाल्छ।

**Example:**
```bash
factor 12
```

**Output (sample):**
```text
12: 2 2 3
```

### 446. `units`
**संक्षिप्त जानकारी:** विभिन्न measurement units बीच conversion गर्छ।

**Example:**
```bash
units '1 meter' 'centimeter'
```

**Output (sample):**
```text
100 centimeter
```

### 447. `script`
**संक्षिप्त जानकारी:** terminal session लाई file मा record गर्छ।

**Example:**
```bash
script session.log
```

**Output (sample):**
```text
Script started, file is session.log
```

### 448. `scriptreplay`
**संक्षिप्त जानकारी:** record गरिएको terminal session पुनः चलाउँछ।

**Example:**
```bash
scriptreplay timing.txt typescript
```

**Output (sample):**
```text
Recorded terminal session is replayed.
```

### 449. `xdg-open`
**संक्षिप्त जानकारी:** file वा URL लाई system को default application मा खोल्छ।

**Example:**
```bash
xdg-open https://example.com
```

**Output (sample):**
```text
Default browser opens.
```

### 450. `poweroff`
**संक्षिप्त जानकारी:** system बन्द गर्छ।

**Example:**
```bash
sudo poweroff
```

**Output (sample):**
```text
System powers off.
```

### 451. `access`
**संक्षिप्त जानकारी:** file/directory मा access permission जाँच गर्छ (system call wrapper)।

**Example:**
```bash
access file.txt
```

**Output (sample):**
```text
0  # accessible
```

### 452. `accton`
**संक्षिप्त जानकारी:** process accounting सक्रिय/निष्क्रिय गर्छ।

**Example:**
```bash
accton --help
```

**Output (sample):**
```text
Usage/help information for `accton` (illustrative; exact output varies by distribution/version).
```

### 453. `acpi`
**संक्षिप्त जानकारी:** battery/thermal जस्ता ACPI जानकारी देखाउँछ।

**Example:**
```bash
acpi -b
```

**Output (sample):**
```text
Battery 0: Full, 100%
```

### 454. `acpid`
**संक्षिप्त जानकारी:** ACPI events (power button, lid आदि) सुन्ने daemon।

**Example:**
```bash
acpid --help
```

**Output (sample):**
```text
Usage/help information for `acpid` (illustrative; exact output varies by distribution/version).
```

### 455. `addr2line`
**संक्षिप्त जानकारी:** memory address लाई source code को file/line मा convert गर्छ (debugging)।

**Example:**
```bash
addr2line -e app 0x401136
```

**Output (sample):**
```text
main at main.c:10
```

### 456. `agetty`
**संक्षिप्त जानकारी:** virtual console/serial line मा login prompt दिने getty को संस्करण।

**Example:**
```bash
agetty --help
```

**Output (sample):**
```text
Usage/help information for `agetty` (illustrative; exact output varies by distribution/version).
```

### 457. `amixer`
**संक्षिप्त जानकारी:** ALSA sound card को mixer settings नियन्त्रण गर्छ।

**Example:**
```bash
amixer get Master
```

**Output (sample):**
```text
Mono: Playback 80 [80%] [on]
```

### 458. `aplay`
**संक्षिप्त जानकारी:** ALSA प्रयोग गरी audio file play गर्छ।

**Example:**
```bash
aplay --list-devices
```

**Output (sample):**
```text
card 0: ...
```

### 459. `aplaymidi`
**संक्षिप्त जानकारी:** ALSA प्रयोग गरी MIDI file play गर्छ।

**Example:**
```bash
aplaymidi --help
```

**Output (sample):**
```text
Usage/help information for `aplaymidi` (illustrative; exact output varies by distribution/version).
```

### 460. `autoupdate`
**संक्षिप्त जानकारी:** configure.in फाइललाई नयाँ autoconf संस्करणमा अद्यावधिक गर्छ।

**Example:**
```bash
autoupdate --help
```

**Output (sample):**
```text
Usage/help information for `autoupdate` (illustrative; exact output varies by distribution/version).
```

### 461. `banner`
**संक्षिप्त जानकारी:** ठूला ASCII-art अक्षरहरूमा text print गर्छ।

**Example:**
```bash
banner --help
```

**Output (sample):**
```text
Usage/help information for `banner` (illustrative; exact output varies by distribution/version).
```

### 462. `biff`
**संक्षिप्त जानकारी:** नयाँ mail आउँदा notify गर्ने सेवा on/off गर्छ।

**Example:**
```bash
biff --help
```

**Output (sample):**
```text
Usage/help information for `biff` (illustrative; exact output varies by distribution/version).
```

### 463. `bzcmp`
**संक्षिप्त जानकारी:** दुई bzip2 compressed files तुलना गर्छ (bzdiff जस्तै)।

**Example:**
```bash
bzcmp --help
```

**Output (sample):**
```text
Usage/help information for `bzcmp` (illustrative; exact output varies by distribution/version).
```

### 464. `case`
**संक्षिप्त जानकारी:** shell script मा conditional branching गर्ने built-in keyword।

**Example:**
```bash
help case
```

**Output (sample):**
```text
Built-in shell command 'case'; output/behavior depends on the shell.
```

### 465. `cc`
**संक्षिप्त जानकारी:** C compiler चलाउने standard command (प्रायः gcc को alias)।

**Example:**
```bash
cc --help
```

**Output (sample):**
```text
Usage/help information for `cc` (illustrative; exact output varies by distribution/version).
```

### 466. `chvt`
**संक्षिप्त जानकारी:** अर्को virtual terminal (console) मा switch गर्छ।

**Example:**
```bash
chvt --help
```

**Output (sample):**
```text
Usage/help information for `chvt` (illustrative; exact output varies by distribution/version).
```

### 467. `cpp`
**संक्षिप्त जानकारी:** C preprocessor, macros/includes process गर्छ।

**Example:**
```bash
cpp file.c | head
```

**Output (sample):**
```text
# 1 "file.c"
```

### 468. `cupsd`
**संक्षिप्त जानकारी:** CUPS printing system को daemon।

**Example:**
```bash
cupsd --help
```

**Output (sample):**
```text
Usage/help information for `cupsd` (illustrative; exact output varies by distribution/version).
```

### 469. `dc`
**संक्षिप्त जानकारी:** reverse-Polish notation प्रयोग गर्ने calculator।

**Example:**
```bash
echo '10 2 / p' | dc
```

**Output (sample):**
```text
5
```

### 470. `dir`
**संक्षिप्त जानकारी:** directory सामग्री सूची देखाउँछ (ls को variant)।

**Example:**
```bash
dir
```

**Output (sample):**
```text
file.txt  notes.txt
```

### 471. `disable`
**संक्षिप्त जानकारी:** shell built-in commands लाई अस्थायी रूपमा निष्क्रिय गर्छ।

**Example:**
```bash
disable --help
```

**Output (sample):**
```text
Usage/help information for `disable` (illustrative; exact output varies by distribution/version).
```

### 472. `domainname`
**संक्षिप्त जानकारी:** system को NIS/YP domain नाम देखाउँछ/सेट गर्छ।

**Example:**
```bash
domainname --help
```

**Output (sample):**
```text
Usage/help information for `domainname` (illustrative; exact output varies by distribution/version).
```

### 473. `dos2unix`
**संक्षिप्त जानकारी:** DOS format (CRLF) फाइललाई Unix (LF) मा परिवर्तन गर्छ।

**Example:**
```bash
dos2unix file.txt
```

**Output (sample):**
```text
dos2unix: converting file file.txt to Unix format...
```

### 474. `dosfsck`
**संक्षिप्त जानकारी:** DOS FAT file system जाँच र मर्मत गर्छ।

**Example:**
```bash
dosfsck --help
```

**Output (sample):**
```text
Usage/help information for `dosfsck` (illustrative; exact output varies by distribution/version).
```

### 475. `exec`
**संक्षिप्त जानकारी:** हालको shell process लाई अर्को command ले replace गरेर चलाउँछ।

**Example:**
```bash
help exec
```

**Output (sample):**
```text
Built-in shell command 'exec'; output/behavior depends on the shell.
```

### 476. `fc`
**संक्षिप्त जानकारी:** अघिल्लो shell commands edit र पुनः execute गर्न प्रयोग हुन्छ।

**Example:**
```bash
fc --help
```

**Output (sample):**
```text
Usage/help information for `fc` (illustrative; exact output varies by distribution/version).
```

### 477. `fc-cache`
**संक्षिप्त जानकारी:** font cache database अद्यावधिक/पुनर्निर्माण गर्छ।

**Example:**
```bash
fc-cache -f
```

**Output (sample):**
```text
No output on success.
```

### 478. `fc-list`
**संक्षिप्त जानकारी:** system मा उपलब्ध fonts को सूची देखाउँछ।

**Example:**
```bash
fc-list | head -n 2
```

**Output (sample):**
```text
/usr/share/fonts/...: DejaVu Sans
```

### 479. `getent`
**संक्षिप्त जानकारी:** system databases बाट user, group, host आदि जानकारी निकाल्छ।

**Example:**
```bash
getent passwd root
```

**Output (sample):**
```text
root:x:0:0:root:/root:/bin/bash
```

### 480. `gs`
**संक्षिप्त जानकारी:** Ghostscript, PostScript/PDF interpret र render गर्छ।

**Example:**
```bash
gs --help
```

**Output (sample):**
```text
Usage/help information for `gs` (illustrative; exact output varies by distribution/version).
```

### 481. `hash`
**संक्षिप्त जानकारी:** shell मा प्रयोग भइसकेका commands को path cache देखाउँछ (built-in)।

**Example:**
```bash
hash --help
```

**Output (sample):**
```text
Usage/help information for `hash` (illustrative; exact output varies by distribution/version).
```

### 482. `hexdump`
**संक्षिप्त जानकारी:** file को सामग्री hexadecimal (र अन्य formats) मा देखाउँछ।

**Example:**
```bash
hexdump -C hello.txt
```

**Output (sample):**
```text
00000000  48 65 6c 6c 6f 0a  |Hello.|
```

### 483. `hostid`
**संक्षिप्त जानकारी:** system को unique 32-bit hexadecimal identifier देखाउँछ।

**Example:**
```bash
hostid
```

**Output (sample):**
```text
a1b2c3d4
```

### 484. `iconv`
**संक्षिप्त जानकारी:** text encoding परिवर्तन गर्न प्रयोग हुन्छ।

**Example:**
```bash
iconv -f UTF-8 -t UTF-16 file.txt > file16.txt
```

**Output (sample):**
```text
No output on success.
```

### 485. `import`
**संक्षिप्त जानकारी:** screen वा window को screenshot लिन्छ (ImageMagick)।

**Example:**
```bash
import --help
```

**Output (sample):**
```text
Usage/help information for `import` (illustrative; exact output varies by distribution/version).
```

### 486. `install`
**संक्षिप्त जानकारी:** file copy तथा permission सेट गर्न वा केही systems मा package installation सम्बन्धी काम गर्न प्रयोग हुन्छ।

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
**संक्षिप्त जानकारी:** IPC resources (shared memory, semaphore, message queue) हटाउँछ।

**Example:**
```bash
ipcrm --help
```

**Output (sample):**
```text
Usage/help information for `ipcrm` (illustrative; exact output varies by distribution/version).
```

### 488. `ipcs`
**संक्षिप्त जानकारी:** system का IPC resources (shared memory, semaphores) को स्थिति देखाउँछ।

**Example:**
```bash
ipcs --help
```

**Output (sample):**
```text
Usage/help information for `ipcs` (illustrative; exact output varies by distribution/version).
```

### 489. `pinky`
**संक्षिप्त जानकारी:** finger जस्तै, user बारे संक्षिप्त जानकारी देखाउँछ।

**Example:**
```bash
pinky --help
```

**Output (sample):**
```text
Usage/help information for `pinky` (illustrative; exact output varies by distribution/version).
```

### 490. `ranlib`
**संक्षिप्त जानकारी:** static library (.a) भित्र index (symbol table) बनाउँछ।

**Example:**
```bash
ranlib libdemo.a
```

**Output (sample):**
```text
No output on success.
```

### 491. `rev`
**संक्षिप्त जानकारी:** प्रत्येक लाइनको अक्षरहरूलाई उल्टो क्रममा देखाउँछ।

**Example:**
```bash
rev --help
```

**Output (sample):**
```text
Usage/help information for `rev` (illustrative; exact output varies by distribution/version).
```

---

<p align="right"><a href="#top">⬆️ सूचीमा फर्कने</a></p>

</details>

---

## ⚠️ महत्वपूर्ण नोटहरू

1. ✅ सबै 491 commands लाई PDF को numbering अनुसार समेटिएको छ।
2. 🕰️ केही commands पुराना/legacy, package-dependent, distro-specific वा विशेष hardware/service का लागि मात्र उपलब्ध हुन सक्छन्।
3. 🔄 `ifconfig`, `netstat` जस्ता केही पुराना networking utilities को आधुनिक विकल्पका रूपमा अहिले `ip` र `ss` प्रयोग गरिन्छ।
4. 🧪 `Example` र `Output` हरू अभ्यासका लागि representative हुन्; आफ्नो system मा command चलाउँदा output फरक आउन सक्छ।
5. 🛑 Destructive commands (`dd`, `mkfs`, `fdisk`, `parted`, `rm -rf`, firewall changes आदि) वास्तविक disk/server मा चलाउनु अघि command राम्ररी दोहोर्‍याएर verify गर्नुहोस्।

## 📖 Source
संलग्न `linux.pdf` — **Linux Commands Cheat Sheet: A clean and minimal guide to 491 Linux commands**।

<p align="right"><a href="#top">⬆️ माथि फर्कने</a></p>
