
**Objective:** Log in as `bandit0`, read the `readme` file in the home
directory, use its contents as the password for `bandit1`.
**Setup:**
```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
# password: bandit0
```

**What I tried first:**

`cat readme` — worked immediately. This level is deliberately trivial; the real lesson is the SSH connection syntax (`-p 2220`) and that the password is the _contents_ of the file, not the filename.

**What worked:**

```
ls
cat readme
# output: [redacted]
```

**Why it worked:** 

`cat` prints file contents to stdout. The password for  
the next level is literally the file's contents.
