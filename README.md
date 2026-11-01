# EduLedger - A School Management System

A comprehensive, full-stack application designed to streamline school administration, encompassing student identity management, academic cycles, and complex financial tracking. 

## System Architecture
This project is structured as a decoupled monorepo, separating the client interface from the API services.

* **Frontend:** React with TypeScript, bundled via Vite. It includes a robust routing structure handling role-based access (Admin vs. Teacher) and specialized modules for fee collection, receipt printing (including thermal receipts), and reporting.
* **Backend:** Node.js with Express and TypeScript. It utilizes a modular, domain-driven design separating concerns into `academics`, `auth`, `dashboard`, `finance`, `identity`, and `system`.
* **Database:** Multi-database configuration supporting SQL (initialization scripts provided in `/sql`) and MongoDB. 

## Core Modules
* **Identity Management:** Track and manage Student and Teacher profiles, including admission forms, bonafide certificate generation, and bulk class promotions.
* **Academic Organization:** Manage Academic Years, Classes, and Sections seamlessly.
* **Finance & Accounting:** Comprehensive fee structures, ledger tracking, pending fee calculations, and expense logging.
* **Reporting & Analytics:** Dashboard KPIs and detailed reporting tools for Daily, Monthly, Half-Yearly, and Yearly Income/Expense statements.
* **Access Control:** Role-based dashboards isolating Admin privileges from standard Teacher access.

## Project Structure
```text
SKA-School-Management-Desktop-App/
├── backend/                  # Express/Node.js API
│   ├── sql/                  # SQL initialization and seed scripts
│   ├── src/                  # Domain modules (auth, finance, identity, etc.)
│   └── package.json          
├── frontend/                 # React/Vite Client
│   ├── public/               
│   ├── src/                  # Components, Contexts, Pages, and API services
│   └── package.json          
└── documentation/            # Deep-dive architecture and context docs
```

## Getting Started

### Prerequisites
* [Node.js](https://nodejs.org/) (v16 or higher recommended)
* A running instance of your configured database (PostgreSQL/MongoDB)

### Backend Setup
1. Navigate to the backend directory: `cd backend`
2. Install dependencies: `npm install`
3. Configure your environment variables (Database URIs, JWT secrets).
4. Initialize the database using the provided scripts in the `/sql` directory or the `init-db.js` script.
5. Start the development server: `npm run dev`

### Frontend Setup
1. Navigate to the frontend directory: `cd frontend`
2. Install dependencies: `npm install`
3. Start the Vite development server: `npm run dev`

## Documentation
For deeper technical insights, refer to the `/documentation` directory. It includes detailed breakdowns of the frontend data flow, system architecture, database migration plans, and context-specific documentation for domains like Fee Structures and Student Management.
