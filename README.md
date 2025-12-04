# TeamG Capstone Project
 
# 🏢 EMS Portal - Employee Management System

![React](https://img.shields.io/badge/Frontend-React-61DAFB.svg) ![Spring Boot](https://img.shields.io/badge/Backend-Spring%20Boot-6DB33F.svg) ![AWS](https://img.shields.io/badge/Deployed-AWS-FF9900.svg)

A comprehensive, full-stack **Employee Management System** designed to streamline HR operations. This application features a microservices architecture, a modern glassmorphism UI, real-time workforce analytics, and secure role-based access control.

---

## 📐 Architecture & Workflow

| **System Architecture** | **Request Workflow** |
| :---: | :---: |
| ![EMS Architecture](assets/ems-architecture.png) | ![EMS Workflow](assets/ems-workflow.png) |
| *Microservices Overview* | *End-to-End Request Flow* |

---

## 🚀 Key Features

### 🛡️ Authentication & Security
* **Role-Based Access Control (RBAC):** Distinct portals for **Super Admins** (HR) and **Employees**.
* **JWT Security:** Stateless authentication using JSON Web Tokens.
* **Secure Recovery:** "Forgot Password" flow using a composite Security Key (`Username` + `Birth Year`).
* **Credential Reset:** Admins can securely reset user credentials to a default format.

### 👨‍💼 Admin Dashboard (HR Portal)
* **Workforce Analytics:** Interactive charts (powered by Recharts) displaying:
    * Skill Distribution (Pie Charts).
    * Salary Ranges & Designation Breakdown (Bar/Area Charts).
    * Demographics (Age Group Analysis).
* **Talent Search:** Advanced multi-filter search to find candidates based on **Tech Stack**, **Company**, and **Experience**.
* **Employee Management:** Complete CRUD capabilities for employee records.
* **Automated Notifications:** System triggers emails for Account Creation, Password Resets, and Profile Updates.

### 👤 User Dashboard (Employee Portal)
* **My Profile:** A polished, read-only view of personal employment details and salary.
* **Work History:** Digital resume tracking previous companies, tech stacks, and tenure.
* **Team Directory:** Searchable list of colleagues and their designations.
* **Responsive Design:** Fully optimized mobile view with a sliding sidebar and backdrop support.

---

## 🛠️ Tech Stack

### 💻 Frontend
* **Framework:** React.js (v18+)
* **Styling:** Tailwind CSS (Custom Glassmorphism Theme)
* **Routing:** React Router DOM v6
* **Visualization:** Recharts
* **HTTP Client:** Axios (with Interceptors)
* **Icons:** React Icons 

### ⚙️ Backend (Microservices)
* **Framework:** Spring Boot 3.x
* **Language:** Java 21
* **Architecture:**
    1.  **API Gateway:** Central entry point routing traffic (Port 9999).
    2.  **Employee Service:** Core user data and authentication (Port 8081).
    3.  **Experience Service:** Manages work history and skill analytics (Port 8082).
* **Database:** MySQL (AWS RDS).
* **Security:** Spring Security, JWT.
* **Communication:** REST APIs.
* **Notifications:** JavaMailSender (SMTP).

---

## 📂 Project Structure

```bash
Employee_management_System/
├── EMS-Backend-Capstone/       # Core Employee Microservice
├── ExperienceService/          # Work Experience Microservice
├── EMS_API_GATEWAY/            # Spring Cloud Gateway
├── EMS-Frontend-Capstone/      # React Application
└── assets/                     # Project Diagrams & Static Images
