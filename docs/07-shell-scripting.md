# 07. Shell Scripting Basics

Automate boring tasks with Shell Scripts! A shell script is just a file containing a series of commands.

## The Shebang (`#!`)

Every script starts with a "Shebang". It tells the system which interpreter to use.

```bash
#!/bin/bash
echo "Hello, World!"
```

1.  Create file: `touch script.sh`
2.  Add content above.
3.  Make executable: `chmod +x script.sh`
4.  Run it: `./script.sh`

## Variables

```bash
NAME="Alice"
echo "Hello, $NAME"
```

- **Note:** No spaces around `=`.

## Loops

### For Loop

Run a command multiple times.

```bash
for i in {1..5}
do
   echo "Number: $i"
done
```

## Conditionals (If/Else)

Make decisions.

```bash
if [ -f "file.txt" ]; then
    echo "File exists."
else
    echo "File not found."
fi
```

## Functions

Group commands together.

```bash
greet() {
    echo "Hello, $1!"
}

greet "Bob"
```

## Common Exit Codes

- `0`: Success.
- `1` (or non-zero): Error.
- Check last exit code with `echo $?`.
