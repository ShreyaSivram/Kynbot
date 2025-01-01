# Kynbot

Community Discovery Track
Problem Statement: Develop a chatbot that helps users discover events, activities, and
community gatherings based on their interests and location. The bot should:
• Process natural language queries
• Provide personalized recommendations
• Support location-based discovery
• Learn from user interactions
Rasa(the ML model) enables the development of customizable conversational AI chatbots that understand user intents and manage dialogues, while Retrieval-Augmented Reasoning (RAR) enhances these capabilities by integrating real-time data retrieval and logical reasoning for more accurate and context-aware responses.

BookMyShow Event Finder

This project is a web scraping and user interface solution to dynamically fetch and display event URLs from BookMyShow for specific locations. The project leverages Selenium for scraping and Streamlit for building an interactive user interface.

Features

Dynamic Event Scraping: Scrapes event data, including URLs, for locations such as Chennai, Mumbai, and Delhi.

User-Friendly Interface: Allows users to select a location from a dropdown and view event URLs instantly.

Efficient Backend: Uses Selenium with a headless browser for efficient data retrieval.

Project Structure

├── debug_scraper.py      # Script for scraping event data using Selenium
├── streamlit_app.py      # Streamlit app for user interaction and displaying event URLs
├── README.md             # Project documentation

Prerequisites

Python 3.8+

Google Chrome Browser

ChromeDriver (matching your browser version)

Python Libraries:

Install the following dependencies:

pip install selenium streamlit

Setup and Usage

1. Download and Setup ChromeDriver

Download ChromeDriver from the official website and place it in a directory on your machine. Note the path to this file.

2. Configure debug_scraper.py

Update the Service path in the script to point to your ChromeDriver:

service = Service('path/to/chromedriver')  # Replace with your actual path

3. Run the Scraper

To verify that the scraper is working:

python debug_scraper.py

This will print event URLs for predefined locations to the console.

4. Run the Streamlit App

Launch the Streamlit app to interact with the scraper via a web interface:

streamlit run streamlit_app.py

5. Interact with the App

Open the app in your browser (typically at http://localhost:8501).

Select a location from the dropdown menu.

View event URLs for the selected location.

File Descriptions

debug_scraper.py

This script handles web scraping using Selenium. It navigates to BookMyShow's website, extracts event URLs for specified locations, and prints them to the console.

streamlit_app.py

This script integrates the scraping functionality into a Streamlit-based web application. It provides an intuitive user interface for selecting a location and viewing event URLs.

Notes

Ensure your Chrome browser and ChromeDriver versions match.

If the app takes time to load, the delay is due to waiting for dynamic JavaScript content to render.

Troubleshooting

Timeout Errors:

Increase the wait time in the script:

WebDriverWait(driver, 30).until(
    EC.presence_of_element_located((By.CLASS_NAME, "event-card"))
)

ChromeDriver Issues:

Ensure ChromeDriver is correctly installed and accessible from the specified path.

Missing Events in App:

Verify the structure of the event container on BookMyShow's website. The HTML structure may change over time.

Future Enhancements

Add support for more locations dynamically.

Include event details such as name, date, and time.

Improve scraping logic to handle changes in website structure.

License

This project is licensed under the MIT License.

Contact

For questions or issues, feel free to reach out:

Email: shreya.sivram@gmail.com

GitHub: ShreyaSivram
