# Linux Daily Used Commands — Category-wise Nepali Guide (Table Format)

> **नोट:** यो सूचीमा दैनिक जीवनमा सबैभन्दा धेरै प्रयोग हुने (commonly used) Linux commands मात्र categorywise table मा राखिएको छ। पूरा 491 commands को detail चाहिएमा मूल फाइल (`Linux_491_Commands...`) हेर्नुहोस्।

## 📚 Categories
- [📁 File and Directory Operations](#file-directory)
- [📝 Text Processing and Editing](#text-processing)
- [📊 System Monitoring and Management](#system-monitoring)
- [👤 User and Permission Management](#user-permission)
- [🌐 Networking and Communication](#networking)
- [💽 Disk and File System Utilities](#disk-fs)
- [📦 Compression and Archiving](#compression)
- [⚙️ Process Management](#process-management)
- [🛠️ System Configuration and Settings](#system-config)

---

<a id="file-directory"></a>
## 📁 File and Directory Operations

| Command | विवरण | Example | Output (sample) |
|---|---|---|---|
| `ls` | हालको directory भित्रका file/folder हरूको सूची देखाउँछ | `ls -la` | `drwxr-xr-x ... .` `-rw-r--r-- ... file.txt` |
| `cd` | एक directory बाट अर्को directory मा जान | `cd /var/log` | No output; directory change हुन्छ |
| `pwd` | अहिलेको working directory को पूरा path देखाउँछ | `pwd` | `/home/user` |
| `mkdir` | नयाँ directory बनाउन | `mkdir projects` | `'projects' directory बन्छ` |
| `touch` | नयाँ खाली file बनाउन वा timestamp update गर्न | `touch notes.txt` | `'notes.txt' बन्छ` |
| `cp` | file/directory copy गर्न | `cp file.txt backup.txt` | `'backup.txt' बन्छ` |
| `mv` | file/folder सार्न वा rename गर्न | `mv old.txt new.txt` | file rename हुन्छ |
| `rm` | file/directory हटाउन | `rm old.txt` | No output (success भए) |
| `cat` | file को content देखाउन | `cat hello.txt` | `Hello Linux` |
| `less` | ठूलो file scroll गरेर हेर्न | `less hello.txt` | Interactive pager खुल्छ |
| `find` | निश्चित स्थानमा file/directory खोज्न | `find . -name '*.txt'` | `./notes.txt` |
| `cp -r` | folder सहित copy गर्न | `cp -r dir1 dir2` | folder copy हुन्छ |

---

<a id="text-processing"></a>
## 📝 Text Processing and Editing

| Command | विवरण | Example | Output (sample) |
|---|---|---|---|
| `nano` | Simple text editor मा file खोल्न | `nano notes.txt` | Editor खुल्छ |
| `vi` / `vim` | Advanced text editor | `vim notes.txt` | Editor खुल्छ |
| `grep` | file भित्र pattern/text खोज्न | `grep "error" log.txt` | matching lines देखिन्छ |
| `sed` | text find & replace गर्न | `sed 's/old/new/g' file.txt` | replaced text देखिन्छ |
| `awk` | column/pattern आधारमा text process गर्न | `awk '{print $1}' file.txt` | पहिलो column print हुन्छ |
| `sort` | lines लाई sort गर्न | `sort file.txt` | sorted output |
| `uniq` | duplicate lines हटाउन | `sort file.txt \| uniq` | unique lines |
| `wc` | lines/words/characters count गर्न | `wc -l file.txt` | `25 file.txt` |
| `head` | file को सुरुका lines देखाउन | `head -n 5 file.txt` | पहिलो 5 lines |
| `tail` | file को अन्तिम lines देखाउन | `tail -n 5 file.txt` | अन्तिम 5 lines |
| `tail -f` | log file लाई real-time follow गर्न | `tail -f /var/log/syslog` | नयाँ लाइन आउँदै जान्छ |
| `diff` | दुई file बीच फरक हेर्न | `diff file1.txt file2.txt` | difference देखिन्छ |

---

<a id="system-monitoring"></a>
## 📊 System Monitoring and Management

| Command | विवरण | Example | Output (sample) |
|---|---|---|---|
| `top` | running processes को real-time view | `top` | CPU/Memory usage table |
| `htop` | interactive/graphical process monitor | `htop` | color-coded process view |
| `ps` | running processes को सूची | `ps aux` | process list |
| `free` | RAM/Memory usage हेर्न | `free -h` | `Mem: 8G 3G 5G` |
| `uptime` | system कति समयदेखि चलिरहेको छ | `uptime` | `up 3 days, load average ...` |
| `df` | disk space usage हेर्न | `df -h /` | `50G 18G 30G 38% /` |
| `du` | file/directory ले लिएको space हेर्न | `du -sh .` | `12M .` |
| `whoami` | अहिलेको login user को नाम | `whoami` | `user` |
| `date` | system को मिति र समय देखाउन | `date` | `Fri Aug 21 2026 ...` |
| `uname` | system/kernel जानकारी हेर्न | `uname -a` | kernel version info |
| `vmstat` | virtual memory statistics हेर्न | `vmstat 1` | system performance data |

---

<a id="user-permission"></a>
## 👤 User and Permission Management

| Command | विवरण | Example | Output (sample) |
|---|---|---|---|
| `sudo` | administrator (root) अधिकारमा command चलाउन | `sudo apt update` | root privilege मा execute हुन्छ |
| `su` | अर्को user मा switch गर्न | `su username` | user switch हुन्छ |
| `useradd` | नयाँ user बनाउन | `sudo useradd newuser` | user बन्छ |
| `passwd` | password परिवर्तन गर्न | `passwd` | password update हुन्छ |
| `chmod` | file/folder को permission बदल्न | `chmod 755 script.sh` | permission update हुन्छ |
| `chown` | file/folder को owner बदल्न | `chown user:group file.txt` | ownership update हुन्छ |
| `id` | user को UID/GID जानकारी | `id` | `uid=1000(user) gid=1000` |
| `groups` | user कुन group मा छ हेर्न | `groups` | group नामहरू देखिन्छ |
| `usermod` | existing user को setting बदल्न | `sudo usermod -aG sudo user` | user group मा थपिन्छ |

---

<a id="networking"></a>
## 🌐 Networking and Communication

| Command | विवरण | Example | Output (sample) |
|---|---|---|---|
| `ping` | network connectivity जाँच्न | `ping google.com` | reply from server देखिन्छ |
| `ip` | network interface/IP जानकारी हेर्न | `ip a` | IP address list |
| `ss` | network connections/ports हेर्न | `ss -tulnp` | active ports देखिन्छ |
| `curl` | URL बाट data fetch गर्न | `curl https://example.com` | webpage content |
| `wget` | file/webpage download गर्न | `wget https://example.com/file.zip` | file download हुन्छ |
| `ssh` | remote server मा secure login गर्न | `ssh user@server.com` | remote shell खुल्छ |
| `scp` | remote server मा/बाट file copy गर्न | `scp file.txt user@server:/path` | file transfer हुन्छ |
| `netstat` | network connections/statistics हेर्न (legacy) | `netstat -tulnp` | port/connection list |
| `hostname` | system को hostname हेर्न | `hostname` | `myserver` |

---

<a id="disk-fs"></a>
## 💽 Disk and File System Utilities

| Command | विवरण | Example | Output (sample) |
|---|---|---|---|
| `mount` | file system लाई attach गर्न | `sudo mount /dev/sdb1 /mnt` | drive mount हुन्छ |
| `umount` | mounted file system हटाउन | `sudo umount /mnt` | drive unmount हुन्छ |
| `fdisk` | disk partition व्यवस्थापन गर्न ⚠️ | `sudo fdisk -l` | partition list |
| `lsblk` | block devices/partitions को सूची | `lsblk` | disk/partition tree |
| `mkfs` | नयाँ file system बनाउन ⚠️ | `sudo mkfs.ext4 /dev/sdb1` | filesystem बन्छ |
| `fsck` | file system error check गर्न | `sudo fsck /dev/sdb1` | error check result |

---

<a id="compression"></a>
## 📦 Compression and Archiving

| Command | विवरण | Example | Output (sample) |
|---|---|---|---|
| `tar` | files/folders लाई archive बनाउन/खोल्न | `tar -czvf archive.tar.gz folder/` | `.tar.gz` file बन्छ |
| `zip` | file/folder लाई `.zip` मा compress गर्न | `zip -r archive.zip folder/` | `.zip` file बन्छ |
| `unzip` | `.zip` file extract गर्न | `unzip archive.zip` | files extract हुन्छन् |
| `gzip` | file compress गर्न | `gzip file.txt` | `file.txt.gz` बन्छ |
| `gunzip` | `.gz` file extract गर्न | `gunzip file.txt.gz` | original file फर्किन्छ |

---

<a id="process-management"></a>
## ⚙️ Process Management

| Command | विवरण | Example | Output (sample) |
|---|---|---|---|
| `kill` | process ID अनुसार process बन्द गर्न | `kill 1234` | process terminate हुन्छ |
| `killall` | नामबाट process बन्द गर्न | `killall firefox` | सबै matching process बन्द हुन्छ |
| `jobs` | current shell का background jobs हेर्न | `jobs` | running jobs को सूची |
| `bg` | job लाई background मा चलाउन | `bg %1` | job background मा जान्छ |
| `fg` | job लाई foreground मा ल्याउन | `fg %1` | job foreground मा आउँछ |
| `nice` | process को priority तोक्न | `nice -n 10 command` | कम priority मा चल्छ |
| `nohup` | terminal बन्द भए पनि process चलिरहन दिन | `nohup command &` | background मा चलिरहन्छ |

---

<a id="system-config"></a>
## 🛠️ System Configuration and Settings

| Command | विवरण | Example | Output (sample) |
|---|---|---|---|
| `apt` | package install/update/remove गर्न (Debian/Ubuntu) | `sudo apt install curl` | package install हुन्छ |
| `apt update` | package list अद्यावधिक गर्न | `sudo apt update` | package list refresh हुन्छ |
| `apt upgrade` | installed packages upgrade गर्न | `sudo apt upgrade` | packages upgrade हुन्छन् |
| `systemctl` | services start/stop/status गर्न | `sudo systemctl restart nginx` | service restart हुन्छ |
| `service` | service व्यवस्थापन (legacy) | `sudo service ssh status` | service को स्थिति देखिन्छ |
| `crontab` | scheduled task (cron job) व्यवस्थापन गर्न | `crontab -e` | cron editor खुल्छ |
| `env` | environment variables हेर्न | `env` | सबै environment variables |
| `export` | environment variable set गर्न | `export PATH=$PATH:/new/path` | variable update हुन्छ |
| `alias` | command को shortcut बनाउन | `alias ll='ls -la'` | shortcut बन्छ |
| `history` | अघि चलाइएका commands हेर्न | `history` | command history list |
| `reboot` | system restart गर्न ⚠️ | `sudo reboot` | system restart हुन्छ |
| `shutdown` | system बन्द गर्न ⚠️ | `sudo shutdown now` | system बन्द हुन्छ |

---

## ⚠️ महत्वपूर्ण नोट
1. यो सूची **daily/commonly used commands** मा केन्द्रित छ, पूरा 491 commands होइन।
2. `sudo`, `rm`, `dd`, `mkfs`, `fdisk`, `shutdown`, `reboot` जस्ता destructive/critical commands प्रयोग गर्दा सावधानी अपनाउनुहोस्।
3. `Example` र `Output` हरू सिकाइका लागि illustrative छन्; वास्तविक output distro/version अनुसार फरक हुन सक्छ।

## 📖 Source
मूल आधार: `Linux_491_Commands_Nepali_Category_Example_Output.md` फाइल — यसैबाट दैनिक चलाइने commands छानेर table format मा तयार गरिएको।
