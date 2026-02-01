# 🕸️ StudyWeave  
**Research Analytics & Artifact Evaluation Platform**

A scalable **human-in-the-loop (HITL)** platform for evaluating **AI-generated vs. human-written software artifacts**.

---

## 🚀 Overview

**StudyWeave** is a full-stack research management system designed to address the *“black box”* problem in AI-assisted software engineering. It enables **blinded, side-by-side evaluations** of software artifacts (code, UML diagrams, test cases) to assess **readability, maintainability, and correctness**.

Unlike basic survey tools, StudyWeave provides a **complete research lifecycle platform**, featuring a custom competency engine, real-time analytics dashboards, and automated AI-powered result summarization.

---

## ⚡ Key Features

### 🤖 AI & Intelligence
- **Automated Summarization**  
  Integrated LLM services generate concise textual summaries of study results, enabling rapid insight extraction from complex datasets.

- **Smart Reporting**  
  Automated generation of professional **PDF and CSV reports** for offline analysis and publication.

---

### 📊 Analytics & Visualization
- **Custom SVG Dashboards**  
  A high-performance analytics engine built without heavy third-party libraries to render participant competency matrices and study progress in real time.

- **Anomaly Detection**  
  Algorithms automatically flag irregular behaviors such as speed-running participants or inconsistent evaluation patterns.

---

### 🛡️ Security & Architecture
- **Role-Based Access Control (RBAC)**  
  Secure, clearly separated workflows for:
  - Researchers (study creation)
  - Participants (artifact evaluation)
  - Reviewers (adjudication)

- **Study “Time Travel”**  
  Snapshot-based versioning of study configurations prevents data corruption during active research phases.

---

### 🎨 Advanced UX
- **Customizable Dashboards**  
  Researchers can rearrange widgets, enable dark mode, and persist UI preferences using PostgreSQL and LocalStorage.

- **Blinded Evaluation Mode**  
  A specialized interface removes author metadata from artifacts to ensure unbiased A/B testing.

---

## 🛠️ Tech Stack

| Domain | Technologies |
|------|-------------|
| Frontend | React.js, Shadcn UI, Tailwind CSS, Vite |
| Backend | Node.js, Express.js, Multer (file uploads) |
| Database | PostgreSQL, Sequelize ORM |
| Auth & Security | JWT (JSON Web Tokens), SMTP email verification |
| DevOps | Docker, GitHub Actions (CI/CD) |

---

## 📸 Screenshots

**Researcher Dashboard**

<img width="3304" height="1628" alt="image" src="https://github.com/user-attachments/assets/b06f5a92-8355-4134-9bc6-d7e51d9afd4c" />

<img width="3318" height="1566" alt="image" src="https://github.com/user-attachments/assets/d1402438-8996-4b69-91fb-ea317ef2bdf1" />

```

screenshots/
├── dashboard-1.png
├── dashboard-2.png
├── analytics-view.png

````

---

## ⚙️ Installation & Configuration

### Clone the Repository
```bash
git clone https://github.com/notfarruks/StudyWeave.git
````

Install dependencies in **both** `server` and `client` directories.

---

### Backend Setup

```bash
cd server
npm install
```

Create a `.env` file in the **server root**:

```env
NODE_ENV=development
PORT=5200

# Database Configuration
DB_HOST=127.0.0.1
DB_PORT=5432
DB_NAME=study_weave_db
DB_USER=postgres
DB_PASSWORD=postgres

# Auth & Security
JWT_SECRET=change_this_to_a_long_random_string

# Email Services (SMTP)
SMTP_HOST=sandbox.smtp.mailtrap.io
SMTP_PORT=2525
SMTP_USER=your_mailtrap_user
SMTP_PASS=your_mailtrap_password
SMTP_SECURE=false
SMTP_FROM=noreply@study_weave.com

# CORS & URLs
FRONTEND_URL=http://localhost:5173
BACKEND_URL=http://localhost:5200

# AI Integration (Google Gemini)
GEMINI_API_KEY=your_google_genai_api_key
GEMINI_LLM_NAME=gemini-2.5-flash
```

---

### Database Initialization

Run the following inside the `server` directory:

```bash
# Create tables
npx sequelize-cli db:migrate

# Seed initial data
npx sequelize-cli db:seed:all
```

---

### Frontend Setup

```bash
cd client
npm install
```

---

## 🚀 Usage

You must run **two terminal processes simultaneously**.

### Terminal 1 — Start Backend

```bash
cd server
npm run dev
```

### Terminal 2 — Start Frontend

```bash
cd client
npm run dev
```

The application will be available at:

```
http://localhost:5173
```

---

## 👥 Contributors

* **Zaeem Masood Sheikh** — Full Stack Architect & Analytics Engine
* **Ali Demir**
* **İsmail Yağız Güven**
* **Shahin Ibrahimli**
* **Farrukh Mammadov**

---

