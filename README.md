📄 Django DRF Post API with Nested Categories

A **clean and minimal Django REST Framework project** built to practice API development from scratch.  
This version includes **nested serializers** for related models, allowing posts to show their associated category in JSON responses.  

---

## 🚀 Features

- **Post model** with title, content, timestamp, and category  
- **Category model** to organize posts  
- **ModelSerializer** automatically converts models to JSON  
- **Nested serializer**: PostSerializer includes category data  
- **ModelViewSet + Router** provides full CRUD operations:
  - List all posts  
  - Retrieve a single post  
  - Create new posts  
  - Update posts (full & partial)  
  - Delete posts  
- Optional **search** and **ordering** on posts  

---

## 🛠️ Tech Stack

- Python 3  
- Django 5  
- Django REST Framework  
- SQLite (default development database)

---

## 📦 Installation

1️⃣ Clone the repository:

```bash
git clone https://github.com/banumariwan/post_api_project.git
cd post_api_project
2️⃣ Create and activate a virtual environment:

bash
Copy code
python -m venv env
# Linux/Mac
source env/bin/activate
# Windows
env\Scripts\activate
3️⃣ Install dependencies:

bash
Copy code
pip install djangorestframework
pip install -r requirements.txt   # if available
4️⃣ Apply migrations:

bash
Copy code
python manage.py migrate
5️⃣ Create superuser (optional, for admin):

bash
Copy code
python manage.py createsuperuser
6️⃣ Run the server:

bash
Copy code
python manage.py runserver
📁 Project Structure
bash
Copy code
post_api_project/
│
├── posts/
│   ├── models.py
│   ├── serializers.py       # nested CategorySerializer
│   ├── views.py             # ModelViewSet
│   ├── urls.py              # Router for CRUD
│   ├── admin.py
│   └── apps.py
│
├── post_api_project/
│   ├── settings.py
│   └── urls.py
│
├── manage.py
└── README.md
📌 API Endpoints
Endpoint	Method	Description
/api/posts/	GET	List all posts
/api/posts/<id>/	GET	Retrieve a single post
/api/posts/	POST	Create a new post
/api/posts/<id>/	PUT	Full update of a post
/api/posts/<id>/	PATCH	Partial update of a post
/api/posts/<id>/	DELETE	Delete a post

Each post includes nested category data:

json
Copy code
{
    "id": 1,
    "title": "Hello",
    "content": "My first post",
    "created_at": "2025-11-16T03:00:00Z",
    "category": {
        "id": 1,
        "name": "Tech"
    }
}
⭐ Learning Outcomes
DRF setup and configuration

Returning JSON with ModelSerializer

Full CRUD with ModelViewSet and Router

Nested serializers for related models

Search and ordering for better API usability

🔮 Future Improvements
Add authentication & permissions

Expand relationships (e.g., authors, comments)

Add Postman tests or Swagger documentation

Extend to a full blog API

❤️ Author
Banu Mariwan
GitHub: banumariwan
