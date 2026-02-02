# Level 9 → Level 10

## 🎯 Goal
The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

## 🏁 Last Flag
 **4CKMh1JI91bUIZZPXDqGanal4xvAg0JM**

## 💡 Solution

```bash
bandit9@bandit:~$ strings data.txt | grep ====
========== the
========== password
f\Z'========== is
========== FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
```
