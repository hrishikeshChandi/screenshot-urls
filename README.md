# Website Screenshot App

The **Website Screenshot App** is a Flask web app that takes screenshots of any list of websites entered by the user. It uses Selenium and ChromeDriver to load pages and save screenshots in organized folders.

## Features

- Simple web form to input URLs.
- Automatically takes screenshots using headless Chrome.
- Saves screenshots in a structured folder (`screenshots/hostname/`).
- Shows which screenshots succeeded or failed.

## Prerequisites

Before using the app, you need:

1. Python 3.7 or higher  
2. Google Chrome installed  
3. Chrome WebDriver (handled automatically by `webdriver-manager`)

## Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/website-screenshot-app.git
   cd website-screenshot-app
   ```

2. **Install the Required Packages**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Make Sure Google Chrome is Installed**:
   The script uses Chrome in headless mode.

## Usage

1. **Start the Flask App**:
   ```bash
   python main.py
   ```

2. **Open in Browser**:
   Go to:
   ```
   http://localhost:3000
   ```

3. **Enter URLs**:
   - Type or paste URLs (one per line or space-separated) into the input box.
   - Submit the form.
   - The app will take screenshots and show success/failure results.

## File Structure

- **main.py**: The main Flask app and Selenium logic.
- **templates/index.html**: HTML form to input URLs.
- **screenshots/**: Folder where screenshots are saved.
  - Each hostname (like `example.com`) gets its own subfolder.

## How It Works

1. **Input**:
   - User enters website URLs in the form.

2. **Screenshot Process**:
   - Chrome runs in headless mode.
   - Each page is opened and a screenshot is taken.
   - Screenshots are saved in folders named after each site's hostname.

3. **Results**:
   - After processing, the app shows which screenshots were successful or failed.

## Technologies Used

- **Flask**: Web framework for Python.
- **Selenium**: Used to open pages and take screenshots.
- **ChromeDriver**: Controls the Chrome browser.
- **Webdriver-Manager**: Automatically downloads the right ChromeDriver version.

## Limitations

- If the screenshots folder is deleted while running, the app may fail.
- Requires internet connection to load pages.
- Pages with heavy JavaScript might not load fully in headless mode.

## License

This project is open-source and available under the MIT License.