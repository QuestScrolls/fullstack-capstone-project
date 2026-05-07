# 🎁 GiftLink – Full‑Stack Gift Sharing App

A full‑stack web application where users can browse, search, and share gifts.  
Built with **React**, **Node.js/Express**, **MongoDB**, and **JWT authentication**.  
This project was completed as the final capstone for the **IBM Full Stack Developer Professional Certificate** on Coursera.

![React](https://img.shields.io/badge/React-18-61DAFB?logo=react)
![Node.js](https://img.shields.io/badge/Node.js-18-339933?logo=node.js)
![Express](https://img.shields.io/badge/Express-4.18-000000?logo=express)
![MongoDB](https://img.shields.io/badge/MongoDB-6-47A248?logo=mongodb)
![JWT](https://img.shields.io/badge/JWT-auth-000000?logo=json-web-tokens)

---

## 📚 Project Origin
This is the final capstone project of the [IBM Full Stack Developer Professional Certificate](https://www.coursera.org/professional-certificates/ibm-full-stack-cloud-developer) on Coursera.  
The assignment provided starter code and a step‑by‑step guide; I completed all missing parts, connected the frontend to the backend, and ensured the app works end‑to‑end.

---

## ✨ Features

- **User Authentication**  
  Register, login, and logout using JWT (stored in `sessionStorage`). Protected routes redirect unauthenticated users.

- **Gift Catalog (Main Page)**  
  Fetch and display all gifts from MongoDB. Each card shows image, name, condition, and date added.

- **Search with Filters**  
  Search gifts by name, category, condition, and maximum age. Filters are sent to the backend API.

- **Gift Details Page**  
  View full details of a single gift (category, condition, date added, description, age).  
  Hardcoded comments section for demonstration.

- **Profile Management**  
  View and edit your name (email is fixed). Success message shown after update.

- **Responsive UI**  
  Built with Bootstrap 5 and custom CSS.

- **Backend API**  
  RESTful endpoints for gifts, search, and user management.

---

## 🛠️ Tech Stack

### Frontend
- React 18 (functional components, hooks)
- React Router v6 (client‑side routing)
- Bootstrap 5 (styling)
- Context API (`AuthContext`)

### Backend
- Node.js with Express
- MongoDB (with native driver)
- JSON Web Token (JWT) for authentication
- bcryptjs for password hashing
- Pino logger
- dotenv for environment variables
- CORS enabled

### Database
- MongoDB (`giftdb` database, `gifts` and `users` collections)


## 🚀 Getting Started

### Prerequisites
- Node.js (v18 or higher)
- npm (v9+)
- MongoDB (local or MongoDB Atlas connection string)

### Installation & Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/QuestScrolls/giftlink-capstone.git
   cd giftlink-capstone
   
2. Start the backend server (from the server directory):

       node app.js
3. Start the React development server (from the client directory):

       npm start
4. Use the app!
  Register a new account, browse gifts, use the search, and update your profile.

📡 API Endpoints
Method	Endpoint	Description	Auth Required
POST	/api/auth/register	Register a new user	No
POST	/api/auth/login	Login and receive JWT	No
PUT	/api/auth/update	Update user name	Yes (email in header)
GET	/api/gifts	Get all gifts	No
GET	/api/gifts/:id	Get single gift by ID	No
POST	/api/gifts	Add a new gift	No (demo)
GET	/api/search	Search gifts with query params	No

Search query parameters: name, category, condition, age_years (maximum age).

🧪 Testing & Verification

  Authentication flow: After login, auth-token is stored in sessionStorage. Protected routes (e.g., /app/profile) redirect to login if no token exists.

  Gift list: Main page fetches all gifts from the backend.

  Search: Use the search page with filters; verify results update.

  Profile update: Edit name, save, and see the “Name Changed Successfully!” message.
  
📝 Credits & Acknowledgements

  Course: IBM Full Stack Developer Professional Certificate (Coursera)

  Starter code & guidance: IBM Skills Network

  Implementation & completion: Mihajlo Bjelanovic
