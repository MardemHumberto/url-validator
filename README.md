# url-validator
A Python automation script that checks the validity of links stored in Google Sheets, identifying broken, redirected, or functional URLs related to real estate reports.

This project was driven by a real-world problem I faced while working at a tech company in Brazil. We send forms to customers via WhatsApp in large volumes, but there was no visibility into whether the links were working or broken before sending them. With this scalable automation, I can now reliably check the status of each link prior to delivery, ensuring quality and preventing broken links from being shared with customers.---

## Features

- Connects to Google Sheets.
- Checks links from two different tabs:
  - form_links: Checks if form links are working or broken.
  - website_links: Checks if website links redirect to the homepage (indicating expiration) or lead to valid pages.
- Runs checks in parallel using multithreading for faster results.
- Writes the results directly back into the same Google Sheet.
- Handles errors like timeouts, connection failures, and redirects.

---

## Tech Stack

- Python 3
- Google Sheets API
- Libraries:
  - pandas
  - requests
  - gspread
  - gspread_dataframe
  - pygsheets
  - tqdm
  - concurrent.futures

---

## How to Run

### 1. Install dependencies

```bash
pip install pandas requests gspread gspread_dataframe pygsheets tqdm
