# Tarot - IP Geolocation Tool

## What it does
Tarot is a simple command-line tool that retrieves detailed geolocation information for any IP address. It fetches comprehensive data including location, ISP details, timezone, and security flags, then displays the results in a colorized terminal output and optionally saves them to a file.

## Features
- 🌍 Comprehensive IP geolocation lookup
- 🎨 Colorized terminal output with binary ASCII art
- 💾 Optional file output for results
- 🖥️ Windows-optimized with proper terminal color support
- 📊 Detailed information including ISP, timezone, coordinates, and security flags

## Installation

### Step 1: Install Python
If you don't have Python installed:

**Windows:**
1. Download Python from [python.org](https://www.python.org/downloads/)
2. Run the installer and **check "Add Python to PATH"**
3. Verify installation by opening Command Prompt and typing: `python --version`

**Alternative methods:**
- Using Microsoft Store: Search for "Python" and install
- Using Chocolatey: `choco install python`
- Using Winget: `winget install Python.Python.3`

### Step 2: Install Dependencies
Open Command Prompt or PowerShell and run:
```cmd
pip install requests colorama
```

Or install from requirements file:
```cmd
pip install -r requirements.txt
```

## Usage

### Basic Usage
```cmd
python tarot-template.py -i 8.8.8.8
```

### Save Results to File
```cmd
python tarot-template.py -i 8.8.8.8 -o results.txt
```

### Command Line Options
- `-i, --ip`: IP address to lookup (required)
- `-o, --output`: Output filename (optional, defaults to `{ip}.txt`)

### Examples
```cmd
# Lookup Google's DNS server
python tarot-template.py -i 8.8.8.8

# Lookup with custom output file
python tarot-template.py -i 1.1.1.1 -o cloudflare_dns.txt

# Lookup your public IP (get it first from whatismyip.com)
python tarot-template.py -i YOUR_PUBLIC_IP
```

## Sample Output
```
111111111   0000000   111111111   0000000   111111111
    1      0       0      1      0       0      1    
    1      0       0      1      0       0      1    
    1      0000000        1      0       0      1    
    1      0       0      1      0       0      1    
    1      0       0      1      0000000       1    

► status: success
► country: United States
► countryCode: US
► region: CA
► regionName: California
► city: Mountain View
► zip: 94043
► lat: 37.4192
► lon: -122.0574
► timezone: America/Los_Angeles
► isp: Google LLC
► org: Google Public DNS
► as: AS15169 Google LLC
...

[✔] Output saved to: 8.8.8.8.txt
```

## Information Retrieved
- Geographic location (country, region, city, coordinates)
- ISP and organization details
- Timezone and UTC offset
- Security flags (proxy, VPN, hosting detection)
- AS (Autonomous System) information
- Mobile/cellular detection

## Requirements
- Python 3.6+
- `requests` library for API calls
- `colorama` library for Windows terminal colors

## Disclaimer
**IMPORTANT:** This tool is intended for educational and legitimate network administration purposes only. 

- Only use this tool on IP addresses you own or have explicit permission to investigate
- Respect privacy and applicable laws in your jurisdiction
- The geolocation data is provided by ip-api.com and may not always be 100% accurate
- This tool should not be used for stalking, harassment, or any malicious activities
- Users are responsible for complying with all applicable local, state, and federal laws
- The author is not responsible for any misuse of this tool

## API Credits
This tool uses the free tier of [ip-api.com](http://ip-api.com/) for geolocation data. Please respect their rate limits and terms of service.

## License
This project is provided as-is for educational purposes. Use responsibly and ethically.