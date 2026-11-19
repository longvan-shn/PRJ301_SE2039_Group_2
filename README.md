# AutoWashPro

A modern vehicle wash and membership management platform developed using Java Servlet, JSP, and MVC2 architecture.

## Screenshots

### Landing Page

<img src="docs/images/landing-page.png" width="100%">

### Customer Dashboard

<img src="docs/images/customer-dashboard.png" width="100%">

## Overview

AutoWashPro is a web-based system designed to streamline vehicle wash booking, membership management, loyalty rewards, and customer engagement.

The platform provides:

* Customer self-service portal
* Membership tier progression
* Loyalty points system
* Vehicle management
* Booking management
* Staff administration portal

This project was developed as part of the PRJ301 course.

---

## 👨‍💻 My Contributions — Trần Long Vân ([@longvan-shn](https://github.com/longvan-shn))

> **Role:** Backend & Database Logic Developer (`branch: tlv`, PR `#31` · **31 commits**)  
> **Upstream Repo:** [`phanthanhhung03/PRJ301_SE2039_Group_2`](https://github.com/phanthanhhung03/PRJ301_SE2039_Group_2)

### Key Engineering Contributions

* **Customer Registration & Dual-Layer Validation (`4fa8799`, `469173d`, `dc97fd3`, `457ae38`):**
  - Built the end-to-end customer sign-up flow (`createCus`, `getCus(phone)`) with frontend and backend input validation, duplicate-account checks in the DAO layer, and automatic default membership tier assignment (`tierID = 1` / `Member`).
* **Time-Slot Booking Engine & SQL Server Schema Extension (`7bbfc49`, `5cc4703`):**
  - Extended the `Booking` table in SQL Server with the `TimeSlot` column ([`database/back-up/add-TimeSlot-column-for-Booking-table.sql`](database/back-up/add-TimeSlot-column-for-Booking-table.sql)), implemented slot conflict validation, and wired real-time customer/admin dashboard updates after booking.
* **Membership-Tier Booking Rules & Payment Confirmation Flow (`7344281`, `b4abbab`, `4975bfd`):**
  - Enforced advance-booking date limits based on customer membership tier across both JSP views and Controller servlets.
  - Built the post-booking payment confirmation flow and prevented invalid `COMPLETED ↔ CANCELLED` booking state transitions (`c2681f9`).
* **Defect Resolution & JDBC Resource Safety (`dafed61`, `c2681f9`):**
  - Fixed critical defects including unlimited promotion-code reuse and **JDBC database connection leaks** by ensuring consistent connection closure in DAO methods.

---

## Features

### Customer Portal

#### Landing Page

* Modern responsive interface
* Membership showcase
* Service highlights
* Customer feedback section

#### Authentication

* Customer Sign In
* Customer Sign Up
* Session-based authentication

#### Dashboard

* Membership overview
* Loyalty points tracking
* Tier progression
* Vehicle overview
* Booking overview
* Activity history

#### Membership Program

The loyalty system includes four membership tiers:

| Tier     | Benefits                             |
| -------- | ------------------------------------ |
| Member   | Default customer tier                |
| Silver   | Enhanced loyalty rewards             |
| Gold     | Increased booking privileges         |
| Platinum | Premium benefits and highest rewards |

---

### Staff Portal

#### Administration Dashboard

* Operations overview
* Customer management
* Booking management
* Loyalty management
* Reports and analytics

---

## Technology Stack

### Backend

* Java Servlet
* JSP
* JDBC
* SQL Server

### Frontend

* HTML5
* CSS3
* JavaScript
* Responsive Design
* BEM Methodology

### Architecture

* MVC2 Pattern
* DAO Pattern
* Session-based Authentication

---

## Project Structure

```text
AutoWashPro
│
├── src
│   ├── controller
│   ├── dao
│   ├── dto
│   └── dbutils
│
├── web
│   ├── customer
│   │   ├── landing-page.jsp
│   │   ├── signin.jsp
│   │   ├── signup.jsp
│   │   └── dashboard.jsp
│   │
│   ├── admin
│   │   ├── admin-login.jsp
│   │   ├── admin-dashboard.jsp
│   │   ├── customer-management.jsp
│   │   ├── booking-management.jsp
│   │   ├── loyalty-management.jsp
│   │   └── reports.jsp
│   │
│   ├── css
│   │   └── style.css
│   │
│   ├── META-INF
│   └── WEB-INF
│
└── database
```

---

## Database Modules

* Customers
* Customer Tiers
* Vehicles
* Bookings
* Loyalty Points
* Point Transactions

---

## Design Philosophy

AutoWashPro follows a premium modern design language:

* Dark Luxury Theme
* Japanese-inspired aesthetics
* Apple-like minimalism
* Responsive layouts
* Glassmorphism effects
* Consistent Design System
* Mobile-first approach

---

## MVC2 Workflow

```text
Browser
    ↓
Controller Servlet
    ↓
DAO Layer
    ↓
Database
    ↓
JSP View
```

---

## Authentication Flow

```text
Landing Page
    ↓
Sign In
    ↓
SigninController
    ↓
Session Creation
    ↓
Dashboard
```

Authenticated users are managed through HTTP Session.

---

## Future Enhancements

* Real-time booking updates
* Email notifications
* Payment integration
* Vehicle service history
* Advanced reporting dashboard
* Membership reward automation

---

## Team

Developed for academic purposes as part of the Software Engineering program at FPT University.

---

## License

This project is intended for educational and learning purposes.
