# Level 10 → Level 11

## 🎯 Goal
The password for the next level is stored in the file data.txt, which contains base64 encoded data

## 🏁 Last Flag
 **FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey**

## 💡 Solution

```bash
bandit10@bandit:~$ cat data.txt | base64 -d
The password is dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
```
