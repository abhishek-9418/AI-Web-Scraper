# AI Web Scraper

## Description
AI Web Scraper is a Streamlit-based web scraping tool that allows users to input a URL, scrape the website’s content, and interact with the scraped content through natural language queries. This project combines web scraping techniques with AI parsing using Ollama to interpret and extract valuable information from the scraped content.

## Features
- **Website Scraping**: Scrape any website’s DOM content by providing a URL.
- **DOM Content View**: Display and inspect the raw DOM content in an expandable text box.
- **AI Parsing**: Parse and extract specific information from the DOM content using Ollama's AI.
- **Content Cleaning**: Automatically clean up the scraped content to remove unnecessary HTML tags.

## Requirements

- Python 3.7+
- Streamlit
- BeautifulSoup4 (for scraping and parsing HTML)
- Ollama (for parsing with AI)
- Bright Data (for proxies)

### Install dependencies
To get started, install the required Python libraries by running the following command:

```bash
pip install -r requirements
```

## Setup Bright Data Proxy

To run the web scraper, you need to set up a proxy with Bright Data and store the proxy credentials in an environment file. Once your proxy is set up, store the `proxy_key` in an `.env` file at the root of the project directory. 

## How to Use

1. **Run the Streamlit App**  
   Start the Streamlit app by running:

   ```bash
   streamlit run main.py
   ```

2. **Enter Website URL**  
   Enter the URL of the website you want to scrape into the input field.

3. **Scrape Website**  
   Click the "Scrape Site" button to scrape the website’s content. This will scrape the HTML structure and extract the body content, which will be cleaned and displayed in the app.

4. **View DOM Content**  
   The cleaned DOM content will be shown in a text area that can be expanded for easier viewing. You can inspect the raw content of the website here.

5. **Parse Content**  
   After scraping, you can ask questions about the DOM content. Provide a description of the information you want to extract, and click the "Parse Content" button. The tool will use Ollama's AI model to parse the relevant chunks of the DOM and provide the response based on your query.

## Functions

- `scrape_website(url)`: Scrapes the HTML content from the specified URL.
- `split_dom_content(dom_content)`: Splits the DOM content into manageable chunks for processing.
- `clean_body_content(body_content)`: Cleans and formats the body content to remove unnecessary HTML tags and noise.
- `extract_body_content(dom_content)`: Extracts the main body content from the scraped DOM.
- `parse_with_ollama(dom_chuncks, description)`: Uses Ollama’s AI model to parse the DOM content and extract information based on a given description.

## Example

1. Enter the URL: `https://example.com`
2. Click "Scrape Site" to load and clean the website’s content.
3. Ask a question or give a description like "Extract all article titles" and click "Parse Content".
4. The app will use Ollama’s AI model to analyze the content and return the results.

## Future Enhancements

- Add more customizable scraping options (e.g., scraping specific elements).
- Improve error handling and edge cases (e.g., invalid URLs).
- Add support for scraping different types of content (e.g., images, videos, etc.).

## Contributing

Feel free to fork the repository and submit pull requests. Contributions are welcome!

## Contact

For questions, suggestions, or any issues, feel free to reach out to:

**Email**: abhishekdeshmukh207@gmail.com

Make sure you have set up the Bright Data proxy correctly to run the project. You'll need to store your proxy credentials in an `.env` file as described above.

