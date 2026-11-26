**Objective:** Read a file named `-` in the home directory.

**What I tried first:**
- `cat -` — hung, waiting on stdin. `-` is a convention meaning "read from standard input," so `cat` ignored the file and waited for me to type.
- `cat "-"` — same result. Quoting doesn't help because the shell passes `-` through and `cat` still interprets it as stdin.

**What worked:**

```bash
cat ./-
# output: [redacted]
```

**Why it worked:** 
Prefixing with `./` makes the argument an explicit  
_path_ (`./-` = "the file named `-` in the current directory"), so `cat`  treats it as a filename instead of the stdin convention.