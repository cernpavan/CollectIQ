# PayAnalytics — Smart Payment Collection & Business Analytics ERP for Wholesalers

![Tech Stack](https://img.shields.io/badge/Stack-MERN%20%2B%20MySQL-blue)
![License](https://img.shields.io/badge/License-Private-red)
![Built With](https://img.shields.io/badge/ML-Enabled%20with%20Python-brightgreen)

---

## 🚀 Project Overview

**PayAnalytics** is a full-stack ERP web application that helps wholesalers efficiently collect payments from retailers and analyze their business health using intelligent ML-powered analytics. It enables users to track outstanding balances, predict party payment risks, automate reminders, and visualize collection trends.

Designed for real-world businesses like kirana shops, medical wholesalers, and general distributors, **PayAnalytics** empowers admins and collection agents to manage dues smartly and grow with data.

---

⚠️ **Notice:**  
This ERP tool handles sensitive business and financial data.  
The **source code is private** to prevent unauthorized access or copying.  
For demo access or queries, contact: **gunupatipavankumar@gmail.com**

---

## 🧰 Tech Stack

| Layer                  | Technology                      |
|------------------------|--------------------------------|
| Frontend               | React.js                       |
| Backend                | Node.js (Express.js)           |
| **Database**           | **MySQL**                      |
| Payment Gateway        | Razorpay                       |
| Analytics & ML Engine  | Python (Flask or FastAPI)      |
| Authentication         | JWT (JSON Web Tokens)          |
| Role-based Access      | Admin, Employee (Collection Agent) |

---

## 👥 User Roles & Permissions

### 🧑‍💼 Admin
- Create, assign, and manage employees
- Assign retailers (parties) to employees
- View analytics:
  - Daily/weekly/custom collection reports
  - Party-specific balance, frequency, risk
  - Business trends and sales charts
- Trigger reminders
- Initiate collections via Razorpay
- Full ERP dashboard access

### 👨‍💻 Employee (Collection Agent)
- Login with role-based access
- View only assigned parties
- Update payment status
- Send Razorpay collection links
- View analytics for assigned parties (risk, frequency, balance)
- Trigger reminders and submit collection logs

---
## 📊 Analytics & ML Engine Details

### 🔢 Inputs:
- Purchase history (volume, frequency)
- Payment patterns (delays, consistency)
- Outstanding balances and duration

### 📈 Outputs:
- **Risk Score** (scale 0–1)
- **Frequency Category**: Frequent / Irregular / Delayed
- **Recommended Reminder Intervals**
- **Debtor Classification**: Safe / Watch / Risky

### 💡 Use Cases:
- Predict which retailers may default or delay payments
- Automatically suggest follow-up/reminder schedules
- Visualize payment patterns and optimize collection strategy
- Enable risk-based credit and decision-making for wholesalers

---

## 🧾 Key Features

### ✅ Admin Features:
- Employee and retailer (party) management (CRUD)
- Assign/unassign parties to employees
- Company-wide and per-party analytics dashboards
- Filterable collection reports (daily, weekly, custom ranges)
- View balance, collection rates, and risk levels
- Trigger reminders and initiate payments via Razorpay
- Visual business insights (charts, graphs, KPIs)

### ✅ Employee Features:
- Secure login with role-based access
- View only assigned parties
- Update and submit collection statuses
- Access assigned party analytics (balance, frequency, risk)
- Generate Razorpay payment links/invoices
- Trigger reminders directly from the UI

---

## 🔐 Security

- **JWT-based Authentication**: Secure and stateless login mechanism
- **Role-Based Access Control (RBAC)**: Admin vs. Employee permissions
- **Server-side Validation**: Prevents unauthorized data access
- **Admin Audit Logs**: Track and monitor admin activity for accountability

---

## 🏗️ System Architecture Overview

```plaintext
                        +-----------------------------+
                        |         Admin Panel         |
                        +-----------------------------+
                          |            |           |
             +------------+            |           +-------------------+
             |                         |                               |
+----------------------+   +----------------------+    +------------------------------+
| Manage Employees     |   | Assign Parties       |    | Analytics Dashboard           |
| (CRUD operations)    |   | to Employees         |    | - Total sales/collection      |
+----------------------+   +----------------------+    | - Risk ratios (A-Z view)      |
                                                     | - Party-wise analytics        |
                                                     +------------------------------+
                                                               |
                                                               |
                                        +------------------------------+
                                        | Python ML/AI Microservice    |
                                        | (risk, frequency, scoring)   |
                                        +------------------------------+
                                                               |
                                                               |
+------------------+        +---------------------+           |
| Collection Agent | <----> | Assigned Parties     |<----------+
| (Employee Panel) |        | (CRUD & View access) |
+------------------+        +---------------------+
    |       |                     |
    |       +--- Razorpay Payment |
    |                             |
    +--- Send Reminders           |
        View Party Analytics      |
        View Collection History   |



🤝 Contribution & Contact
Open to collaborations or integrations with your business!

Reach me at gunupatipavankumar@gmail.com for access, demo, or discussions.
