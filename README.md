#  Django Blog Management System (CMS)

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python)
![Django](https://img.shields.io/badge/Django-4.2%2B-092E20?style=for-the-badge&logo=django)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active-success?style=for-the-badge)

> **A robust Content Management System (CMS) designed for creating, organizing, and sharing dynamic content with ease.**



##  Overview

The **Blog Management System** is a full-featured web application that allows users to create, edit, and categorize content. It moves beyond a simple webpage by implementing dynamic content rendering, a comment moderation system, and a powerful search engine.

This project demonstrates proficiency in **Django's MVT architecture**, database relationships (ForeignKey/ManyToMany), and CRUD operations.

---

##  Architecture: Content Lifecycle

The system manages data through a strict lifecycle to ensure quality and organization.

| Stage | Status | Description | Action |
| :--- | :--- | :--- | :--- |
| **Creation** | **Draft** | Content is saved locally; visible only to the author. | `Create` / `Update` |
| **Review** | **Pending** | (Optional) Content is queued for admin approval. | `Review` |
| **Public** | **Published** | Content is live; indexed for search and open for comments. | `Read` / `Comment` |
| **Archive** | **Archived** | Old content is preserved but removed from the main feed. | `Soft Delete` |

---

##  Key Features

###  For Authors
* **Rich Text Editor:** Format posts with headings, bold text, and links.
* **Dashboard:** Manage drafts, published posts, and views analytics.
* **Media Management:** Upload and handle cover images for blogs.
* **Categorization:** Organize posts via Categories and Tags.

###  For Readers
* **Advanced Search:** Find articles by keyword, author, or tag.
* **Interaction:** Like posts and leave threaded comments.
* **Social Sharing:** Easily share articles to social media platforms.
* **Responsive UI:** Clean reading experience on mobile and desktop.

###  Admin Features
* **Comment Moderation:** Approve or delete user comments.
* **User Management:** Manage permissions for different authors.

---

##  Tech Stack

| Domain | Technologies Used |
| :--- | :--- |
| **Backend** | Python 3.8+, Django 4.2+ |
| **Frontend** | HTML5, CSS3, JavaScript, Bootstrap 5 |
| **Database** | SQLite (Dev) / PostgreSQL (Production) |
| **Media** | Pillow (Image processing) |

---

##  Quick Start Guide

### Prerequisites
* Python 3.8+
* pip

### Installation

1.  **Clone the repository**
    ```bash
    git clone [https://github.com/your-username/blog-system.git](https://github.com/your-username/blog-system.git)
    cd blog-system
    ```

2.  **Set up Virtual Environment**
    ```bash
    # Windows
    python -m venv venv
    venv\Scripts\activate

    # macOS/Linux
    python3 -m venv venv
    source venv/bin/activate
    ```

3.  **Install Dependencies**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Run Migrations**
    ```bash
    python manage.py makemigrations
    python manage.py migrate
    ```

5.  **Create Superuser (Admin)**
    ```bash
    python manage.py createsuperuser
    ```

6.  **Run Server**
    ```bash
    python manage.py runserver
    ```
    Visit `http://localhost:8000`


 Usage Guide
1. Writing a Blog Post
Log in and click "New Post".

Add a catchy Title and a Header Image.

Write your content and select a Category.

Click Publish to make it live instantly.

2. Managing Comments
Go to the Post Detail page.

Scroll to the comment section.

(As Author/Admin) Click the 🗑️ icon to remove spam or offensive comments.

 Security & Best Practices
XSS Protection: Django templates automatically escape dangerous characters.

CSRF Tokens: All forms are secured against Cross-Site Request Forgery.

Image Validation: Validates file types to prevent malicious uploads.

 Contact & Author
Arpit Bhojani - Python Developer

📧 Email: bhojaniarpit1432@gmail.com

 Phone: +91 7383181094

<div align="center"> <sub>Built with ❤️ and Django.</sub> </div>
## Project Structure

<details>
<summary>Click to expand file tree</summary>

```text
blog_project/
├── blog/                # Main Blog Application
│   ├── models.py        # Post, Comment, Category models
│   ├── views.py         # CRUD Logic
│   ├── urls.py          # Routing
│   └── templates/       # Blog Feed, Detail View
├── users/               # User Authentication
│   ├── models.py        # User Profile (Bio, Avatar)
│   └── views.py         # Register/Login
├── static/              # CSS, JS, Images
├── media/               # Uploaded images
├── manage.py
└── requirements.txt
