# Level 6 → Level 7

## 🎯 Goal
The password for the next level is stored somewhere on the server and has all of the following properties:

    owned by user bandit7
    owned by group bandit6
    33 bytes in size

## 🏁 Last Flag
 **HWasnPhtq9AVKe0dmk45nxy20cvUa6EG**

## 💡 Solution

```bash
bandit6@bandit:~$ find / -size 33c -group bandit6 -user bandit7 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj

```
