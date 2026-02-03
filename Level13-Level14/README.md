# Level 13 → Level 14

## 🎯 Goal
The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Look at the commands that logged you into previous bandit levels, and find out how to use the key for this level.

## 🏁 Last Flag
 **FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn**

## 💡 Solution
For this solution, I placed the private key on my physical system.

```bash
seppevo@FedoraAsus:~$ ssh -i .ssh/sshkeyb14.private bandit14@bandit.labs.overthewire.org -p 2220
bandit14@bandit:~$ cat /etc/bandit_pass/bandit14
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
```
