# IP Allow List Update Algorithm

## Project Description

This project involves an algorithm written in Python to automate the updating of an "allow_list.txt" file, which contains authorized IP addresses. The algorithm removes IP addresses listed in a "remove_list" from the allow list, thereby maintaining access control integrity.

## Project Structure

- `update_allow_list.py`: The Python script that performs the update operation on the IP allow list.

## How It Works

1. **Open the File**
   - The script opens the `allow_list.txt` file using the `with` statement for efficient resource management.

   ```python
   import_file = "allow_list.txt"

   with open(import_file, "r") as file:
       ip_addresses = file.read()

## Read the File Contents
- The .read() method converts the file's contents into a string.

  -`ip_addresses = file.read()`

## Convert String to List

- The `.split()` method converts the string of IP addresses into a list.

  `ip_addresses = ip_addresses.split()`

## Iterate Through the Remove List

- Iterate over the IP addresses to be removed.

```python
remove_list = ["192.168.1.2", "10.0.0.5"] 

for ip in remove_list:
    if ip in ip_addresses:
        ip_addresses.remove(ip)
```
## update the file

- Convert the updated list back into a string and write it to the file using the `.join()` method.

  ```python
  ip_addresses_str = "\n".join(ip_addresses)

with open(import_file, "w") as file:
    file.write(ip_addresses_str) 
    ```
## Summary

- The algorithm efficiently updates the `"allow_list.txt"` file by removing IP addresses specified in the "remove_list." The process involves reading the file, converting data to a list, removing unwanted IPs, and writing the updated list back to the file.




