# Grant Management System

A comprehensive, production-ready grant management system built with React, TypeScript, Node.js, and PostgreSQL.

## Features

- **User Authentication**: Secure JWT-based authentication (Register/Login).
- **Grant Management**: Admins can create grants; Users can view available grants.
- **Application System**: Users can apply for grants with proposals and document uploads.
- **Dashboard**: Role-based dashboards for Applicants and Admins.
- **Admin Tools**: View all applications, update status (Approved/Rejected), create new grants.
- **Responsive Design**: Mobile-friendly UI with Tailwind CSS.
- **Animations**: Smooth transitions using Framer Motion.

## Tech Stack

- **Frontend**: React, TypeScript, Tailwind CSS, Framer Motion, React Router, Axios.
- **Backend**: Node.js, Express, TypeScript, PostgreSQL (Neon DB), JWT, Multer.
- **Database**: PostgreSQL.

## Prerequisites

- Node.js (v14+)
- PostgreSQL Database (or Neon DB connection string)

## Setup Instructions

### 1. Clone the repository
```bash
git clone <repository-url>
cd grant-management-system
```

### 2. Backend Setup
```bash
cd server
npm install
```

Create a `.env` file in `server/` with the following:
```env
PORT=5000
DATABASE_URL=postgresql://user:password@host:port/database?sslmode=require
JWT_SECRET=your_super_secret_key
NODE_ENV=development
```

Run database migrations (schema is in `src/models/schema.sql`).

Start the server:
```bash
npm run dev
```

### 3. Frontend Setup
```bash
cd client
npm install
```

Start the development server:
```bash
npm run dev
```

## Testing

Run backend tests:
```bash
cd server
npm test
```

## API Documentation

- `POST /api/v1/auth/register`: Register new user.
- `POST /api/v1/auth/login`: Login user.
- `GET /api/v1/grants`: List all grants.
- `POST /api/v1/grants`: Create a grant (Admin only).
- `POST /api/v1/applications`: Submit application (with file upload).
- `GET /api/v1/applications`: Get my applications.
- `GET /api/v1/applications/all`: Get all applications (Admin only).
- `PATCH /api/v1/applications/:id/status`: Update application status (Admin only).

## Accessibility

The application follows WCAG AA standards with semantic HTML, proper ARIA labels, and keyboard navigation support.
