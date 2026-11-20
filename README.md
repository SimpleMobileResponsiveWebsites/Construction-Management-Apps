# 🛠️ Contractor Management Tool

<div align="center">

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-1.x-FF4B4B?logo=streamlit&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.x-150458?logo=pandas&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green)

**A clean, lightweight Streamlit application for contractors and small teams to manage projects, tasks, clients, people, and expenses — all in one place.**

*Version 1.02*

</div>

---

## ✨ Overview

The **Contractor Management Tool** is a simple yet powerful single-file Streamlit app designed to help freelancers, contractors, and small agencies stay organized.  

It provides an intuitive interface to:

- Track team members
- Manage clients
- Create and assign projects
- Break projects into tasks with status tracking
- Record expenses with automatic totals
- View everything in clean, merged tables
- Export your data as CSV files

All data lives in **Streamlit session state**, making it perfect for quick sessions, demos, or temporary tracking. Export your data before closing the app to keep it permanently.

---

## 🚀 Features

| Feature                  | Description                                                                 |
|--------------------------|-----------------------------------------------------------------------------|
| **People Management**    | Add team members who can be assigned to projects and tasks                 |
| **Client Management**    | Store client name, address, email, and phone                               |
| **Project Tracking**     | Create projects with description, assignee, priority, estimate & client    |
| **Task Management**      | Add tasks under projects with status, priority, and estimated hours        |
| **Expense Tracking**     | Log expenses with cost × quantity and automatic total calculation          |
| **Smart Views**          | Projects are automatically joined with client information                  |
| **CSV Export**           | Download projects, tasks, and expenses separately                          |
| **Clean UI**             | Organized with expanders and forms for a pleasant experience               |

---

## 📦 Installation

### Prerequisites
- Python 3.8 or higher
- `pip`

### Setup

1. **Clone or download** this repository
2. **Install dependencies**:

```bash
pip install streamlit pandas
Or create a requirements.txt:

txt
streamlit
pandas
Then run:

bash
pip install -r requirements.txt
Run the app:
bash
streamlit run app.py
Replace app.py with the name of your Python file if different.

The app will open in your browser (usually at http://localhost:8501).

📖 How to Use
The interface is organized into collapsible sections:

1. Add New Person
Add team members who will appear in assignment dropdowns.

2. Add New Client
Store client details (name, address, email, phone).
Clients are automatically linked when you create projects.

3. Add New Project
Project name & description
Assign to a person
Set priority (Low / Medium / High)
Estimated hours
Link to a client (or create a new one on the fly)
4. View Projects
See all projects in a clean table, automatically merged with client information.

5. Add New Task
Select an existing project
Task name, description, status (Not Started, In Progress, Completed)
Assign to a person
Priority and estimated hours
6. View Tasks
View all tasks in a table.

7. Add New Expense
Expense name
Unit cost
Quantity
Total is calculated automatically
8. View Expenses
See all logged expenses.

9. Export Data
Download three separate CSV files:

projects.csv
tasks.csv
expenses.csv
📊 Data Model
Entity	Key Fields
People	Name
Clients	ID, Name, Address, Email, Phone
Projects	Name, Description, Assigned To, Priority, Estimate Hours, Client ID
Tasks	Project Name, Task Name, Description, Status, Assigned To, Priority, Hours
Expenses	Name, Cost, Quantity, Total Cost
⚠️ Important Notes
Session-based storage: All data is stored in memory during your session. Refreshing or closing the browser will clear the data.
Export regularly: Use the Export section to download CSVs before leaving the app.
No authentication: This is a local tool — perfect for personal use or demos.
🛠️ Tech Stack
Frontend / App: Streamlit
Data Handling: Pandas
Language: Python 3.8+
📁 Project Structure
contractor-management-tool/
├── app.py                 # Main Streamlit application
├── requirements.txt       # Dependencies
└── README.md              # This file
