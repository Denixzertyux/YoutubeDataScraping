YouTube Channel Analyzer

This Python script scrapes video data (titles, views, duration) from a specified YouTube channel, processes the information, and generates a word cloud to visualize the most common words found in the video titles.

Description

The project automates the process of gathering insights from a YouTube channel. It uses a combination of web scraping and data analysis techniques to provide a high-level overview of a channel's content strategy based on video titles.

The workflow is as follows:

Scrape Data: Navigates to a YouTube channel's video page using Selenium, scrolls down multiple times to load a sufficient number of videos, and parses the page HTML with BeautifulSoup.

Extract Information: Pulls the title, view count, and duration for each video found on the page.

Store Data: Saves the raw extracted data into an Excel file (file.xlsx).

Process Data: Cleans the data using pandas. This involves converting view counts (e.g., '2.1M', '55K') into numerical integers and video durations into total seconds. It also categorizes videos based on their length.

Analyze Text: The video titles are processed using NLTK to remove common English stopwords and punctuation.

Visualize: A word cloud is generated from the cleaned titles to display the most frequently used terms, offering a quick look at the channel's main topics.

Features

Dynamic web scraping of a YouTube channel.

Handles dynamic page loading by simulating scrolling.

Robust data extraction from HTML.

Data cleaning and transformation for analysis.

Text preprocessing to filter out noise.

Visual representation of title keywords through a word cloud.

Technologies Used

Python 3

Selenium: For browser automation and web scraping.

BeautifulSoup4: For parsing HTML content.

pandas: For data manipulation and analysis.

NLTK (Natural Language Toolkit): For text preprocessing.

WordCloud: For generating the word cloud image.

Matplotlib: For plotting the visualization.

XlsxWriter: For writing data to an Excel file.

WebDriver Manager: For automatic management of the Selenium WebDriver.

Setup and Usage

Follow these steps to run the project on your local machine.

Prerequisites

Python 3.8 or higher

Google Chrome browser installed

Installation

Clone the repository:

git clone [https://github.com/your-username/youtube-channel-analyzer.git](https://github.com/your-username/youtube-channel-analyzer.git)
cd youtube-channel-analyzer


Install the required Python packages:
It's recommended to use a virtual environment.

pip install -r requirements.txt


Running the Script

Modify the Target URL (Optional):
You can change the YouTube channel by editing the urls list in the youtube_analyzer.py script:

# Define the target URL (Updated to the current YouTube channel format)
urls = ['[https://www.youtube.com/@AnotherChannel/videos](https://www.youtube.com/@AnotherChannel/videos)']


Execute the script from your terminal:

python youtube_analyzer.py


Output

file.xlsx: An Excel file containing the raw data of video titles, views, and durations.

A plot window will appear displaying the generated word cloud of the most frequent words in the video titles.

License

This project is open source and available under the MIT License.
