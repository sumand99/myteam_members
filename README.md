# myteam_members

# Team Member Management (Django Backend)

This is the **Django** + **Django Rest Framework** back-end component for a **Team Member Management** application. It provides a RESTful API to create, read, update, and delete team members.

---

## Table of Contents
1. [Overview](#overview)
2. [Key Features](#key-features)
3. [Prerequisites](#prerequisites)
4. [Installation](#installation)
5. [Database and Migrations](#database-and-migrations)
6. [Running the Server](#running-the-server)
7. [API Endpoints](#api-endpoints)
8. [Project Structure](#project-structure)
9. [Customization](#customization)
10. [Contributing](#contributing)
11. [License](#license)

---

## Overview

The Django application exposes a set of endpoints to manage team members, including:

- Listing all members
- Adding new members
- Editing member details
- Deleting members

It’s designed to work with a front-end (for example, a React SPA) to display and manipulate data.

---

## Key Features

- **Django Rest Framework** for quick API development
- **CRUD** operations on `TeamMember` model
- **Role-based** logic (e.g., admin vs. regular)
- **SQLite** by default (easy setup), but can be switched to other databases

---
Project Structure- 


<img width="386" alt="Screenshot 2025-03-23 at 12 57 55 AM" src="https://github.com/user-attachments/assets/9e504452-d2da-40bb-9aac-5bb52c81d943" />


## Prerequisites

- **Python 3.6+** (3.10 or newer recommended)
- **pip**, **pipenv**, or **poetry** to manage Python dependencies

---

## Local Setup

Follow these steps to **run the project locally** on your machine.

1. **Clone the repository**
   git clone https://github.com/sumand99/myteam_members.git
   cd myteam_members


2. **Create a virtual environment (optional, but recommended)**:

python3.13 -m venv venv
source venv/bin/activate  # On macOS/Linux


.\venv\Scripts\activate  #or on Windows

3. **Install dependencies**:
pip install -r requirements.txt

If the project doesn’t have a requirements.txt, run:

pip install django djangorestframework
pip freeze > requirements.txt

4. **Apply Migrations**:
python manage.py makemigrations
python manage.py migrate

5. **Run the Development Server**:
python manage.py runserver 127.0.0.1:8000


It should show something like below - 

<img width="900" alt="Screenshot 2025-03-23 at 12 58 47 AM" src="https://github.com/user-attachments/assets/1fd0b730-1427-4588-a43f-be68084cf0a6" />


**API Endpoints**
If your urls.py is set up for team_members, you can expect endpoints like:

Method	Endpoint	Description
GET	/api/team_members/	List all team members
POST	/api/team_members/	Create a new team member
GET	/api/team_members/<id>/	Retrieve a single team member
PUT	/api/team_members/<id>/	Update a single team member
PATCH	/api/team_members/<id>/	Partially update a single team member
DELETE	/api/team_members/<id>/	Delete a single team member
Note: Adjust the paths above if your configuration differs.

    
**Customization**
Settings: Update settings.py for different databases, debugging flags, allowed hosts, etc.
CORS: If your front end is on a different origin (like http://localhost:3000), consider installing django-cors-headers to handle cross-origin requests.
Authentication: If needed, integrate Django’s auth system or DRF’s token-based authentication.


**Contributing**
Fork this repository.
Create a feature branch: git checkout -b feature/my-new-feature.
Commit your changes: git commit -m 'Add new feature'.
Push the branch: git push origin feature/my-new-feature.
Open a Pull Request on GitHub.


**License**
This project is available under the MIT License. See the LICENSE file for details or choose a different license as needed.
 
