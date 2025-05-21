# Internet Shop Management System 🌐  
**Final Project – Database Management System (IS210)**

## Overview

This project is a **web-based management system for an internet café**, built to streamline daily operations such as user access, billing, product tracking, and employee management. It was developed as a final project for the IS210 course at the University of Information Technology – VNUHCM.

The system utilizes a combination of:
- **Frontend**: HTML, CSS, JavaScript, Bootstrap
- **Backend**: PHP
- **Database**: Oracle SQL

---

##  Features

### Admin Features
- Add/edit/delete computers, users, employees, and products
- Create and update invoices automatically based on purchases
- Recharge user accounts (even during active sessions)
- Track usage and remaining credit
- Ensure **1 user per machine** and **1 machine per user**
- Calculate session time based on remaining balance
- Update balance upon session completion

### User Features
- Login with account credentials
- View and manage remaining balance
- Use services based on real-time credit countdown

---

## System Architecture

- **Database**: Oracle SQL
- **Website Backend**: PHP with OCI8 connection to Oracle DB
- **Frontend**: Bootstrap for responsive UI, JavaScript for interactivity

### Key Components:
- `TAIKHOAN`: user accounts
- `MAYTINH`: computers
- `SUDUNG`: session usage tracking
- `SANPHAM`: available products
- `HOADON`, `CTHD`: invoices and details
- `NHANVIEN`: employee management

---

## Implementation Details

### Login System
- Users can log in only if they have more than 1 minute of available time.
- Enforced using **PL/SQL triggers** and validation logic.

### Credit Tracking
- Admin can recharge accounts, which immediately updates session time.
- After session ends, remaining time and credit are recalculated automatically.

### Invoice Management
- Invoices and their values are updated dynamically.
- Uses `PROCEDURE` to auto-generate invoice IDs and compute totals.

### Other Logic & Constraints
- Ensures unique mapping between computers and accounts during a session.
- Uses **triggers** and **stored procedures** for business logic enforcement.

---

## Technologies Used

| Layer        | Technologies                    |
|--------------|----------------------------------|
| Frontend     | HTML, CSS, JavaScript, Bootstrap |
| Backend      | PHP (with OCI8 for Oracle)       |
| Database     | Oracle SQL, Triggers, Procedures |

---

## Limitations & Future Work

### Current Limitations
- Interface is basic and not visually appealing
- System only works on web (no mobile version)
- Security features are minimal
- Heavy reliance on JavaScript libraries

### Future Improvements
- Improve UI/UX with modern frontend frameworks
- Add role-based access and better authentication
- Implement mobile app support
- Enhance system security and audit trails

---

## Team Members

| Name               | Role                |
|--------------------|---------------------|
| Luong Anh Huy      | SQL, Coding, Slides |
| Pham Dong Hung     | SQL, Coding, Report |
| Phan Cong Minh     | SQL, Slides         |
| Hong Khai Nguyen   | Coding, Report      |

---

## 🧑‍🏫 Instructor

- **Lecturers**: Thai Bao Tran, Nguyen Ho Duy Tri  
- **Course**: Database Management System (IS210)  
- **University**: UIT – VNUHCM

---

