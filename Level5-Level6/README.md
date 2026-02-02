# Level 5 → Level 6

## 🎯 Goal
The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:

    human-readable
    1033 bytes in size
    not executable


## 🏁 Last Flag
 **4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw**

## 💡 Solution

```bash
bandit5@bandit:~/inhere$ find . -type f -size 1033c ! -executable
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG

```
