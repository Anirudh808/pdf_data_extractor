# PDF Table Extractor to Google Sheets

This Python project extracts tabular data from PDF files and uploads each table to a separate worksheet in a specified Google Sheet using the Google Sheets API and a service account.

---

## 📌 Features

- Extracts all tables from a PDF file using `pdfplumber`.
- Converts each table into a Pandas DataFrame.
- Authenticates using a Google service account.
- Creates a new worksheet for each table in the specified Google Sheets document.
- Uploads data with column headers preserved.

---

## 🧰 Technologies Used

- Python 3.x
- `pandas`
- `pdfplumber`
- `gspread`
- `google.oauth2` (Google API authentication)

---

## 🚀 How It Works

1. **Provide the PDF File Path**  
   Place your PDF in the `input/` folder (or specify another path in the code).

2. **Set the Google Sheet ID**  
   Provide the target Google Sheets document ID where you want to upload the tables.

3. **Authenticate via Service Account**  
   Use your `credentials.json` downloaded from Google Cloud Console.

4. **Run the Script**  
   Each table from the PDF is extracted and uploaded to a new worksheet in the Google Sheet.

---

## 🛠️ Setup Instructions

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/pdf-to-google-sheets.git
   cd pdf-to-google-sheets
   
2. Install dependencies:
   ```bash
   pip install pandas pdfplumber gspread google-auth

3. Create a Google Cloud Project:
   - Enable Google Sheets API.
   - Create a Service Account.
   - Share your target Google Sheet with the service account's email

4. Save your `credentials.json` in the root directory.

5. Run the script:
   ```bash
   python main.py