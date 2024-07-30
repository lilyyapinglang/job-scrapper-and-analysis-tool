# Job Scraper and Language Analysis Tool

## Project Overview

This project is a job scraping and analysis tool designed to extract job postings from LinkedIn, analyze the language requirements of these postings, and provide daily updates via email. The tool also includes a dashboard for visualizing trends and statistics about job postings, focusing on the language requirements.

## Features

- **Web Scraping:** Extract job postings based on specific keywords and locations from LinkedIn.
- **Language Analysis:** Use LangChain to analyze job descriptions and determine if the job requires fluency in languages other than English.
- **Data Storage:** Store job data and analysis results in a database.
- **Automation:** Daily scraping and analysis automation with scheduled tasks.
- **Email Notifications:** Send daily filtered job postings to your inbox.
- **Dashboard & Visualization:** Display trends and statistics in a dashboard.

## Technologies Used

- **Python:** Core programming language for development.
- **LangChain:** For NLP and language detection in job descriptions.
- **Selenium / BeautifulSoup / Scrapy:** For web scraping.
- **SQLAlchemy / SQLite / PostgreSQL:** For data storage.
- **APScheduler / cron:** For scheduling and automation.
- **Dash / Plotly:** For creating the dashboard and visualizations.

## Installation

### Prerequisites

- Python 3.7 or higher
- LinkedIn account (for accessing job postings)
- OpenAI API key (if using OpenAI's models)
- Database setup (SQLite, PostgreSQL, or another SQL database)

### Setup

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/job-scraper-langchain.git
   cd job-scraper-langchain
   ```

2. **Install dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

3. **Set up environment variables:**
   Create a `.env` file in the root directory and add the following:

   ```
   OPENAI_API_KEY=your_openai_api_key
   DATABASE_URL=your_database_url
   EMAIL_HOST=your_smtp_host
   EMAIL_PORT=your_smtp_port
   EMAIL_HOST_USER=your_email
   EMAIL_HOST_PASSWORD=your_email_password
   ```

4. **Initialize the database:**
   ```bash
   python init_db.py
   ```

## Usage

### Running the Scraper

To run the scraper and analyze job postings:

```bash
python scrape_and_analyze.py
```

This script will:

- Scrape job postings from LinkedIn based on specified keywords and locations.
- Analyze the language requirements using LangChain.
- Store the results in the database.

### Scheduling the Task

To schedule the task to run daily, set up a cron job or use APScheduler within your application. Example cron job setup:

```bash
0 9 * * * /path/to/your/python /path/to/scrape_and_analyze.py
```

### Viewing the Dashboard

To start the dashboard:

```bash
python dashboard.py
```

Access the dashboard at `http://localhost:8050`.

### Email Notifications

The tool sends daily filtered job postings to your inbox. Ensure your email settings in the `.env` file are correctly configured.

## Contributing

Contributions are welcome! Please submit a pull request or open an issue to discuss your ideas.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For any questions or feedback, please reach out to [yaping.lang@outlook.com](mailto:yaping.lang@outlook.com).

> > > > > > > 33ed22c (Initial commit with README and project files)
