# Pinterest Image Scraper

<div align="center">

### 🖼️ Image Scraping | 🤖 Automation | 🔍 Duplicate Detection

**Python script for automated Pinterest image scraping with duplicate removal**

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Prerequisites](#-prerequisites)
- [Setup](#-setup)
- [Usage](#-usage)
- [How It Works](#-how-it-works)
- [Technologies Used](#-technologies-used)
- [Important Notes](#-important-notes)
- [Disclaimer](#-disclaimer)

---

## 🎯 Overview

This Python script automates the process of scraping and downloading images from Pinterest. It utilises search terms derived from the names of the deepest subdirectories within a specified base directory, ensuring a topic-specific collection of images. Additionally, the script includes functionality to remove duplicate images based on content hashing, maintaining a unique set of images in each directory.

### Use Cases

- **Dataset Creation**: Collect images for machine learning datasets
- **Content Curation**: Gather images for specific topics or themes
- **Research**: Collect visual data for research purposes
- **Automation**: Streamline image collection workflows

---

## ✨ Features

- **🔄 Automatic Image Downloading**: Downloads images from Pinterest based on directory-derived search terms
- **🔍 Duplicate Removal**: Ensures all downloaded images are unique within their respective directories using content hashing
- **⚡ Multi-threading Support**: Allows for faster downloads by leveraging multiple threads
- **🌐 Proxy Support**: Capable of using proxy lists to bypass network restrictions or for privacy reasons
- **📁 Directory-Based Organisation**: Automatically organises images by topic based on directory structure

---

## 🛠️ Prerequisites

- **Python 3.x** — Python 3.6 or higher
- **pinscrape** — Pinterest scraping library

---

## 🚀 Setup

### Installation

1. **Ensure Python 3.x is installed:**
   ```bash
   python --version
   ```

2. **Install the pinscrape module:**
   ```bash
   pip install pinscrape
   ```

3. **Clone or download this repository:**
   ```bash
   git clone https://github.com/MatthewPaver/pinterest-image-scraper.git
   cd pinterest-image-scraper
   ```

---

## 📖 Usage

### Basic Usage

1. **Configure the base directory:**
   - Open `Pinterest image scraper.py` in a text editor
   - Set the `base_directory` variable to the path of your base directory containing the deepest subdirectories for which you want to download images

2. **Run the script:**
   ```bash
   python "Pinterest image scraper.py"
   ```

3. **Process:**
   - The script will automatically process each deepest subdirectory
   - Uses the subdirectory name as a search term to download images from Pinterest
   - Saves images in the same subdirectory
   - Removes duplicates based on content hashing

### Example Directory Structure

```
base_directory/
├── topic1/
│   └── images/          # Images downloaded here
├── topic2/
│   └── images/          # Images downloaded here
└── topic3/
    └── images/          # Images downloaded here
```

---

## 🔄 How It Works

### Step 1: Directory Scanning

- Scans the base directory to identify the deepest subdirectories
- Uses subdirectory names as search terms for Pinterest

### Step 2: Image Scraping

- For each subdirectory:
  - Uses the directory name as a Pinterest search query
  - Downloads images using the `pinscrape` library
  - Saves images to the respective directory

### Step 3: Duplicate Removal

- Calculates content hash for each downloaded image
- Compares hashes to identify duplicates
- Removes duplicate images, keeping only unique ones

### Step 4: Multi-threading

- Uses multiple threads for parallel downloading
- Significantly improves download speed
- Configurable thread count

### Step 5: Proxy Support (Optional)

- Can use proxy lists for:
  - Bypassing rate limits
  - Privacy protection
  - Network restrictions

---

## 💻 Technologies Used

<div align="center">

**🐍 Python** **🖼️ pinscrape** **🔍 Content Hashing** **⚡ Multi-threading**

</div>

### Key Libraries

- **pinscrape** — Pinterest scraping library
- **Python Standard Library** — File operations, hashing, threading

---

## ⚠️ Important Notes

### Performance

- **Efficiency**: Download speed varies based on:
  - Number of threads configured
  - Use of proxies
  - Network connection speed
  - Pinterest rate limits

### Processing Time

- **Duplicate Removal**: The script removes duplicates post-download, which may slightly extend the overall processing time
- **Content Hashing**: Hash calculation adds processing overhead but ensures accurate duplicate detection

### Permissions

- **Legal Compliance**: Ensure you have the necessary permissions to scrape and download images from Pinterest
- **Terms of Service**: Review Pinterest's terms of service before use

---

## 🔒 Disclaimer

**This script is provided for educational and research purposes only.**

### Important Considerations

- **Terms of Service**: Always respect Pinterest's terms of service
- **Image Rights**: Ensure you have the right to download and use the images
- **Copyright**: Respect copyright and intellectual property rights
- **Rate Limiting**: Be mindful of Pinterest's rate limits and usage policies
- **Ethical Use**: Use responsibly and ethically

### Legal Notice

The authors and contributors of this script are not responsible for any misuse or violation of terms of service. Users are solely responsible for ensuring their use complies with all applicable laws and terms of service.

---

## 🔧 Configuration

### Customising Thread Count

Modify the thread count in the script to balance speed and resource usage:

```python
# Example: Set number of threads
thread_count = 4  # Adjust based on your system
```

### Proxy Configuration

To use proxies, configure proxy lists in the script:

```python
# Example: Proxy list configuration
proxy_list = [
    "proxy1:port",
    "proxy2:port",
    # Add more proxies as needed
]
```

---

## 📝 Notes

- **Directory Names**: Ensure directory names are descriptive and suitable as search terms
- **Image Quality**: Image quality and quantity depend on Pinterest's search results
- **Storage**: Ensure sufficient disk space for downloaded images
- **Network**: Stable internet connection recommended for best results

---

## 📄 License

This project is provided for educational and research purposes only.

---

<div align="center">

**Automated Pinterest Image Scraping Tool**

[⬆ Back to Top](#pinterest-image-scraper)

</div>
