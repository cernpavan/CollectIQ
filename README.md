# CollectIQ

# CollectIQ — Smart Payment Collection & Business Analytics Platform for Wholesalers



## 🚀 Project Overview

**CollectIQ** is a full-stack web application designed to streamline payment collections from retailers and provide deep business analytics for wholesalers. It integrates ML-powered risk prediction and party behavior analysis to help businesses manage credit risk, optimize collections, and gain real-time insights.

Ideal for wholesale businesses such as Kirana shops, medical wholesalers, and general retailers, CollectIQ empowers admins and collection agents with powerful tools to manage payments, analyze data, and reduce risks effectively.

⚠️ **Important Notice:**  
This project is an **ERP tool for wholesalers** that handles sensitive business and payment data.  
The **source code is private** and not publicly available to prevent misuse, unauthorized copying, and to protect confidential business information.

If you want to learn more about the project or see a demo, please contact me directly at: pavan.kumar@example.com
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




------

📊 Analytics & ML Engine Details
Inputs:
Purchase history (volume, frequency)

Payment patterns (timeliness, amount)

Outstanding balances

Outputs:
Risk Score (0 to 1 scale)

Payment Frequency Clusters (Frequent, Irregular, Delayed)

Suggested payment reminder intervals

Debtor categorization (Safe / Watch / Risky)

Example Use Cases:
Credit risk prediction for each party

Automated reminder scheduling based on predicted behavior

Sales and collection trend visualizations

Party segmentation for better decision making

🧾 Features Breakdown
Admin Module
Employee management (CRUD)

Party assignment and management

Company-wide and party-specific reports with filtering

Control employee permissions

Send reminders & initiate payments via Razorpay

Visualize sales and collection analytics

Employee Module
Secure login with role-based access

View and update assigned party payment statuses

Access party-wise analytics

Generate Razorpay payment links/invoices

Send payment reminders to retailers

🔐 Security
JWT token-based authentication

Role-Based Access Control (Admin & Employee)

Audit trails and action logging for accountability

🤝 Contribution & Contact
Contributions are welcome!
Feel free to open issues or submit pull requests.
Contact: gunupatipavankumar@gmail.com

