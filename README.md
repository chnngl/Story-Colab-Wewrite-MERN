# We‑Write: Story Collab Tool

A web application for seamless, real-time collaboration on stories, allowing authors to write, edit, and review each other’s work with robust locking, tagging, and history features. Online version: https://we-write.onrender.com/

---

## Team Members

- Anjaly Jose
- Archana Sahoo
- Chang Liu
- Gabriela Goncalves Simoes
- Luxin Chen

---

## Features

-  **User Authentication**: Secure sign-up, login, and JWT sessions.
-  **Create & Edit**: Rich editor for story chapters, with per-story locking to avoid collisions.
-  **View & Collaborate**: Read published stories, add inline images, and filter by tags.
-  **Activity Logs**: Track edit history and view logs per story.
-  **Tag Filtering**: Browse stories by genre or custom tags.
-  **Responsive UI**: Mobile-first design with Bootstrap 5.
-  **Image Uploads**: Embed images in stories via Multer.
-  **Profile & Password Management**: Update password, view user profile.

---

##  Tech Stack

**Frontend**  
- React 18 & React Router v6  
- Bootstrap 5 
- Framer Motion & React Icons  

**Backend**  
- Node.js & Express.js  
- MongoDB with Mongoose  
- Multer for file uploads, JWT for auth  

**Dev**  
- ESLint, Prettier  
- Nodemon for auto-reload  

---

## Folder Structure

```
we-write/                    # Project Root
├── backend/                 # Express API
│   ├── config/              # DB connection
│   ├── controllers/         # Business logic
│   ├── middleware/          # Auth + upload
│   ├── models/              # Mongoose schemas
│   ├── routes/              # API endpoints
│   ├── .env                 # Env vars
│   ├── index.js             # Server entry
│   └── package.json         # Backend dependencies
└── frontend/                # React Client
    ├── public/              # Static assets
    ├── src/
    │   ├── assets/          # Images, icons
    │   ├── components/      # Reusable UI
    │   ├── pages/           # Views (Home, AboutUs, etc.)
    │   ├── store/           # Zustand authStore
    │   ├── utils/           # apiRequest, constants
    │   ├── App.jsx          # Root component
    │   └── main.jsx         # Entry point
    └── package.json         # Frontend dependencies
```

---

## Getting Started

### Prerequisites

- Node.js v18+  
- npm or Yarn  
- MongoDB Atlas (or local MongoDB)  

### Installation

```bash
# Clone repository
git clone https://github.com/your-username/we-write.git
cd we-write

# Backend setup
cd backend
npm install
cp .env.example .env   # set MONGO_URI and JWT_SECRET
npm run dev            # or nodemon index.js

# Frontend setup
cd ../frontend
npm install
npm run dev            # Vite or CRA dev server
```


---

## API Endpoints

| Method | Path                                 | Description                         |
|--------|--------------------------------------|-------------------------------------|
| POST   | `/api/register`                      | Register new user                   |
| POST   | `/api/login`                         | Authenticate user                   |
| GET    | `/api/stories`                       | List all stories (optional `tags`)  |
| POST   | `/api/stories`                       | Create a new story                  |
| GET    | `/api/stories/:id`                   | Get story by ID                     |
| PUT    | `/api/stories/:id`                   | Update story (locks apply)          |
| DELETE | `/api/stories/delete/:id`            | Delete a story                      |
| POST   | `/api/stories/lock/:id`              | Lock story for editing              |
| POST   | `/api/stories/unlock/:id`            | Unlock story after editing          |
| GET    | `/api/stories/:id/logs`              | Fetch story’s edit/view logs        |
| PUT    | `/api/updatepwd`                     | Update user password                |

---

## Usage & Routes

**Client Routes** (React Router):

- `/signup` — Sign up page  
- `/login` — Login page  
- `/home` — Dashboard / Story list  
- `/create` — Create new story  
- `/viewStory/:id` — Read story  
- `/updateStory/:id` — Edit story (locks apply)  
- `/loghistory/:storyId` — View activity logs  
- `/aboutus` — Team & project info  
- `/profile` — User profile  

---

*Happy writing!*

