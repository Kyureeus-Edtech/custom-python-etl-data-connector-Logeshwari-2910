# Spamhaus DROP ETL Script

## Overview
This ETL (Extract, Transform, Load) script fetches the Spamhaus DROP list and stores it in a MongoDB collection.  
It is designed to automatically update existing records based on the `cidr` field.

---

## Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>
2. Create and Activate Virtual Environment
Windows (CMD):

bash
Copy
Edit
python -m venv venv
venv\Scripts\activate
macOS / Linux:

bash
Copy
Edit
python3 -m venv venv
source venv/bin/activate
3. Install Dependencies
bash
Copy
Edit
pip install -r requirements.txt
4. Environment Variables
Create a .env file (based on ENV_TEMPLATE) in the root directory:

env
Copy
Edit
DROP_URL=https://www.spamhaus.org/drop/drop.txt
MONGO_URI=mongodb://localhost:27017
DB_NAME=security_feeds
COLLECTION_NAME=spamhaus_drop
⚠ Do not commit your .env file to GitHub.
Add it to .gitignore.

5. Run the ETL Script
bash
Copy
Edit
python spamhaus_etl.py
