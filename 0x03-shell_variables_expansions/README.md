# 0x03. Shell, init files, variables and expansions

## Description

This project focuses on shell initialization files, creating and manipulating environment/local variables, working with aliases, and performing arithmetic and string expansions using the Bash shell.

Each task is a small script showcasing a specific concept in shell scripting.

---

## Tasks

### 0. `<o>`

**File:** `0-alias`
Defines an alias `ls` that deletes all files in the current directory:

```bash
alias ls='rm *'
```

---

### 1. Hello you

**File:** `1-hello_you`
Prints `hello <current_user>` using:

```bash
echo "hello $(whoami)"
```

---

### 2. The path to success...

**File:** `2-path`
Adds `/action` to the end of the `PATH` environment variable:

```bash
export PATH="$PATH:/action"
```

---

### 3. If the path be beautiful...

**File:** `3-paths`
Counts the number of directories in the `PATH`:

```bash
echo "$PATH" | tr ':' '\n' | grep -v '^$' | wc -l
```

---

### 4. Global variables

**File:** `4-global_variables`
Lists all global environment variables:

```bash
printenv
```

---

### 5. Local variables

**File:** `5-local_variables`
Lists all local variables, environment variables, and functions:

```bash
set
```

---

### 6. Local variable

**File:** `6-create_local_variable`
Creates a local variable `BEST` with value `School`:

```bash
BEST="School"
```

---

### 7. Global variable

**File:** `7-create_global_variable`
Creates a global variable `BEST` with value `School`:

```bash
export BEST="School"
```

---

### 8. Every addition to true knowledge...

**File:** `8-true_knowledge`
Adds 128 to the value in `TRUEKNOWLEDGE`:

```bash
echo $((TRUEKNOWLEDGE + 128))
```

---

### 9. Divide and rule

**File:** `9-divide_and_rule`
Divides `POWER` by `DIVIDE`:

```bash
echo $((POWER / DIVIDE))
```

---

### 10. Love is anterior to life...

**File:** `10-love_exponent_breath`
Raises `BREATH` to the power of `LOVE`:

```bash
echo $((BREATH ** LOVE))
```

---

### 11. Binary to decimal

**File:** `11-binary_to_decimal`
Converts binary in `BINARY` to decimal:

```bash
echo "$((2#$BINARY))"
```

---

### 12. Combination

**File:** `12-combinations`
Prints all combinations of two lowercase letters except `oo`:

```bash
#!/bin/bash
for l1 in {a..z}; do for l2 in {a..z}; do [[ "$l1$l2" != "oo" ]] && echo "$l1$l2"; done; done
```

---

### 13. Floats

**File:** `13-print_float`
Prints the value of `NUM` with two decimal places:

```bash
printf "%.2f\n" "$NUM"
```

---

## Usage

To run a script, give it execute permission and run it:

```bash
chmod +x 1-hello_you
./1-hello_you
```

Some scripts require environment variables:

```bash
export TRUEKNOWLEDGE=1209
./8-true_knowledge
```

