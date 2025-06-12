# password-checker
A Python app to check password strength
📌 Overview

This tool helps users validate the strength of their passwords in real time. It's a simple terminal-based application that uses regular expressions to analyze the given password and returns a clear verdict.

---

## ✨ Features

- ✅ Checks for password **length (min 8 characters)**
- 🔠 Must contain **both uppercase and lowercase** letters
- 🔢 Must contain at least one **digit**
- 🔣 Must contain at least one **special character** (`!@#$%^&*`, etc.)
- 🧠 Easy-to-read result: **Strong ✅ / Weak ❌**
- 👩‍💻 Built using plain Python
- ## 📁 Folder Structure

password-checker/
│
├── checker.py # Python script with logic
└── README.md # Project description

---

## ⚙️ How to Run

### 🐍 Prerequisites
- Python 3.x installed

### ▶️ Steps to Run

1. **Clone the Repository** or [Download ZIP](https://github.com/YAGAVI2006/password-checker)
```bash
git clone https://github.com/YAGAVI2006/password-checker.git
cd password-checker
Run the Python script

bash
Copy
Edit
python checker.py
Try entering a password like

css
Copy
Edit
Yaga@2006
It will return:

css
Copy
Edit
✅ Strong Password
🔍 Code Snapshot
python
Copy
Edit
import re

def check_password_strength(password):
    length = len(password) >= 8
    upper = re.search(r"[A-Z]", password)
    lower = re.search(r"[a-z]", password)
    digit = re.search(r"\d", password)
    special = re.search(r"[!@#$%^&*(),.?\":{}|<>]", password)

    if all([length, upper, lower, digit, special]):
        return "✅ Strong Password"
    else:
        return "❌ Weak Password"

print("🔐 Password Strength Checker")
password = input("Enter your password: ")
print(check_password_strength(password))
💡 Future Ideas
GUI version with Tkinter

Add star * masking for input

Export results to a file

Web version using Flask

👩‍💻 Developed by
Yagavi – Python beginner with curiosity in software and security 💫
