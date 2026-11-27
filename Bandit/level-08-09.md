**Objective:** The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once

**What I tried first:**
- `uniq -u data.txt` — it showed a lot of lines, clearly not what I needed because the objective says the line occurs only once.
- I figured out that `uniq -u` can only show unique lines if the duplicate line are adjacent, which was not this case.
- So I used `uniq` along with the `sort` command.
- To use both the commands together, I used a `|` pipeline.

**What worked:**

```bash
sort data.txt | uniq -u
# output: [redacted]
```

**Why it worked:** The `sort` command will first sort the file which means the duplicates lines will now be adjacent. This gives a green signal to my previous `uniq -u` command and it only shows the line that occurs once in the file.