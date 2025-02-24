# Programming Courses Platform

### Yerzhan Zholaman 
### Darkhan Serikov
### Meiirzhan Zhumabek

## Overview
This platform provides an interactive environment for learning programming. It includes:
- **Online Compiler**: Execute code in various programming languages directly in the browser.
- **Book Search**: Find books related to programming and coding.
- **Admin Panel**: Manage users by adding, deleting, and editing their information.


## Features
- 📚 **Programming Courses** with structured lessons.
- 💻 **Online Compiler** for hands-on coding experience.
- 🔍 **Book Search** integrated with APIs for finding relevant coding books.
- 🔧 **Admin Panel** for user management
---

## Project Structure
```
3assignment-main/
│── models/             # Frontend assets (CSS, JS, HTML)
|   ├── Item.js
|   ├── User.js
├── public/
|   ├── styleForAdmin.css
|   ├── styles.css
|   ├── stylesForMain.css
├── routes/
|   ├── adminRoutes.js
|   ├── authRoutes.js
|   ├── courseRoutes.js
|   ├── profile.js
│── node_modules/       # Dependencies
├── views/
|   ├── about.ejs
|   ├── admin.ejs
|   ├── compiler.ejs
|   ├── contact.ejs
|   ├── courses.ejs
|   ├── footer.ejs
|   ├── index.ejs
|   ├── login.ejs
|   ├── profile.ejs
|   ├── signup.ejs
|   ├── topic.ejs   
│── server.js           # Main Express server
│── package.json        # Dependencies and scripts
│── package-lock.json   # Dependency lock file
│── .gitattributes
│── README.md          
```

---

## Database Structure
The project uses **MongoDB** with the following collections:

### **Users Collection (`users`):**
```json
{
  "_id": ObjectId,
  "username": String,
  "email": String,
  "password": String,  // Hashed password
  "isAdmin": Boolean
}
```

### **Items Collection (`items`):**
```json
{
  "_id": ObjectId,
  "images": Array,
  "title": String,
  "name_en": String,
  "name_other": String,  
  "description_en": String,  
  "description_other": String
}
```



---

## Setup & Installation
### Clone Repository
```sh
git clone https://github.com/Dorkhan1/MADE/tree/main.git
cd 3assignment-main
```

### Install Dependencies
```sh
npm install
```

### Run the Server
```sh
node server.js
```

---

## Admin Access
To access the admin panel, use the following credentials:

- **Username:** Yerzhan
- **Password:** 1212  

---

## API Endpoints
### User Authentication
| Method | Endpoint       | Description         |
|--------|--------------|---------------------|
| POST   | `/register`   | Register a new user |
| POST   | `/login`      | Log in a user       |

### Item Management
| Method | Endpoint     | Description         |
|--------|-------------|---------------------|
| GET    | `/item`    | Fetch all items  |
| POST   | `/admin/items/add`    | Add a new item  |
| PUT    | `/admin/items/edit/:id` | Update an item    |
| DELETE | `/admin/items/delete/:id` | Remove an item   |



---

## License
This project is licensed under the **MIT License**.

---