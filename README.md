# Personal Finance Dashboard

## Overview
A secure and user-friendly personal finance dashboard that allows users to manage their financial data while ensuring data security and privacy. This project demonstrates robust security features, including encryption, hashing, and backup & recovery mechanisms, implemented using Python and Streamlit.

---

## Features

### **User-Friendly Interface**
- Interactive dashboard built with Streamlit.
- Tabs for managing financial data, viewing analytics, and handling security settings.

### **Data Security**
- **Encryption:** Data is encrypted using *Fernet* to ensure confidentiality.
- **Password Security:**
  - Passwords are hashed with SHA-256 and salted to resist brute-force and dictionary attacks.
  - Login attempts are limited to prevent brute-force attacks.
- **CIA Principles:**
  - **Confidentiality:** Data encryption and salted password hashing.
  - **Integrity:** Hashing and secure backup mechanisms.
  - **Availability:** Reliable backups and recovery options ensure data accessibility.

### **Backup & Recovery**
- Users can create secure backups of their data.
- Backup files are stored securely and can be restored as needed.
- Options to recover the database from backup files in case of data loss.

### **Protection Against Attacks**
- **Brute Force Attacks:**
  - Account lockout after multiple failed login attempts.
  - Salting of passwords to prevent Rainbow Table attacks.
- **SQL Injection:**
  - Parameterized queries and SQLAlchemy ORM for database interaction.

---

## Tech Stack
- **Frontend:** Streamlit
- **Backend:** Python
- **Database:** SQLite (SQLAlchemy ORM)
- **Security:** Fernet Encryption, SHA-256 Hashing
- **Libraries:**
  - `cryptography` for encryption
  - `hashlib` for hashing
  - `timeit` for benchmarking
  - `os` for secure key generation

---

## Setup Instructions

### Prerequisites
1. Python 3.8 or higher installed on your system.
2. Install required libraries using pip:
   ```bash
   pip install streamlit cryptography sqlalchemy
    ```
### Running the Application
1. Clone the repository
  ```bash
   git clone https://github.com/yourusername/personal-finance-dashboard.git
```
2. Navigate to the project directory: 
  ```bash
   cd personal-finance-dashboard
```
3. Run the application: 
```bash
   streamlit run app.py
```
4. Open the provided local URL in your browser to use the app.

---

## Usage
1. **Login/Register:** Securely log in or register with your credentials.
2. **Manage Data:** Add, edit, or delete financial entries in the dashboard.
3. **Backup:** Use the "Backup & Recovery" tab to create and restore backups of your data.
4. **Security Settings:** View and understand how your data is protected under the "Security" tab.

---

## Future Enhancements
- Two-factor authentication for enhanced login security.
- Cloud-based backup storage for additional reliability.
- More advanced analytics and visualizations for financial insights.
- Role-based access control (RBAC) for multi-user scenarios.

---

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Contributors
- Advait
- Tarini
- Avinash

---

## Timing Comparison of Hashing Algorithms
The application benchmarks the performance of different hashing algorithms to ensure an optimal balance between security and efficiency:
- **SHA-256:** Faster and secure enough for password hashing.
- **SHA-512:** More secure but slower than SHA-256.
- **MD5:** Fast but insecure due to vulnerabilities.

Example Timing Results for 10,000 iterations:
- SHA-256: 0.0183 seconds
- SHA-512: 0.0252 seconds
- MD5: 0.0180 seconds

---

## Repository Tags
- streamlit
- encryption
- backup-recovery
- python
- finance

---

## Feedback & Issues
Feel free to raise an issue or submit a pull request for improvements or bug fixes.
