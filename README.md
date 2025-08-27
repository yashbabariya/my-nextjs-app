# Next.js + MongoDB CRUD App

A minimal full-stack app built with **Next.js (App Router)** and **MongoDB** using **Mongoose**.  

This project demonstrates how to:

- Connect to MongoDB (Atlas or CosmosDB with Mongo API).
- Expose API endpoints for CRUD operations (`/api/users`).
- Fetch and display data on the frontend.

---

## 🚀 Tech Stack

- **Next.js 14+ (App Router)** – Frontend + API Routes  
- **MongoDB / MongoDB Atlas** – Database  
- **Mongoose** – ODM for MongoDB  
- **TypeScript** – Strongly typed development  

---

## 📂 Project Structure
```bash
.
├── app
│   ├── api
│   │   └── users
│   │       └── route.ts     # API routes (GET, POST)
│   ├── page.tsx             # Frontend page
├── lib
│   └── mongodb.ts           # MongoDB connection helper
├── models
│   └── User.ts              # Mongoose User model
├── package.json
└── README.md
```




---

## ⚙️ Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/nextjs-mongodb-crud.git
cd nextjs-mongodb-crud
```        

### 2. Install Dependencies
```bash
npm install
```
#### or
```bash
yarn install
```

### 3. Configure Environment Variables

* Create a .env.local file in the project root:
```bash
MONGODB_URI="your-mongodb-connection-string"
```

* For MongoDB Atlas, it looks like:
```bash
MONGODB_URI="mongodb+srv://<username>:<password>@cluster0.mongodb.net/mydb"
```

### 4. Run the Development Server
```bash
npm run dev
```

* Visit: http://localhost:3000
----

### 📡 API Endpoints
* GET /api/users

#### Fetch all users.
```bash
curl http://localhost:3000/api/users
```
```bash
POST /api/users
```

### Create a new user.
```bash
curl -X POST http://localhost:3000/api/users \
  -H "Content-Type: application/json" \
  -d '{"name": "John Doe", "email": "john@example.com"}'
```

### 🎨 Frontend Page

* Fetches users from /api/users.
* Displays them in a styled list.
* Provides a simple form to add new users.

### ✅ Example Workflow

1. Start the app.
2. Open the homepage → See user list (initially empty).
3. Add a user with the form.
4. The list updates with the new user (thanks to live API fetch).

## 📌 Future Improvements

* Add PUT and DELETE endpoints.
* Add authentication with NextAuth.js.
* Add UI framework like TailwindCSS for better styling.

## 📝 License

MIT © 2025 YASH BABARIYA
