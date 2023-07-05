# Blog created with NODE, EXPRESS, EJS, MONGODB ATLAS, and an MVC approach. 
👇👇👇 Read more about how it is built below the video. 👇👇👇
***
***

https://github.com/vanesascode/blog-node-express-ejs-mdbatlas-mvc/assets/131259155/2cd25228-790b-4b43-b5f7-fa975d365c88

***
***

'YOUR DEVELOPMENT BLOG’ is created with Express, a popular framework for creating web applications in Node.js, and has an MVC approach.

## 🔹 MVC:

>MVC stands for Model-View-Controller. It is a software architectural pattern used in web development to separate the application's logic into three interconnected components: the model, the view, and the controller.

The MVC pattern promotes separation of concerns, making the codebase more modular, maintainable, and scalable. It allows for easier code reuse, as each component has a specific responsibility. Changes made to one component do not affect the others, enabling developers to work on different parts of the application simultaneously. Additionally, MVC facilitates the implementation of test-driven development and promotes code organization and readability.

## 🔹 SERVER:

In the app.js file we find a basic Express.js server that connects to a MongoDB database and sets up routes for a blog application. It sets the view engine to EJS (Embedded JavaScript) for rendering dynamic HTML templates. It sets up MIDDLEWARE functions:

- express.static('public') serves static files from the "public" directory.
- express.urlencoded({ extended: true }) parses incoming request bodies.
- morgan('dev') logs HTTP requests to the console.
- (req, res, next) => { ... } is a custom middleware function that sets the "path" variable in the response locals object.

## 🔹 ROUTES:

App.js defines two routes: - The root route ("/") redirects to the "/blogs" route. - The "/tips" route renders the "tips" view with a title of "Tips to write blog posts". It sets up the "/blogs" route to use the blogRoutes.js file inside the routes folder for handling blog-related routes. It defines a default 404 route that renders the "404" view with a title of "404".

## 🔹 CONTROLLER:

>"The controller acts as an intermediary between the model and the view. It handles user input, processes requests, and updates the model or selects the appropriate view to render. The controller receives input from the user through the view and decides how to respond to it. It updates the model based on the user's actions and sends the updated data to the view for display. "

The blogRoutes.js file defines several routes that will be handled by the blogController module, where the blog operations functions are. The routes include handling GET and POST requests for creating a blog, retrieving all blogs, retrieving a specific blog by its ID, and deleting a blog by its ID.

## 🔹 VIEWS:

>"The view is responsible for the presentation layer of the application. It defines how the data is displayed to the user. It generates the HTML markup, CSS styles, and may include some client-side scripting. The view receives data from the controller and renders it to the user interface. Multiple views can be created to represent different visual representations of the same data."

In the Views folder we have HTML templates using the EJS (Embedded JavaScript) templating engine. It is used to dynamically generate HTML content based on the data provided.
We also find a folder with partials. Partials are reusable components or sections of a view that can be included in multiple views. They allow you to break down the HTML code into smaller, modular pieces, making it easier to manage and maintain your codebase. These partials can be included in multiple views using the `<%- include("./partials/partial-name.ejs") %> syntax

## 🔹 MODELS:

>"The model represents the application's data and business logic. It encapsulates the data and provides methods to manipulate and access that data. It is responsible for data validation, retrieval, storage, and any other operations related to the data. In a web application, the model typically interacts with the database or any other data source."

In the folder ‘Models’ there is the file ‘blog.js’ which is an Schema used to define the structure of a blog entry in a database using Mongoose. This establishes the rules and data types that must be met when creating a new blog entry.

## 🔹 MONGODB ATLAS - MONGOOSE:

The database is gathered at the cloud MongoDB service called Atlas. It is used along with Mongoose, which is a popular Node.js library for working with MongoDB.

## 🔹 PUBLIC:

As mentioned before, everything in this folder is going to be accessable at the root level on the website, from the browser thanks to the static middleware that comes along when using Express. It allows us to serve static assets such as HTML, CSS, JavaScript, images, etc. to clients accessing the application.


# ✔️ HOW TO RUN THE NODE SERVER:

1 - In the terminal, run 'node app'. Or 'nodemon app' if you have [installed it](https://github.com/remy/nodemon) It is useful so you don't have to refresh the server all the time everytime you make changes to the code.

2 - In the browser, go to the site: http://localhost:3000/
