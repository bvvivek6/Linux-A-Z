# 08. Text Processing & Redirection

The real power of Linux comes from chaining commands together.

## Pipes (`|`)

Pass the output of one command as input to another.

```bash
ls -la | grep "txt"  # List files, then find lines containing "txt"
cat file.txt | less  # Read file, then open in pager
```

## Redirection (`>`, `>>`)

Save output to a file.

- `>`: **Overwrite**. Replaces file content.
- `>>`: **Append**. Adds to the end of the file.

```bash
echo "Hello" > file.txt   # file.txt now contains "Hello"
echo "World" >> file.txt  # file.txt now contains "Hello\nWorld"
```

## Grep (Global Regular Expression Print)

Search for text within files.

```bash
grep "error" server.log          # Find "error" in server.log
grep -r "config" /etc/           # Recursive search in /etc/
grep -i "User" file.txt          # Case-insensitive search
```

## Sed (Stream Editor)

Find and replace text.

```bash
sed 's/old/new/' file.txt        # Replace first "old" with "new" (prints to screen)
sed -i 's/old/new/g' file.txt    # Replace ALL "old" with "new" inside the file (-i = in-place)
```

## Awk

Powerful text processing tool for columns of data.

```bash
# Print the first column of a file
awk '{print $1}' data.txt

# Print the user (1st col) and shell (7th col) from /etc/passwd
awk -F: '{print $1, $7}' /etc/passwd
```
