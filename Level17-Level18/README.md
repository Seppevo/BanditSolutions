# Level 17 → Level 18

## 🎯 Goal
The password for the next level is There are 2 files in the homedirectory: passwords.old and passwords.new. The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

## 🏁 Last Flag
 **kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx**

## 💡 Solution
I used the private key to login 

```bash
bandit17@bandit:~$ diff -b passwords.old passwords.new 
42c42
< pGozC8kOHLkBMOaL0ICPvLV1IjQ5F1VA
---
> x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO

```
Since i put the .new as second the flag is the second one