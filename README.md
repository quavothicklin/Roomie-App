🏡 Roomie — Shared-Living Management App

> Turn the invisible work of running a household into a clear, shared system.

Roomie is a shared-living management web application designed for college students and young adults living with roommates. It solves everyday household coordination challenges by centralizing task management, equal expense splitting, and household activity in a single, calm dashboard.

---

🚀 Live Demo & Links

- 🌐 Live Web Application: https://YOUR_GITHUB_USERNAME.github.io/roomie-app
- 📄 Product Requirements Document (PRD): MVP v0.1

---

✨ Key Features (MVP Scope)

- 🏠 Household Management: Create a household, view roommates, and share a unique invite code.
- 📋 Shared Task & Chore Tracking: 
  - Create, assign, and track status (To Do, In Progress, Completed).
  - Set due dates with visual overdue indicators.
  - Filter tasks by assignment ("Assigned to Me") or completion status.
- 💰 Equal Expense Splitting:
  - Record shared purchases and select participating roommates.
  - Automatic equal split calculations and net balance tracking (who owes whom).
  - Calculated balance view without storing sensitive banking data.
- ⚡ Activity Feed: Chronological history of completed tasks, new chores, and recorded expenses.
- 🔐 Secure Multi-Tenant Isolation: Row-Level Security (RLS) ensures household data remains private to invited members.

---

🛠️ Tech Stack

- Frontend: React, Tailwind CSS, JavaScript (ES6+)
- Backend & Database: Supabase (PostgreSQL)
- Authentication & Security: Supabase Auth + PostgreSQL Row Level Security (RLS)
- Deployment: GitHub Pages / Vercel

---

🗄️ Database Setup (Supabase)

The project relies on PostgreSQL tables and RLS policies defined in supabase/schema.sql.

1. Execute SQL Schema
In your Supabase SQL Editor, run the SQL script located in supabase/schema.sql to create the required tables:
- households
- household_members
- tasks
- expenses
- expense_shares
- activities

2. Configure Row Level Security (RLS)
Apply the RLS helper function and policies in supabase/rls_policies.sql to ensure users can only query data for households they belong to.

---

💻 Local Development Setup

1. Clone the repository:
   git clone https://github.com/YOUR_GITHUB_USERNAME/roomie-app.git
   cd roomie-app

2. Open index.html in your browser, or serve it using a local development server (e.g., Live Server extension in VS Code).

3. Connect Supabase Credentials:
   Update the initialization variables in index.html or your .env file:
   const SUPABASE_URL = 'https://YOUR_PROJECT.supabase.co';
   const SUPABASE_ANON_KEY = 'YOUR_SUPABASE_ANON_KEY';

---

📜 License

Distributed under the MIT License. See LICENSE for more information.
