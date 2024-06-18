# django-project
# Country API

In this project, a Django REST Framework application was set up using Django 5.0.6, focusing on creating a simple API for managing country data. We defined a Country model, migrated the database, and loaded initial data from a JSON file. Subsequently, we created serializers, views, and configured URL patterns to expose the API endpoints, allowing us to perform CRUD operations on the country data. The development server was successfully run

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Contributing](#contributing)

Create and Activate a Virtual Environment:
It's a good practice to use a virtual environment for Python projects to manage dependencies. Create and activate a virtual environment using:

sh
Copy code
python3 -m venv venv
source venv/bin/activate
Install Dependencies:
Install the required Python packages, including Django and Django REST Framework:

sh
Copy code
pip install django djangorestframework
Navigate to the Project Directory:
Ensure you are in the root directory of the project where the manage.py file is located:

sh
Copy code
cd countryapi
Apply Migrations:
Create and apply the necessary database migrations to set up the initial database schema:

sh
Copy code
python manage.py makemigrations
python manage.py migrate
Load Initial Data:
Create a file named countries/fixtures/countries.json and add initial data to it. This data will be loaded into the database:

json
Copy code
[
    {
        "model": "countries.country",
        "pk": 1,
        "fields": {
            "name": "Thailand",
            "capital": "Bangkok",
            "area": 513120
        }
    },
    {
        "model": "countries.country",
        "pk": 2,
        "fields": {
            "name": "Australia",
            "capital": "Canberra",
            "area": 7617930
        }
    },
    {
        "model": "countries.country",
        "pk": 3,
        "fields": {
            "name": "Egypt",
            "capital": "Cairo",
            "area": 1010408
        }
    }
]
Load the data into the database using:

sh
Copy code
python manage.py loaddata countries.json
Run the Development Server:
Start the Django development server to test the application:

sh
Copy code
python manage.py runserver
Usage
To access the API, open your browser or a tool like Postman and navigate to http://127.0.0.1:8000/countries/. This endpoint provides access to the list of countries and supports CRUD operations, allowing you to create, read, update, and delete country records.

API Endpoints
GET /countries/: Retrieve a list of all countries.
POST /countries/: Create a new country.
GET /countries/{id}/: Retrieve a specific country by ID.
PUT /countries/{id}/: Update a specific country by ID.
DELETE /countries/{id}/: Delete a specific country by ID.
Contributing
Fork the repository.
Create a new branch (git checkout -b feature/your-feature-name).
Commit your changes (git commit -m 'Add some feature').
Push to the branch (git push origin feature/your-feature-name).
Open a pull request.
