# Linux Commands - छोटो परिचय सहित विस्तृत जानकारी

तपाईंलाई Linux थाहा छैन भन्नुभयो, त्यसैले हरेक command लाई सजिलो भाषामा उदाहरण सहित व्याख्या गर्दैछु।

## १. User र System जानकारी

**sudo su** — Administrator (root) प्रयोगकर्तामा switch गर्न प्रयोग हुन्छ। यसले तपाईंलाई सम्पूर्ण अधिकार दिन्छ (जस्तै Windows मा "Run as Administrator")।
```
sudo su
[Password]: तपाईंको password हाल्नुहोस्
```

**whoami** — अहिले कुन user ले login गरेको छ भनेर देखाउँछ।
```
$ whoami
saroj
```

**pwd** (Print Working Directory) — अहिले तपाईं कुन folder मा हुनुहुन्छ भनेर देखाउँछ।
```
$ pwd
/home/saroj
```

## २. Folder हेर्ने र जाने

**ls** — हालको folder भित्रका file/folder हरूको list देखाउँछ।
```
$ ls
Documents  Downloads  Pictures
```

**ls -l** — Detail सहित list (permission, size, date, owner)।
```
$ ls -l
drwxr-xr-x 2 saroj saroj 4096 Aug 10 10:00 Documents
```

**ls -a** — Hidden file हरू (जसको नाम `.` बाट सुरु हुन्छ) समेत देखाउँछ।
```
$ ls -a
.  ..  .bashrc  Documents
```

**ls -c** — File को change time (metadata परिवर्तन भएको समय) अनुसार sort गरेर देखाउँछ।

**cd <directory>** — अर्को folder मा जान (Change Directory)।
```
$ cd Documents
```

**cd ..** — "अघिल्लो (parent) folder" मा फर्कन प्रयोग हुन्छ।
```
$ cd ..
```
यसले एक तह माथिको folder मा लैजान्छ।

**cd /** — Root directory मा जान प्रयोग हुन्छ। (Windows मा root drive जान `cd\` प्रयोग हुन्छ, तर Linux मा भने root मा जान `cd /` लेखिन्छ)।

## ३. File हेर्ने

**cat <file_name>** — File को सम्पूर्ण content एकैचोटि screen मा देखाउँछ।
```
$ cat notes.txt
```

**more <file_name>** — ठूलो file लाई page-by-page (एक screen जति) देखाउँछ, Space थिचेर अगाडि जान सकिन्छ। यसमा पछाडि फर्किन मिल्दैन।

**less <file_name>** — `more` जस्तै तर अझ powerful — अगाडि/पछाडि दुवैतिर scroll गर्न मिल्छ (arrow keys ले)। ठूला files पढ्न उत्तम। बाहिर निस्कन `q` थिच्नुहोस्।

## ४. File/Folder बनाउने र सम्पादन गर्ने

**touch <file_name>** — खाली नयाँ file बनाउँछ (वा existing file भए timestamp मात्र update गर्छ)।
```
$ touch notes.txt
```

**nano <file_name>** — Terminal भित्रैको सजिलो text editor, file खोल्न/सम्पादन गर्न प्रयोग हुन्छ। Save गर्न `Ctrl+O`, बाहिर निस्कन `Ctrl+X`।
```
$ nano notes.txt
```

**mv <file_name> <destination>** — File सार्न (move) प्रयोग हुन्छ। गन्तव्य folder दिनुपर्छ।
```
$ mv notes.txt Documents/
```

**cp <file_name> <destination>** — File copy गर्न। गन्तव्य दिनुपर्छ।
```
$ cp notes.txt Documents/notes_backup.txt
```

**mv <original_file_name> <new_file_name>** — यही `mv` कमाण्डले नाम पनि बदल्न सकिन्छ (rename)।
```
$ mv old.txt new.txt
```

**mkdir <directory>** — नयाँ folder बनाउँछ (Make Directory)।
```
$ mkdir Projects
```

## ५. मेटाउने

**rm <file_name>** — File मेटाउँछ (सावधान: Recycle Bin मा जाँदैन, सिधै delete हुन्छ)।
```
$ rm notes.txt
```

**rmdir <directory>** — खाली folder मेटाउँछ। भित्र केही भए काम गर्दैन (त्यसका लागि `rm -r` चाहिन्छ)।
```
$ rmdir EmptyFolder
```

## ६. जानकारी र खोज

**stat <file_name>** — File को विस्तृत जानकारी (size, permission, created/modified time) देखाउँछ।
```
$ stat notes.txt
```

**echo "<text>"** — Screen मा text print गर्छ। Script मा message देखाउन धेरै प्रयोग हुन्छ। File मा content लेख्न पनि प्रयोग हुन्छ।
```
$ echo "Hello Nepal"
Hello Nepal

$ echo "data" > file.txt
```

**grep "<text>" <file_name>** — File भित्र specific शब्द/text खोज्न प्रयोग हुन्छ।
```
$ grep "error" logfile.txt
```

## ७. System Update गर्ने (Ubuntu/Debian based)

**sudo apt update** — Software को नयाँ version को list (repository info) update गर्छ, वास्तवमा install भने गर्दैन।

**sudo apt full-upgrade** — Installed सबै software लाई नयाँ version मा upgrade गर्छ, आवश्यक भए पुराना package हटाएर पनि।

**sudo apt update && sudo apt upgrade -y && reboot** — तीनवटा काम एकैपटक गर्छ:
- Update list ल्याउँछ
- `-y` ले automatically "yes" भन्छ र upgrade गर्छ
- System restart (reboot) गर्छ

`&&` को अर्थ हो — अघिल्लो command सफल भयो भने मात्र अर्को चल्छ।

## ८. `less` को Important Keys

| Key | काम |
|---|---|
| `q` | Exit गर्न |
| `Space` | अर्को page |
| `b` | अघिल्लो page |
| `↑` | एक line माथि |
| `↓` | एक line तल |
| `g` | File को सुरुमा जान |
| `G` | File को अन्त्यमा जान |
| `/word` | "word" खोज्न (forward search) |
| `n` | अर्को search result मा जान |
