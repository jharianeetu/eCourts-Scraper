# eCourts-Scraper

**Introduction**
"This project automates the process of downloading judge-wise cause list PDFs from the
New Delhi District Court official website
It uses Selenium and BeautifulSoup to scrape the cause list for a selected date and generates individual PDFs for each judge automatically."

**Features**

Automatically selects the New Delhi District Court complex
User selects a date for which the cause list is required
Fetches all judges’ cause lists for that day
Saves one PDF per judge in the data/ folder
Clean, simple Streamlit-based web interface
Built-in error handling and progress indicators

**Setup Instructions**

1-Clone the Repository
    git clone https://github.com/jharianeetu/eCourts-Scraper
    cd ecourts-scraper

2-Create Virtual Environment
    python -m venv venv
Activate it
    venv\Scripts\activate

3-Install Dependencies
    pip install -r requirements.txt

4-Run the Streamlit App
    streamlit run app.py

**How It Works**

    The Streamlit app opens a simple interface where the user selects a date.
    When the user clicks "Download PDFs", the backend function scrape_and_save_pdf() is called.
    Selenium automatically:
    Opens the New Delhi District Court website.
    Clicks on the selected date in the calendar widget.
    Waits for the updated cause list page to load.
    BeautifulSoup parses the HTML to extract judge names and table data.
    Each judge’s data is converted into a PDF file (using fpdf) and stored inside the data/ folder.
    The app confirms the success and displays a message showing how many judge PDFs were saved.        
