# Guide to Running the LinkedIn Profile Scraper

This guide provides step-by-step instructions to run the LinkedIn Profile Scraper script. Follow these steps carefully to scrape LinkedIn profiles for specific job roles at different companies.

---

## Prerequisites

Before running the script, ensure you have the following installed:

1. **Python** (version 3.8 or higher) - [Download here](https://www.python.org/downloads/)
2. **Google Search Library** (`googlesearch-python`)
3. **OpenPyXL** (for handling Excel files)

To install the required Python libraries, run the following command in the terminal or command prompt:

```sh
pip install -r requirements.txt
```

---

## How to Run the Script

### 1. Prepare Your Input File

- Create a CSV file named `input_companies.csv` in the same directory as the script.
- Add a list of company names (one per line) in the file. Example:

```
Google
Amazon
Microsoft
```  

### 2. Modify the Script (Optional)

- If you want to change the job roles being searched, edit the following line in the script:

```python
search_terms = ["Employee"]  # Modify this list to include roles like "CTO", "Co-Founder", etc.
```

- To change the number of search results fetched, modify this line:

```python
results = search(query, num_results=10)  # Change 10 to the desired number of results
```

### 3. Run the Script

- Open a terminal or command prompt.
- Navigate to the script directory.
- Run the script using:

```sh
python scraper.py
```

### 4. View the Results

- The extracted LinkedIn profiles will be saved in an Excel file named `linkedin_profiles.xlsx`.
- Open the file to view the profile names, company names, roles, and clickable LinkedIn URLs.

---

## Notes

- Running the script too frequently may result in a temporary block from Google. If you encounter errors, wait a few minutes before trying again.
- For better privacy and security, consider using a **VPN** before running the script.
- The script uses Google Search, which may be subject to rate limiting. To avoid this:
  - Increase the sleep time in `time.sleep(random.uniform(3, 6))`.
  - Use a VPN or rotating proxies if necessary.
- Always ensure compliance with **LinkedIn's terms of service** when scraping data.

---

Now you're all set! 🚀 Happy Scraping!

