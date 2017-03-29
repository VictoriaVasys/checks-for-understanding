## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

1. List the five common HTTP verbs and what the purpose is of each verb.
GET
POST
HEAD
PUT
DELETE
2. What is Sinatra?
Sinatra is a Ruby framework for building web apps.
4. What is MVC?
MVC is the general setup for web app framework directory structure; Models, Views, Controller
5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
Because Sinatra has built-in functions that implement an HTTP request/response cycle & they won't work properly if we don't follow the conventions.
6. What types of variables are accessible in our view templates without explicitly passing them?
Instance variables
7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
  
  ```ruby
  get '/horses' do
    @count = 1
    name = "Mr. Ed"
    erb :index, locals: {identity: name}
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?

9. What's the purpose of ERB?
ERB is short for Embedded Ruby; it allows you to implement Ruby within HTML code.
10. Why do I need a development AND test database?
Your test datababse is ideally wiped clean at the end and beginning of every test; you need a separate development database in order to make sure your app behaves appropriately with the larger dataset that you want it to. 
11. What's responsive design? 
Responsive design is a method of allowing your app to be cross-compatible amongst devices with different screen sizes; the content re-sizes & moves appropriately when the screen re-sizes.
12. What is CRUD and why is it important?
CRUD stands for Create, Read, Update, Delete; it is the functionality required for any set of data within an app & is important because it's the widely-used standard for building web apps.
13. What does HTTP stand for? 
HyperText Transfer Protocol
14. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
<%= ruby_code %> or <% ruby_code %>; the first will run ruby code and render it to the display; the second will run code but not render to the display.
15. What's an ORM?
Object-relational Map! It's a schematic that helps us visualize what attributes (columns) our tables have and how the connect and interconnect to other tables in our database (primary keys are connected to foreign keys).
16. What's the most commonly used ORM in ruby (Sinatra & Rails)?
WWW SQL Designer (http://ondras.zarovi.cz/sql/demo/); saves & loads in XML format.
17. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
C get '/items/new'
C post '/items'
R get '/items'
R get '/items/:id'
U get '/items/:id/edit'
U put '/items'
D delete '/items/:id'
18. What's a migration? 
A migration is a function that allows us to add to, update, or delete from our database.
19. When you create a migration, does it automatically modify your database?
No! You must `rake db:migrate`
20. How does a model relate to a database?
A model sends requests to a db with various methods (usually in SQL) & the db sends data back based on the request.
21. What's the difference between agile workflow and waterfall method?
Waterfall is linear & predicts what will happen from the very beginning; Agile is cyclical & continually changing; it attempts to accomplish things as they arise.
22. What is the difference between `#new` and `#create`?
#new creates an instance of a class, but it just lives in the ether/p; #create creates the instance & saves it to the database.

