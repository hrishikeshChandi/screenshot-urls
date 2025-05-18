# Screenshot URLs

## Overview

This is a simple web app that lets you take screenshots of multiple URLs at once. It uses Selenium WebDriver to visit each website, capture a screenshot, and then saves them neatly in folders named after each website’s hostname. The backend is built with Flask, and there’s a clean, easy-to-use web interface.

## Features

- **Batch Screenshots:** Enter any number of URLs at once and get all screenshots in one go.
- **Organized Storage:** Screenshots are saved in folders named by the website’s hostname.
- **Headless Browsing:** Runs Chrome in the background without opening a browser window.
- **Easy Web Interface:** A simple webpage where you enter URLs and see results.
- **Error Messages:** Shows which URLs worked and which didn’t.

## How It Works

1. Enter one or more URLs (space separated) on the homepage.
2. The app uses Selenium with headless Chrome to visit each URL and take a screenshot.
3. Screenshots are saved inside a `screenshots/` folder, organized by each site’s hostname.
4. The webpage shows which screenshots were successful and which failed.

## Technologies Used

- **Python:** Flask for the web server.
- **Selenium:** To automate the browser and take screenshots.
- **webdriver_manager:** To manage ChromeDriver automatically.
- **HTML with Jinja2:** For the frontend and dynamic updates.

## Setup and Usage

1. **Clone the repo:**

   ```bash
   git clone https://github.com/hrishikeshChandi/screenshot-urls.git
   cd screenshot-urls

   ```

2. **Install dependencies:**
   Make sure you have Python 3.7+ installed, then run:

   ```bash
   pip install -r requirements.txt
   ```

3. **Run the app:**

   ```bash
   python main.py
   ```

   The server will start at `http://localhost:3000`.

4. **Use the app:**

   - Open your browser and go to `http://localhost:3000`.
   - Enter one or more URLs (space-separated) and submit.
   - Wait for screenshots to be taken. They’ll be saved in the `screenshots/` folder, organized by hostname.
   - See which URLs succeeded or failed on the webpage.

## Project Structure

- `main.py` – Flask app and screenshot logic.
- `templates/index.html` – Webpage for user input.
- `screenshots/` – Where all screenshots are saved, organized by hostname.
- `requirements.txt` – Python dependencies.
- `README.md` – This documentation.

## Notes

- Chrome browser must be installed for ChromeDriver to work.
- `webdriver_manager` automatically downloads and manages ChromeDriver.
- If the `screenshots` folder is deleted while running, saving will fail until recreated.
- For educational and demo use only.

## License

This project is under the MIT License.
