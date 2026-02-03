# Level 15 → Level 16

## 🎯 Goal
The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL/TLS encryption.

## 🏁 Last Flag
 **8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo**

## 💡 Solution

```bash
bandit15@bandit:~$ openssl s_client -connect localhost:30001
.....
.....
---
read R BLOCK
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
Correct!
kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx
```
