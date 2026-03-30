# 07 - Update a File Through a Python Algorithm

## Project Description

In this project, I developed a Python algorithm to automate the process of updating an IP address allow list (`allow_list.txt`). The file contains IP addresses authorized to access restricted content. The algorithm reads the file, removes IP addresses that appear on a separate remove list, and writes the updated list back to the file.

## Skills Demonstrated

- Opening and reading files in Python using `with` and `open()`
- Converting strings to lists using `.split()`
- Iterating through lists using `for` loops
- Removing items from a list using `.remove()`
- Writing updated content back to a file using `.write()` and `.join()`

## Algorithm Overview

```python
# Assign file name
import_file = "allow_list.txt"

# Open and read the file
with open(import_file, "r") as file:
    ip_addresses = file.read()

# Convert string to list
ip_addresses = ip_addresses.split()

# Remove IP addresses on the remove list
for element in remove_list:
    if element in ip_addresses:
        ip_addresses.remove(element)

# Convert list back to string and update the file
ip_addresses = "\n".join(ip_addresses)

with open(import_file, "w") as file:
    file.write(ip_addresses)
```

## Files

| File | Description |
|------|-------------|
| `Algorithm-for-file-updates-in-Python.docx` | Full portfolio document with explanations and code |

## Course

[Google Cybersecurity Professional Certificate](https://www.coursera.org/professional-certificates/google-cybersecurity) — Coursera  
Course 7: Automate Cybersecurity Tasks with Python
