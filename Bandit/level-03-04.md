**Objective:** Find the password in the `inhere/` directory. The file is hidden.

**What I tried first:**
- `ls inhere/` — showed nothing useful because the file starts with `.`  and `ls` hides dotfiles by default.

**What worked:**
```bash
cd inhere
ls -la
cat .Hiding-From-You
# output: [redacted]
```

**Why it worked:** 
`-a` includes entries starting with `.`; `-l` gives  
details. Dotfiles are hidden by convention, not by permission — anyone with read access can open them.