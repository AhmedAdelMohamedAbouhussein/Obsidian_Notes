A **regular expression**  is a sequence of characters that defines a **search pattern**. It’s mainly used for **matching, searching, and manipulating text**.

Regex uses symbols to express rules:
 - `.` → Matches any single character except newline
 - `*` → Matches 0 or more of the preceding element
 - `+` → Matches 1 or more of the preceding element
 - `?` → Matches 0 or 1 of the preceding element
 - `^` → Matches the start of a line
 - `$` → Matches the end of a line
 - `[abc]` → Matches any one character in the brackets (a, b, or c)
 - `[^abc]` → Matches any character except a, b, or c
 - `(pattern)` → Groups multiple characters or expressions
 - `|` → Acts as OR between patterns

Examples:
- `.` → `a.c` matches `"abc"`, `"a1c"`, `"a-c"`
- `*` → `ab*` matches `"a"`, `"ab"`, `"abb"`, `"abbb"`
- `+` → `ab+` matches `"ab"`, `"abb"`, `"abbb"` (but not `"a"`)
- `?` → `colou?r` matches `"color"` or `"colour"`
- `^` → `^Hello` matches `"Hello world"` but not `"Say Hello"`
- `$` → `world$` matches `"Hello world"` but not `"world peace"`
- `[abc]` → `[abc]at` matches `"aat"`, `"bat"`, `"cat"`
- `[^abc]` → `[^abc]at` matches `"dat"`, `"eat"`, `"fat"`
- `(pattern)` → `(abc)+` matches `"abc"`, `"abcabc"`, `"abcabcabc"`
- `|` → `cat|dog` matches `"cat"` or `"dog"`

**grep**
`grep` (Global Regular Expression Print) is a **Linux command-line tool** used to **search for text patterns in files** — and it uses **regex** internally.

**Basic Syntax** : grep [options] 'pattern' filename

For example, the command  
`grep "error" logfile.txt`  
searches through the file named **logfile.txt** and prints all lines that contain the word **“error”**.

