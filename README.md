# MirrorMate

MirrorMate is a simple command-line tool for mirroring websites and downloading files. It utilizes `wget` to perform these tasks, making it easy to retrieve entire sites or specific files.

## Table of Contents
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
  - [Command Line Interface](#command-line-interface)
  - [Importing as a Module](#importing-as-a-module)
- [Command Line Options](#command-line-options)
- [Example Commands](#example-commands)
- [License](#license)

## Features
- Mirror entire websites.
- Download single files from specified URLs.
- Simple command-line interface.
- Silent mode for background operations.

## Installation
To install MirrorMate, run the following command:

```bash
pip install mirrormate
```

Make sure you have `wget` installed on your system. You can install it using:

- **For Debian/Ubuntu**:
  ```bash
  sudo apt-get install wget
  ```
  
- **For macOS** (using Homebrew):
  ```bash
  brew install wget
   ```

## Usage

### Command Line Interface

You can use MirrorMate directly from the command line:

```bash
mirrormate --mirror https://example.com
```

This command will mirror the specified website.

### Importing as a Module

You can also use MirrorMate as a Python module in your scripts:

```python
import mirrormate

# To mirror a website
if mirrormate.clone(url="https://example.com", silent=False):
    print("Successfully mirrored the website.")
else:
    print("Not downloadable.")

# To download a single file
if mirrormate.clone(file_url="https://example.com/file.py", silent=False):
    print("Successfully downloaded the file.")
else:
    print("Not downloadable.")
```

## Command Line Options
- `--help`: Show help message and exit.
- `--mirror <url>`: URL to mirror.
- `--copy <file_url>`: Single file URL to download.

### Example Commands
- To display help information:
  ```bash
  mirrormate --help
  ```

- To mirror a website:
  ```bash
  mirrormate --mirror https://example.com
  ```

- To download a single file:
  ```bash
  mirrormate --copy https://example.com/index.html
  ```

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
