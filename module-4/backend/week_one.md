## Week One - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What's the most useful thing you learned from completing the intermission week work?
It's a tie between using 'var', 'return', and array prototype methods. I haven't yet used constructor functions, but I imagine they're really important for OOP.
2. What are some tools to help debug JavaScript code?
console.log()
debugger
pryjs
3. What are some tools you need in order to unit test your JavaScript?
mocha & chai
4. What is the syntax for invoking a function?
nameOfFunction()
5. What's the difference between `==` and `===` in JavaScript?
`==` will eval to true for different datatypes (eg. "1" == 1), `===` is exactly equal to, meaning it will only evaluate to true if both values are equal and the same datatype.
6. What's the difference between asynchronous and synchronous JavaScript? 
Asynchronous JS continues to run, no matter order and regardless of req/response (eg. in our tests we need to provide `done()` to indicate that the test can move on); synchronous is much like Ruby where it runs in the order (and/or hierarchy) that we indicate
7. How do we setup a route when creating an API with Node and Express?
we define an app then
app.get('path/pathname', function(request, response){})
8. What do we use Knex for?
Knex gives us similar functionality as ActiveRecord; it allows us to connect to the psql Database. It also allows us to make migrations & seeds & we use `.raw()` to run SQL queries. 
9. What's `npm` and what do we use it for?
npm is Node Package Manager and it allows us to include various js libraries in our app.

#### Review  
10. What's the MVC design pattern? Describe each part of MVC?
Model-View-Controller; Model is where we define relationships & make calculations; View is where we decide what information to send to the browser (in http format) & Controller is where we define the actions that can occur based on the route & http verb request. The client reaches the controller first, which reaches to the model to gather any data & then provides that information to the view.
11. What is AJAX? What are some benefits of using AJAX?
AJAX is a tool used to asynchronously make requests to either the database or an outside source (so you don't have to load the page in order for changes to occur)
12. What's a background worker? When would we want to use a background worker?
A background worker performs tasks in the background; it is very useful for completing things that the user doesn't need to know about while the browser refreshes or redirects so they can continue to perform actions without waiting for the task to complete (e.g. mailers)
