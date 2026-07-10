# Anveshak Hub Internal Applications

This repository is the central monorepo hosting the internal suite of business applications for **Anveshak Hub Private Limited**. It integrates operational workflows, sales pipeline automation, and identity governance into a unified codebase.

---

## 📂 Repository Structure

The project is structured to manage two primary applications:

### 1. 💼 Anveshak CRM (V2)
A tailor-made Customer Relationship Management system designed to automate B2G (Business-to-Government) and manufacturing sales pipelines across Karnataka.
*   **Rule-Based Lead Scoring:** Automated scoring engine prioritizing leads based on event outcomes (emails, demo requests, calls).
*   **Pipeline & Kanban Board:** Drag-and-drop opportunity cards with real-time total value calculations per pipeline stage.
*   **GST Document Engine:** One-click automated compiler for localized, brand-compliant GST quotations and dispatch.
*   **Audit Trail & Governance:** Strict server-side route guards (RBAC) and database-level tracking logging all export and record modifications.

### 2. 🌐 Anveshak Ecosystem Portal
The core operations platform connecting Anveshak Hub's central business services and database directories.

---

## 🛠️ Technological Stack

Both applications leverage a modern, serverless-first TypeScript stack:

*   **Framework:** [Next.js 15+ (App Router)](https://nextjs.org/) utilizing React Server Components (RSC) and React 19 Server Actions for secure, high-performance page rendering (<2s load times).
*   **Database:** [Neon Serverless PostgreSQL](https://neon.tech/) providing transactional data consistency, auto-scaling compute (scale-to-zero when idle), and instant branching.
*   **ORM:** [Prisma Client](https://www.prisma.io/) serving as the type-safe relational bridge.
*   **Identity & Auth:** [Clerk](https://clerk.com/) implementing invite-only signups, session persistence, and secure Role-Based Access Control (RBAC).
*   **UI System:** [Tailwind CSS](https://tailwindcss.com/) & [shadcn/ui](https://ui.shadcn.com/) (Radix primitives) for a clean, responsive layout fitting both desktop monitors and field reps' mobile screens (PWA).

---

## 🚀 Getting Started

### 📋 Prerequisites
Ensure you have the following installed locally:
*   [Node.js (v18.x or higher)](https://nodejs.org/)
*   [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)

### 🔧 Installation
1.  **Clone the repository:**
    ```bash
    git clone https://github.com/Sumanth069/Anveshak-Hub-internal-applications.git
    cd Anveshak-Hub-internal-applications
    ```
2.  **Install dependencies:**
    ```bash
    npm install
    ```
3.  **Configure Environment Variables:**
    Create a `.env` file in the root of the project (or appropriate subfolders) and configure the following services:
    ```env
    # Database Configuration (Neon Postgres Connection String)
    DATABASE_URL="postgresql://user:password@endpoint/dbname?sslmode=require"

    # Authentication Configuration (Clerk)
    NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY="pk_test_..."
    CLERK_SECRET_KEY="sk_test_..."
    ```
4.  **Run Database Migrations:**
    ```bash
    npx prisma migrate dev
    ```
5.  **Start the Local Development Server:**
    ```bash
    npm run dev
    ```
    Open [http://localhost:3000](http://localhost:3000) in your browser to view the application.
