# backupToZip.py

**Backup to Zip Script**
=========================

This Python script, `backupToZip.py`, is designed to backup an entire folder and its contents into a zip file. The script automatically increments the filename of the zip file if a file with the same name already exists.

**Functionality**

1. The script takes a folder path as input and ensures it is an absolute path using `os.path.abspath()`.
2. It determines the filename for the zip file by appending a number to the base folder name. If a file with the same name already exists, it increments the number until a unique filename is found.
3. The script creates a new zip file with the determined filename using `zipfile.ZipFile`.
4. It uses `os.walk()` to traverse the entire folder tree, compressing files in each subfolder.
5. For each file, it checks if the file is a backup zip file (i.e., starts with the base folder name and ends with `.zip`) and skips