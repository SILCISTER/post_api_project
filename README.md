📄 Django DRF Post API

A simple Django REST Framework project built to practice creating APIs from scratch.
This project is designed for learning DRF basics: APIView, models, JSON responses, and API endpoints.

🚀 Features

Create a Post model with title, content, and timestamp

Return JSON response for all posts via API

Easy-to-extend structure for serializers, viewsets, and routers in future

Clean and minimal — perfect for learning DRF fundamentals

🛠️ Tech Stack

Python 3

Django 5

Django REST Framework

SQLite (default development database)

📦 Installation

1️⃣ Clone the repository:

git clone https://github.com/banumariwan/post_api_project.git
cd post_api_project


2️⃣ Create and activate a virtual environment:

python -m venv env
# Linux/Mac
source env/bin/activate
# Windows
env\Scripts\activate


3️⃣ Install dependencies:

pip install djangorestframework
pip install -r requirements.txt   # if you have one


4️⃣ Apply migrations:

python manage.py migrate


5️⃣ Create superuser (optional, for admin):

python manage.py createsuperuser


6️⃣ Run the server:

python manage.py runserver

📁 Project Structure
post_api_project/
│
├── posts/
│   ├── models.py
│   ├── views.py
│   ├── urls.py
│   ├── admin.py
│   └── apps.py
│
├── post_api_project/
│   ├── settings.py
│   └── urls.py
│
├── manage.py
└── README.md

📌 API Endpoint
Endpoint	Method	Description
/api/posts/	GET	Returns all posts in JSON
⭐ Learning Outcomes

DRF setup and configuration

APIView and returning JSON

Django models + DRF integration

Preparing for serializers and ViewSets (next steps)

🔮 Future Improvements

Add ModelSerializer for structured JSON

Add CRUD endpoints with ViewSet

Implement nested serializers (e.g., categories or authors)

Add Postman tests

Expand to full blog API

❤️ Author

Banu Mariwan
GitHub: banumariwan
