## Week Two - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What is Webpack and why is it useful?
Webpack is a compiler that converts all JS to ES5 for browser compatability & compiles & minifies js, css, and html.
2. When do you want to use event delegation?
Event delegation is used to listen for events on a higher "bubble" than the actualy event; you can listen to something on the "outside" & delegate tasks according to the event's target.
3. What's one difference between ES5 and ES6?
ES6 phases out semicolons, uses arrow functions, implements "classes" (similar to constructor functions), uses `const` & `let` instead of `var` and allows parameters to have default values.
4. How are you using the MVC design pattern in your Quantified Self project?
We're implementing models & controllers in files & directors structured similarly to rails. We extracted out SQL queries and other functions related to our "models" according to their responsibility and extracted the callback functions in our "routes" (from server.js) into controllers with functions named like controller actions
5. How do you execute raw SQL in node? 
`.raw(<SQL Query>)`
6. What's a callback function and what are some reasons when we use/need callback functions?
Callback functions are functions that are passed as parameters to other functions; we use them for traversing the dom (when an event occurs, something should happen), and with enumerables. We use it when a function really only needs to be run as the result of another function being called.
7. What is CORS?
CORS allows our front-end local host port to communicate with our back-end localhost port
8. What are some steps to avoid CORS?
Not sure; I thought we wanted to use CORS.

#### Review  

9. Why do people say "HTTP is stateless"?
HTTP is stateless because it doesn't keep track of its state between request & response cycles; the connection between the client & the server is lost after each cycle is over.
10. What is a RESTful API?
A RESTful API is one that implements "representational state transfer" & thereby handles GET (retrieve), POST (create), PUT (update), and DELETE requests.
11. What are some main characteristics of a team following an agile workflow?
An agile team is continually communicating with the client, evolving to satisfy new client and/or owner needs, delivering deployable product, consistently requesting feedback from & supplying feedback to each other, actively participating in stand-ups and retros, and keeping everything organized through a project management tool such as Pivotal Tracker.
12. What are some advantages/disadvantages to using OAuth to authenticate a user?
OAuth provides an easy way for a user to sign-up/log-in to your site and a simple way for your site to ensure the user has a unique property (usually email). It doesn't always provide the properties you want from a user (phone number, user name), so oftentimes internal data collection is required after authentication sign-up. 
