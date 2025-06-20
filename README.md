# CollectIQ

# CollectIQ — Smart Payment Collection & Business Analytics Platform for Wholesalers

![CollectIQ Logo](link-to-your-logo-if-any)

## 🚀 Project Overview

**CollectIQ** is a full-stack web application designed to streamline payment collections from retailers and provide deep business analytics for wholesalers. It integrates ML-powered risk prediction and party behavior analysis to help businesses manage credit risk, optimize collections, and gain real-time insights.

Ideal for wholesale businesses such as Kirana shops, medical wholesalers, and general retailers, CollectIQ empowers admins and collection agents with powerful tools to manage payments, analyze data, and reduce risks effectively.

---

## 🧰 Tech Stack

| Layer                  | Technology                      |
|------------------------|--------------------------------|
| Frontend               | React.js                       |
| Backend                | Node.js (Express.js)           |
| Database               | MySQL (or PostgreSQL)          |
| Payment Gateway        | Razorpay                      |
| Analytics & ML Engine  | Python (Flask or FastAPI)      |
| Authentication         | JWT (JSON Web Tokens)          |
| Role-based Access      | Admin, Employee (Collection Agent) |

---

## 👥 User Roles & Permissions

### Admin (Full Access)
- Manage employees (create, assign, delete)
- Assign parties (retailers) to employees
- View company-wide and party-specific analytics:
  - Collections (daily, weekly, custom ranges)
  - Party risk, balance, frequency, sales trends
- Trigger payment reminders
- Initiate payments via Razorpay
- Access a full business dashboard with comprehensive insights

### Employee (Collection Agent)
- View only assigned parties
- Collect payments using Razorpay integration
- Access analytics for assigned parties:
  - Payment status, balance, risk profile
- Send payment reminders
- Submit and update collection records

---

## 🏗️ System Architecture Overview

```plaintext
                        +-----------------------------+
                        |           Admin Panel       |
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
