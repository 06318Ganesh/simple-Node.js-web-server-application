# simple-Node.js-web-server-application
A simple Node.js web server application that interacts with MongoDB to manage users, posts, and comments. This project includes creating a set of RESTful API routes to load data, retrieve, update, and delete users and related information. The server is built using TypeScript and MongoDB for data persistence."


This project is a Node.js web server built with TypeScript, designed to interact with a MongoDB database. The server handles users, posts, and comments, allowing CRUD (Create, Read, Update, Delete) operations through well-structured RESTful APIs. It fetches data from JSONPlaceholder, a free fake API, and stores it in MongoDB for manipulation and retrieval.

Project Features:
Data Initialization:

On initial setup, the server loads user, post, and comment data from JSONPlaceholder API into a MongoDB database. This data is used for performing CRUD operations.

CRUD Operations:

Create, Read, Update, and Delete operations are implemented for users, posts, and comments. These operations are exposed via RESTful API routes, allowing you to interact with the database.

RESTful API Design:

The server exposes GET, POST, PUT, and DELETE endpoints for interacting with users, posts, and comments. These APIs follow REST conventions for consistency and scalability.

MongoDB Integration:

MongoDB serves as the database for storing user data, posts, and comments. It supports fast, scalable data storage and retrieval, especially suited for semi-structured data like posts and comments.

TypeScript for Type Safety:

The server is built using TypeScript, providing type safety, better code maintainability, and reducing runtime errors. It ensures that the application is less error-prone during development.

Modular and Scalable Architecture:

The application’s architecture is designed to be modular, allowing easy expansion by adding more features or services. The API routes and database interactions are decoupled to allow for easy management and scaling.

How to Initialize and Run:
Clone the Repository:

bash
Copy
Edit
git clone https://github.com/06318Ganesh/simple-Node.js-web-server-application
cd simple-nodejs-web-server
Install Dependencies:

Run npm install to install the required dependencies:

bash
Copy
Edit
npm install
Setup MongoDB:

Ensure you have MongoDB installed and running on your machine, or use a cloud-based MongoDB provider like MongoDB Atlas.

Set up the connection URL for MongoDB in the src/database.ts file.

Start the Server:

Once the dependencies are installed and MongoDB is set up, start the server using the following command:

bash
Copy
Edit
npx ts-node src/index.ts
Load Data into MongoDB:

On the first run, the server will fetch data from JSONPlaceholder API and populate the MongoDB database with users, posts, and comments.

API Routes You Can Test:
Once your server is running (after running npx ts-node src/index.ts), you can test the following routes using your browser or Postman:

✅ Get All Users

URL:
http://localhost:3000/users

Method: GET

✅ Get All Posts

URL:
http://localhost:3000/posts

Method: GET

✅ Get All Comments

URL:
http://localhost:3000/comments

Method: GET

✅ Get Posts by User ID (e.g., user ID = 1)

URL:
http://localhost:3000/users/1/posts

Method: GET

✅ Get Comments by Post ID (e.g., post ID = 1)

URL:
http://localhost:3000/posts/1/comments

Method: GET

Expected Output:
Server Start: The server will start successfully, and you should see the following message:

bash
Copy
Edit
✅ Connected to MongoDB
Server running on http://localhost:3000
Data Loaded: After running the server for the first time, you will see the message:

bash
Copy
Edit
✅ Users, Posts, and Comments loaded to MongoDB.
This confirms that the data has been fetched from the JSONPlaceholder API and stored in MongoDB.

API Endpoints:
GET /api/users – Retrieves all users.

GET /api/users/:id – Retrieves a specific user by ID.

POST /api/users – Creates a new user.

PUT /api/users/:id – Updates an existing user by ID.

DELETE /api/users/:id – Deletes a user by ID.

GET /api/posts – Retrieves all posts.

GET /api/posts/:id – Retrieves a specific post by ID.

POST /api/posts – Creates a new post.

PUT /api/posts/:id – Updates an existing post by ID.

DELETE /api/posts/:id – Deletes a post by ID.

GET /api/comments – Retrieves all comments.

GET /api/comments/:id – Retrieves a specific comment by ID.

POST /api/comments – Creates a new comment.

PUT /api/comments/:id – Updates an existing comment by ID.

DELETE /api/comments/:id – Deletes a comment by ID.

Conclusion:
This Simple Node.js Web Server/Application provides a clean and structured approach to developing backend services using Node.js, MongoDB, and TypeScript. It offers an excellent foundation for anyone interested in understanding how to handle basic backend operations, including interacting with APIs, managing databases, and creating RESTful APIs.
