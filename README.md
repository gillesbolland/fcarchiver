# fcarchiver

fcarchiver is a Bash script designed to automate the process of creating a Final Cut Pro archive for a specified directory. It scans the directory for supported media files, generates a plist file (`FCArchMetadata.plist`) with necessary metadata, and optionally adjusts file creation dates based on file content or metadata.

## Features

- Automatically generates a plist file (`FCArchMetadata.plist`) required by Final Cut Pro.
- Extracts creation dates from filenames or uses `mediainfo` to obtain metadata if available.
- Supports renaming the directory to `.fcarch` format and setting creation dates to reflect the oldest file's date (optional).
- Allows disabling date extraction and file modification with the `--notouching` option.

## Installation

### Prerequisites

Before running `fcarchiver`, ensure you have the following dependencies installed on your system:

- `uuidgen`: To generate unique identifiers for files and directories.
- `mediainfo`: To extract creation dates from media files.

1. **Install Homebrew (if not already installed):**

   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

2. **Install `uuidgen` and `mediainfo` using Homebrew:**

   ```bash
   brew install ossp-uuid mediainfo

3. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/fcarchiver.git
   cd fcarchiver

4. **Make the script executable:**

   ```bash
   chmod +x fcarchiver

5. **Run fcarchiver:**
    Now you can run `fcarchiver` with the desired directory path:

   ```bash
    ./fcarchiver /path/to/your/directory