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
  "role": String   //Admin or user
}
```

### **Products Collection (`products`):**
```json
{
  "_id": ObjectId,
  "category": String,
  "title": String,
  "description": String,
  "price": String,  // Format: "XXX XXXKZT"
  "link": String,   // Product page URL
  "images": Array 
}
```

### **Cart Collection (`carts`):**
```json
{
  "_id": ObjectId,
  "userId": ObjectId,  // Reference to Users Collection
  "productId": ObjectId, // Reference to Products Collection
  "totalPrice": String,
  "imageUrl": String,
  "title": String
}
```

---

## Setup & Installation
### Clone Repository
```sh
git clone https://github.com/sq1der/Clothing-store.git
cd Clothing-store
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

### Product Management
| Method | Endpoint     | Description         |
|--------|-------------|---------------------|
| GET    | `/products`    | Fetch all products  |
| POST   | `/products`    | Add a new product   |
| PUT    | `/product/:id` | Update a product    |
| DELETE | `/product/:id` | Remove a product    |

### Cart Management
| Method | Endpoint         | Description          |
|--------|----------------|----------------------|
| POST   | `/cart`         | Add product to cart      |
| GET    | `/cart`         | View user's cart         |
| DELETE | `/cart/:id`     | Remove product from cart |

---

## License
This project is licensed under the **MIT License**.

---