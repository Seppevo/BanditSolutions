# Level 8 → Level 9

## 🎯 Goal
The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

## 🏁 Last Flag
 **dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc**

## 💡 Solution

```bash
bandit8@bandit:~$ cat data.txt | sort | uniq -u
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM

```
