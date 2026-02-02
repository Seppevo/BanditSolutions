# Level 4 → Level 5

## 🎯 Goal
The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.

## 🏁 Last Flag
 **2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ**

## 💡 Solution

```bash
bandit4@bandit:~/inhere$ ls -l
total 40
-rw-r----- 1 bandit5 bandit4 33 Oct 14 09:26 -file00
-rw-r----- 1 bandit5 bandit4 33 Oct 14 09:26 -file01
-rw-r----- 1 bandit5 bandit4 33 Oct 14 09:26 -file02
-rw-r----- 1 bandit5 bandit4 33 Oct 14 09:26 -file03
-rw-r----- 1 bandit5 bandit4 33 Oct 14 09:26 -file04
-rw-r----- 1 bandit5 bandit4 33 Oct 14 09:26 -file05
-rw-r----- 1 bandit5 bandit4 33 Oct 14 09:26 -file06
-rw-r----- 1 bandit5 bandit4 33 Oct 14 09:26 -file07
-rw-r----- 1 bandit5 bandit4 33 Oct 14 09:26 -file08
-rw-r----- 1 bandit5 bandit4 33 Oct 14 09:26 -file09
bandit4@bandit:~/inhere$ file ./*
./-file00: data
./-file01: OpenPGP Public Key
./-file02: OpenPGP Public Key
./-file03: data
./-file04: data
./-file05: data
./-file06: data
./-file07: ASCII text
./-file08: data
./-file09: data
bandit4@bandit:~/inhere$ cat ./-file07
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
```
