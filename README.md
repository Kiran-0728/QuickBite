# QuickBite
Full-stack food ordering and management web application.

## Prerequisites
- Node.js (v18+)
- PostgreSQL Database
- Stripe Account

## Setup Instructions

### 1. Database & Backend
1. Go to `backend` directory: `cd backend`
2. Install packages: `npm install`
3. Make sure your PostgreSQL server is running.
4. Update `DATABASE_URL`, `JWT_SECRET`, and `STRIPE_SECRET_KEY` in `backend/.env` according to your local setup. The default configuration uses Postgres on localhost.
5. Initialize the database and run migrations: `npx prisma migrate dev --name init`
6. Seed the sample data (12 food items): `npx prisma db seed` 

### 2. Frontend
1. Go to `frontend` directory: `cd frontend`
2. Install packages: `npm install`
3. Create `.env` file if not present and specify `VITE_BACKEND_URL=http://localhost:4000`

### 3. Admin Panel
1. Go to `admin` directory: `cd admin`
2. Install packages: `npm install`
3. Create `.env` file if not present and specify `VITE_BACKEND_URL=http://localhost:4000`

### Running the App
Since `concurrently` is set up in the root package, you can run all 3 apps together.
1. `npm install` in the root directory (to install concurrently). 
2. `npm run dev`

Alternatively, start them separately:
- Backend: `cd backend && npm run dev`
- Frontend: `cd frontend && npm run dev` (Runs on port 5173)
- Admin: `cd admin && npm run dev` (Runs on port 5174)
