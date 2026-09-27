
# Naukri Job Scraper using Python & Playwright

## Project Overview

This project is a Python-based web scraper that collects job listings from Naukri.com using Playwright.

The scraper extracts important job information and stores it in an Excel file. On every new run, the scraper compares the newly scraped jobs with existing records and adds only new jobs.

## Features

* Scrapes job listings from Naukri.com
* Uses Playwright for browser automation
* Extracts:

  * Job ID
  * Job Title
  * Company
  * Location
  * Experience
  * Skills
  * Posted Date
  * Job URL
* Stores job data in an Excel file
* Prevents duplicate job entries using Job URL
* Preserves previously stored jobs
* Adds only newly discovered jobs
* Includes basic error handling
* Maintains a scraper log file

## Technologies Used

* Python 3.10+
* Playwright
* Pandas
* OpenPyXL
* Microsoft Excel / WPS Office

## Project Structure

```text
naukri-job-scraper/
│
├── naukri_scraper.py
├── requirements.txt
├── README.md
├── naukri_jobs.xlsx
├── scraper.log
└── venv/
```

## Installation and Setup

### Step 1: Install Python

Make sure Python 3.10 or later is installed on the system.

Check the Python version:

```cmd
python --version
```

### Step 2: Open the Project Folder

Open Command Prompt and navigate to the project folder:

```cmd
cd C:\Users\user\Desktop\naukri-job-scraper
```

### Step 3: Create a Virtual Environment

Create a Python virtual environment:

```cmd
python -m venv venv
```

### Step 4: Activate the Virtual Environment

Activate the virtual environment:

```cmd
venv\Scripts\activate
```

After activation, `(venv)` will appear at the beginning of the Command Prompt.

Example:

```text
(venv) C:\Users\user\Desktop\naukri-job-scraper>
```

### Step 5: Install Required Packages

Install all required Python packages using:

```cmd
pip install -r requirements.txt
```

The project uses the following packages:

* Playwright
* Pandas
* OpenPyXL

### Step 6: Install Playwright Chromium

Install the Chromium browser required by Playwright:

```cmd
playwright install chromium
```

Wait until the installation is completed.

### Step 7: Run the Scraper

Run the Python scraper:

```cmd
python naukri_scraper.py
```

The browser will open and the scraper will access the Naukri.com job listings page.

### Step 8: Scrape Job Details

The scraper collects the following information:

* Job ID
* Job Title
* Company
* Location
* Experience
* Skills
* Posted Date
* Job URL

### Step 9: Save Data to Excel

After scraping, the job data is saved to:

```text
naukri_jobs.xlsx
```

The Excel file can be opened using Microsoft Excel or WPS Office.

### Step 10: Duplicate Detection

When the scraper is run again, it reads the existing Excel file and compares the Job URLs.

If a job already exists, it is not added again.

Example:

```text
Existing jobs in Excel: 22
No new jobs found.
```

If new jobs are found, only the new jobs are added while previously stored jobs are preserved.

### Step 11: Check the Log File

The scraper creates a log file:

```text
scraper.log
```

The log records important events such as:

* Scraper start
* Number of job cards found
* Jobs added
* Errors
* Browser closure

## Output

The Excel file contains the following columns:

| Column      | Description                    |
| ----------- | ------------------------------ |
| Job ID      | Unique job identifier          |
| Job Title   | Title of the job               |
| Company     | Company offering the job       |
| Location    | Job location                   |
| Experience  | Required experience            |
| Skills      | Skills associated with the job |
| Posted Date | Job posting date               |
| Job URL     | Link to the job listing        |

## Duplicate Handling

The scraper uses the Job URL to identify duplicate job listings.

The duplicate handling process is:

1. Scrape job listings from Naukri.com.
2. Read the existing Excel file if it exists.
3. Compare the newly scraped Job URLs with the existing Job URLs.
4. Remove jobs that already exist.
5. Add only new jobs to the Excel file.
6. Preserve all previously stored jobs.

This prevents duplicate job entries across multiple scraper runs.

## Error Handling

The scraper includes basic error handling for:

* Page loading errors
* Job extraction errors
* Excel file reading errors
* Unexpected runtime errors

Errors and important events are recorded in `scraper.log`.

## Example Execution

Run the following command:

```cmd
python naukri_scraper.py
```

Example output:

```text
Opening Naukri...
Page loaded successfully.
Job cards found: 20

Saving jobs to Excel...
Existing jobs in Excel: 22
No new jobs found.

Scraping completed successfully.
```

## Notes

* An active internet connection is required to run the scraper.
* Naukri.com may change its webpage structure in the future, which may require updating the Playwright selectors.
* The project is intended for educational and assignment purposes.
* The `venv` folder is used for the local Python environment and does not need to be submitted.

## Assignment Deliverables

The project submission contains:

1. `naukri_scraper.py` - Python source code
2. `naukri_jobs.xlsx` - Scraped Excel output
3. `requirements.txt` - Required Python packages
4. `README.md` - Setup and execution instructions
5. `scraper.log` - Scraper execution log
   id="x8q7pr"


