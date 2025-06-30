# BookNest Backend

Backend for BookNest bookstore, built with Node.js, Express, and MongoDB Atlas.

##  Features
- User authentication (JWT, bcrypt)
- Book management (CRUD, filters)
- Order system (place, view, history)
- User profile and admin/organizer dashboards
- Role-based access (user, admin, organizer)
- CORS enabled, async/await, error handling

##  Folder Structure
```
booknest-backend/
├── config/           # DB connection & env config
├── controllers/      # Business logic
├── middleware/       # JWT auth & error handlers
├── models/           # Mongoose models
├── routes/           # RESTful API routes
├── utils/            # JWT token utility
├── .env
├── .gitignore
├── server.js         # Entry point
└── README.md
```

##  Setup Instructions
1. Clone the repo and `cd booknest-backend`
2. Install dependencies:
   ```bash
   npm install
   ```
3. Create a `.env` file:
   ```env
   MONGO_URI=mongodb+srv://bhavyajha42:87654321g@cluster1.tyuenuq.mongodb.net/booknest?retryWrites=true&w=majority&appName=Cluster1
   JWT_SECRET=supersecretkey
   ```
4. Start the server:
   ```bash
   npm run dev
   # or
   npm start
   ```

##  API Endpoints
- `POST   /api/auth/signup`      — Register new user
- `POST   /api/auth/login`       — Login, returns JWT
- `GET    /api/auth/profile`     — Get logged-in user profile
- `GET    /api/books`            — List books (filters: genre, author, rating, search)
- `GET    /api/books/:id`        — Get book details
- `POST   /api/books`            — Create book (admin/organizer)
- `PUT    /api/books/:id`        — Update book (admin/organizer)
- `DELETE /api/books/:id`        — Delete book (admin/organizer)
- `POST   /api/orders`           — Place order (user)
- `GET    /api/orders`           — Get user's orders
- `GET    /api/orders/:id`       — Get order by id (user/admin/organizer)
- `GET    /api/users`            — List all users (admin)
- `GET    /api/users/:id`        — Get user by id (admin)
- `PUT    /api/users/:id`        — Update user (self/admin)
- `DELETE /api/users/:id`        — Delete user (admin)

##  Security
- Passwords hashed with bcrypt
- JWT for authentication (send as Bearer token)
- Role-based route protection
- CORS enabled for frontend integration

##  Deployment
- Ready for Render, Railway, Heroku, etc.
- All config via `.env`

##  MongoDB Atlas
- Uses MongoDB Atlas for cloud database
- Database: `booknest`

##  Authors
This website is designed and developed by:  
**Bhavya Jha**, **R Akash**, **S Jahnavi**, and **G Bhavya Sree**

---
MIT License 