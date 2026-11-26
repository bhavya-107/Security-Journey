**Objective:** Read a file whose name contains spaces.

**What I tried first:**
- `cat spaces in here` — shell split it into three arguments; `cat` tried
  to open three files that don't exist.

**What worked:**

```bash
cat "spaces in here"
# output: [redacted]
```

**Why it worked:** Quotes group the words into one argument, hence it is considered as a filename.