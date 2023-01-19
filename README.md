# Node.js, Express and MongoDB Project Structure 
This is a basic project structure to help you to start building your own RESTful web APIs (for Android, IOS, or JavaScript framworks) using Express framework and MongoDB with a good structure practices based on clean MVC Architecture.


# Features
- Fundamental of Express: routing, middleware, sending response and more
- Fundamental of Mongoose: Data models, data validation and middleware
- RESTful API including pagination,sorting and limiting fields
- CRUD operations with MongoDB
- Security: encyption, sanitization and more
- Authentication with JWT : login and signup
- Authorization (User roles and permissions)
- Error handling
- Enviroment Varaibles
- handling error outside Express
- Catching Uncaught Exception

# Project Structure
- server.js : Responsible for connecting the MongoDB and starting the server.
- app.js : Configure everything that has to do with Express application. 
- config.env: for Enviroment Varaiables
- routes -> userRoutes.js: The goal of the route is to guide the request to the correct handler function which will be in one of the controllers
- controllers -> userController.js: Handle the application request, interact with models and send back the response to the client 
- models -> userModel.js: (Business logic) related to business rules, how the business works and business needs ( Creating new user in the database, checking if the user password is correct, validating user input data)

# Packages
- hpp => Express middleware to protect against HTTP Parameter Pollution attacks.
  HPP puts array parameters in req.query and/or req.body aside and just selects the last parameter value. You add the middleware and you are done.

- xss-clean=> Node.js Connect middleware to sanitize user input coming from POST body, GET queries, and url params. Works   with Express, Restify, or any other Connect app.

- validator=> If you're not sure if your input is a string, coerce it using input + ''. Passing anything other than a string will result in an error.

-helmet=>Helmet helps you secure your Express apps by setting various HTTP headers. It's not a silver bullet, but it can help!

- express-rate-limit=> Basic rate-limiting middleware for Express. Use to limit repeated requests to public APIs and/or endpoints such as password reset. Plays nice with express-slow-down.

- express-mongo-sanitize=> Express 4.x middleware which sanitizes user-supplied data to prevent MongoDB Operator Injection.