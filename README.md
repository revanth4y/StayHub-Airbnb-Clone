# 🏠 StayHub (Airbnb Clone)

StayHub is a **full-stack web application** inspired by Airbnb, built using **Node.js, Express, MongoDB, and EJS**. Users can explore, create, and manage property listings with **map-based search, image uploads, and secure authentication**.  

This project showcases **frontend development** (responsive EJS templates, interactive maps, forms), **backend development** (Node.js, Express, RESTful APIs), **MVC architecture**, **database modeling with MongoDB**, and **deployment on Render**.

🔗 **Live Demo:** [https://stayhub-jd2n.onrender.com/listings](https://stayhub-jd2n.onrender.com/listings)

---

## 🌟 Features

- 🔐 User authentication (Register / Login / Logout)  
- 🏡 Add, edit, and delete property listings  
- 🖼️ Upload images via Cloudinary  
- 🗺️ Integrated Mapbox interactive maps for locations  
- ✍️ Add and manage reviews  
- 📱 Responsive EJS templates for mobile and desktop  
- 💬 Flash messages for user feedback  
- 🔒 Environment-secured configuration  
- 🏛️ **MVC Architecture:** Clean separation of concerns with **Models** (data), **Views** (UI), and **Controllers** (business logic) for maintainable and scalable code  

---

## 🧰 Tech Stack

- **Frontend:** EJS, HTML5, CSS3, Bootstrap, JavaScript  
- **Backend:** Node.js, Express.js  
- **Database:** MongoDB (via Mongoose)  
- **Authentication:** Passport.js  
- **File Storage:** Cloudinary, Multer, Multer-Storage-Cloudinary  
- **Geocoding & Maps:** Mapbox API  
- **Validation:** Joi  
- **Environment:** dotenv  
- **Deployment:** Render (Server), MongoDB Atlas (Database)  

---

## ⚙️ Installation & Setup
```
1. **Clone the repository**
    bash
    git clone https://github.com/revanth4y/StayHub-Airbnb-Clone.git
    cd StayHub-Airbnb-Clone
2.  Install dependencies:
    npm install
3. Create a .env file in the root directory and add the following environment variables:
   ATLASDB_URL=<your_mongodb_connection_string>
   CLOUDINARY_CLOUD_NAME=<your_cloud_name>
   CLOUDINARY_KEY=<your_cloudinary_api_key>
   CLOUDINARY_SECRET=<your_cloudinary_secret>
   MAP_TOKEN=<your_mapbox_token>
   SECRET=<any_random_secret>
4. Run the development server:
   node app.js
5. Open your browser and visit:
   http://localhost:8080
```
```
🗂️ Folder Structure:

StayHub/
├── models/              # Mongoose models (Listing, Review, User)
├── routes/              # Express routes
├── controllers/         # Controller logic for routes
├── public/              # Static assets (CSS, JS, Images)
├── views/               # EJS templates
├── utils/               # Helper files (error handling, validation)
├── app.js               # Main application file
├── package.json         # Dependencies and scripts
└── .env.example         # Example environment variables

```
```
🔄 How It Works:

.StayHub follows the Model-View-Controller (MVC) design pattern for a clean and maintainable structure.
   
             ┌─────────────┐
             │   User      │
             └─────┬───────┘
                   │
        (Sends request / submits form)
                   │
                   ▼
             ┌─────────────┐
             │   Routes    │
             │ (Traffic)   │
             └─────┬───────┘
                   │
                   ▼
             ┌─────────────┐
             │ Controller  │
             │ (Logic)     │
             └─────┬───────┘
       ┌───────────┴───────────┐
       ▼                       ▼
┌─────────────┐           ┌─────────────┐
│   Model     │           │    View     │
│ (Database)  │           │ (EJS Pages) │
└─────────────┘           └─────────────┘
       │                       ▲
       └───────────────┬───────┘
                       │
      (Data / Response rendered back to User)



1.Flow Example: Adding a Listing
2.User submits a form on /listings/new.
3.Route directs the request to listingsController.createListing.
4.Controller validates the data and saves it via the Listing Model to MongoDB.
5.Updated listings page is rendered in the View with a success flash message.


```
🚀 Future Enhancements: 

- 🔍 Search and filter listings by location and price
- ❤️ Wishlist feature for users
- 🗓️ Booking system with date availability
- 📧 Password reset via email (Nodemailer)
- 🧑‍💼 Admin dashboard to manage users and listings

👨‍💻 Author:
   Revanth Y  
📍 Ballari, India  
📧 revanth.cse.rYmec@gmail.com  <br>
💼 GitHub Profile: (https://github.com/revanth4y)

