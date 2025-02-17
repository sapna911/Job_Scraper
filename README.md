# Job Scraper

## Project Overview
This project is a web scraper that extracts job listings from **Indeed** using **Selenium** and stores the data in **MongoDB**. Additionally, it provides an **admin panel** built with **Django** to manage job listings. The project also includes **NumPy** calculations to determine average salaries.

## Features
- **Scrape job listings** from Indeed using Selenium
- **Store scraped data** in MongoDB
- **Admin panel** for managing job listings (Django)
- **Calculate average salaries** using NumPy
- **Deployable online**

## Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/Job_Scraper.git
cd Job_Scraper
```

### 2. Create a Virtual Environment
```bash
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Setup MongoDB
Ensure MongoDB is installed and running. Update the connection string in the `settings.py` file:
```python
DATABASES = {
    'default': {
        'ENGINE': 'djongo',
        'NAME': 'job_scraper_db',
        'CLIENT': {
            'host': 'mongodb://localhost:27017/',
        }
    }
}
```

### 5. Run Migrations & Start Server
```bash
python manage.py migrate
python manage.py runserver
```
Access the admin panel at `http://127.0.0.1:8000/admin`.

### 6. Run the Scraper
```bash
python scraper.py
```

## Deployment
To deploy online, use services like **Heroku, AWS, or DigitalOcean**. Ensure the database and Django settings are properly configured for production.


