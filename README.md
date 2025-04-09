# CRUD-Web-Development---traffic-tickets-
CRUD web development to allow user add, manage tickets and be able to update its state 

📚 Overview
This project demonstrates a full-stack web application using SvelteKit 5, Drizzle ORM, and PostgreSQL. It covers fundamental CRUD operations—Create, Read, Update, and Delete—implemented via API routes and forms.

The project includes:

Configure a SvelteKit project with PostgreSQL using Drizzle ORM.

Create, insert, and retrieve records from a database.

Update and delete data using API routes.

Work with migrations for database schema management.

Test database interactions using form-based UI.

🧰 Technologies Used
SvelteKit 5

Drizzle ORM

PostgreSQL (hosted via Neon)

TypeScript

Neon Serverless driver

Drizzle Kit (for migrations)

📁 Project Structure

src/
├── lib/
│   ├── db.ts               # Database configuration
│   ├── schema.ts           # Database schema (users, courses)
│   └── queries/            # All CRUD logic (insert, select, update, delete)
│
├── routes/
│   ├── api/
│   │   └── getUsers/+server.ts   # API for fetching users
│   ├── +page.server.ts           # Server actions for form submissions
│   └── +page.svelte              # UI and form logic

⚙️ Setup Instructions
1. Clone the Repo
git clone https://github.com/your-username/your-repo.git
cd your-repo

3. Install Dependencies
npm install

5. Configure Environment
Create a .env file with your Neon DB URL: env
DATABASE_URL="your_neon_connection_string"

4. Generate and Apply Migrations
npx drizzle-kit generate
npx drizzle-kit migrate

6. Run the App
npm run dev

🔧 CRUD Summary
Operation	File(s) Involved	Route
Create (User)	insert.ts, +page.server.ts	POST /createUser
Read (User)	select.ts, +server.ts	GET /api/getUsers
Update (User)	update.ts, +page.server.ts	POST /updateUser
Delete (User)	delete.ts, +page.server.ts	POST /deleteUser

📊 Course Table CRUD
Create: insertCourse.ts

Read: selectCourses.ts

Update: updateCourse.ts

Delete: deleteCourse.ts

All implemented similarly to users.


🧪 Testing
Tested through form submissions and API calls.


