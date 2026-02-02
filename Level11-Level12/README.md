# Level 11 → Level 12

## 🎯 Goal
The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

## 🏁 Last Flag
 **dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr**

## 💡 Solution

```bash
bandit11@bandit:~$ tr 'A-Za-z' 'N-ZA-Mn-za-m' < data.txt 
The password is 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
```
