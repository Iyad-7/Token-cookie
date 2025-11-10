# PLU5_TokenCookieProject_YourName

## Setup
1. Install dependencies:
   npm install

2. Create .env file:
   PORT=4000
   JWT_SECRET=supersecretlongkey
   JWT_EXPIRES_IN=1h
   NODE_ENV=development

3. Run the server:
   npm start
   or development:
   npm run dev

---

## Pre-seeded Users
Role   | Email           | Password
-------|------------------|------------
Admin  | admin@test.com   | AdminPass123!
User   | user@test.com    | UserPass123!

---

## API Routes

### Public
- POST /register → Create user {email, password, firstName}
- POST /login → Get JWT cookie
- POST /logout → Clear cookie

### Protected (login required)
- GET /profile → Current user info
- GET /tasks → User’s own tasks
- POST /tasks → Create new task {title, description}
- DELETE /tasks/:id → Delete own task

### Admin only
- GET /admin/users → List all users
- GET /admin/tasks → List all tasks

---

## Authentication Flow
1. /login checks credentials, signs JWT
2. JWT stored in HTTP-only cookie (auth_token)
3. Middleware verifies cookie token on protected routes
4. /logout clears the cookie

---

## Submission Checklist
- server.js
- package.json
- .env.example
- README.md
- screenshots/ (login, cookie, profile)
- Deployed URL:``
- Zip as PLU5_TokenCookieProject_Iyad.zip
