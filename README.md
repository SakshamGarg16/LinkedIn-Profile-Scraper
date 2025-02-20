# LinkedIn Profile Scraper

## Overview
This script automates the process of searching for LinkedIn profiles associated with specific companies and job roles. It utilizes Google Search to find LinkedIn profiles and saves the results in an Excel file.

## Features
- Searches for LinkedIn profiles of specified job roles (CTO, Co-Founder, Founder, Employee).
- Uses Google Search to fetch results.
- Saves data (Profile Name, Company Name, Role, LinkedIn URL) to an Excel file.
- Implements a delay between requests to avoid rate limits.

## Prerequisites
Ensure you have the following installed:
- Python 3.x
- Required Python libraries:
  ```bash
  pip install -r requirements.txt
  ```

## Usage
1. **Prepare Input File**
   - Create a CSV file named `input_companies.csv` containing a list of company names (one per line).

2. **Run the Script**
   - Execute the script using the command:
     ```bash
     python script_name.py
     ```

3. **Output**
   - The script will generate an Excel file (`linkedin_profiles.xlsx`) with the extracted LinkedIn profiles.

## File Structure
```
.
├── input_companies.csv         # Input file with company names
├── linkedin_profiles.xlsx      # Output file with LinkedIn profiles
├── scraper.py                  # Main script file
├── Scraper_DDGs.py             # Contains the same code using DuckDuckGo
├── Guide.md                    # Contains a step by step guide to run the code
├── requirements.txt            # Contains the requirements needed for executing
└── README.md                   # Documentation
```

## Notes
- The script uses Google Search, which may be subject to rate limiting. To avoid this:
  - Increase the sleep time in `time.sleep(random.uniform(3, 6))`.
  - Use a VPN or rotating proxies if necessary.
- If search queries fail, check internet connectivity and ensure Google Search is accessible.

## License
This project is open-source and available for modification and distribution.

