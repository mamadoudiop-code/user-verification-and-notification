# Commission Schedule TMWUserID Verification

## Name
Python Script for verification bambooHR entries

## Description
The script is designed for complex interactions involving IBM DB2 database operations and email communications via Outlook. It involves data fetching, manipulation, comparison, and notification processes.

## Key Features 

1. Database Connection:

    - Establishes a connection to an IBM DB2 database using credentials and parameters defined in environment variables.

2.  API Interaction:

    - Makes requests to the BambooHR API to retrieve employee information based on the database records.

3.   Email Notifications: 

    - Sends automated emails through Outlook using OAuth2 credentials.

4.  Data Processing and Comparison: 
 
    - Compares data from the database and the API to identify discrepancies.

5.  Environment Variable Management: 

    - Uses the decouple library for secure access to configuration data.

## Requirement
- Python
- IBM DB2 database
- Access to BambooHR API
- Environment variables for database and API configurations

## Dependencies 

- `decouple`: For managing environment variables.
- `requests`: For making API requests.
- `ibm_db`: For connecting to the IBM Db2 database.
- `exchangelib`: For handling Outlook email operations.
- `smtplib` and `email.message.EmailMessage`: For sending emails via SMTP.
- `re`: For regular expressions in Python.

## Configuration and Setup

- Set up environment variables for database credentials, API keys, and email settings.
- Install necessary Python libraries as mentioned in the dependencies.

## Installation
```
Pip install -r requirement.txt

```
Edit the .env file
-  Provide the database credentials, Database name, your UID and password
-  Provide an authorization bamboorh key. To get this authorization key you must follow these steps by:
    - getting firstly an API key from bamboorh
    - Go to bamboorh API documentation (https://documentation.bamboohr.com/reference/get-employee), provide your API and Password and get the authorization key in the headers

## How the Scripts Works

1. Database Connection: Establishes a connection to an IBM DB2 database using credentials specified in environment variables.

2. API Requests: Sends requests to the BambooHR API to retrieve employee information and compare it with database records.

3. Data Comparison: Identifies discrepancies between the database and the API data.

4. Email Notification: If discrepancies are found, the script formats a detailed report in both French and English and sends it via email using Outlook.

## Usage

1. Ensure all necessary environment variables are set.

3. The script main.py will automatically connect to the database, make API requests, compare data, and send email notifications if discrepancies are found.

## Notes

- The script assumes active database and BambooHR API connections.
- Error handling for database and API interactions is essential for production use.
- The script prints log messages for successful operations and potential discrepancies

## Support
If you meet problem sending email, please refer to support Team for reviewing the credentials

## Contributing
open to contributions 

## Authors and acknowledgment
- Mamadou Bamba Diop: Integration Specialist


## Project status

