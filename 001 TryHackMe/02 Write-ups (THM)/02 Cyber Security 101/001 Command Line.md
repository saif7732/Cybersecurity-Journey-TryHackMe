# Locker Authentication Script – Shell Scripting Write-up

## Overview
This task demonstrates how **variables, loops, and conditional statements** can be combined in a Bash script to implement a simple authentication system.

The script simulates a **bank locker security system** where a user must provide the correct credentials to access their locker.

---

# Objective
Create a shell script that:

- Asks the user for three inputs:
  - Username
  - Company Name
  - PIN
- Verifies the entered credentials
- Grants or denies access based on correctness.

---

# Expected Credentials

| Field | Correct Value |
|------|------|
| Username | John |
| Company Name | Tryhackme |
| PIN | 7385 |

---

# Script Implementation

```bash
#!/bin/bash 

# Defining the variables
username=""
companyname=""
pin=""

# Defining the loop
for i in {1..3}; do

    # Conditional statements
    if [ "$i" -eq 1 ]; then
        echo "Enter your Username:"
        read username

    elif [ "$i" -eq 2 ]; then
        echo "Enter your Company name:"
        read companyname

    else
        echo "Enter your PIN:"
        read pin
    fi

done

# Credential verification
if [ "$username" = "John" ] && [ "$companyname" = "Tryhackme" ] && [ "$pin" = "7385" ]; then
    echo "Authentication Successful. You can now access your locker, John."
else
    echo "Authentication Denied!!"
fi
```
---
## output in terminal:

<img width="574" height="204" alt="image" src="https://github.com/user-attachments/assets/41bc16bd-73be-41fa-9f36-d14943301c1f" />


