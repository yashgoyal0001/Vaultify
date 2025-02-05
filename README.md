**Vaultify - Intelligent File Organizer & Integrity Checker**

Vaultify is a Python-based tool designed to automate file organization, verify data integrity using MD5 checksums, and manage archival storage. It ensures that files are accurately sorted based on their extensions while preventing corruption through checksum verification.

**Features**

✅ Automated File Sorting – Organizes files into extension-based folders
✅ MD5 Checksum Verification – Ensures file integrity before moving
✅ Archival Management – Moves files to an archive before final placement
✅ Custom Configuration – Reads source, destination, and archive paths from a configuration file

**Installation**

**Prerequisites**

Python 3.x must be installed.

**Usage**

**Configure Paths:** 

Edit path.txt and add the source, destination, and archive directories.

**Run the script:**

python main.py

**Process Overview:**

Files are scanned from the source directory.

An .ftsinf file is generated containing username, filename, file size, and MD5 checksum.

Files and their .ftsinf metadata are moved to the archive.

A second checksum verification is performed before placing the file in the correct directory.

If the checksum fails, the file is not moved further.

**How It Works:**

Generate .ftsinf metadata file alongside the original file.

Move files and metadata to the archive.

Recalculate checksum in the archive.

If checksum matches, move file to its respective extension folder.

If checksum fails, do nothing (prevents file corruption).

Example .ftsinf File

Username: your_username
Filename: example.txt
Size: 1024 bytes
Checksum: a5f3c6a11b03839d46af9fb43c97c188...

**Contributing:**

Contributions are welcome! Feel free to fork the repository and submit pull requests.

**License:**

This project is licensed under the MIT License.

⭐ Vaultify - Secure & Smart File Organization! 🚀

