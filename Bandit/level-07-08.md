**Objective:** The password for the next level is stored in the file **data.txt** next to the word **millionth**

**What I tried first:**
- `cat` — massive output
- I figured out that I have to filter out the line that contains 'millionth' using `grep`

**What worked:**

```bash
grep "millionth" data.txt
# output: [redacted]
```

**Why it worked:** `grep` can filter out and display specific patterns in a file.