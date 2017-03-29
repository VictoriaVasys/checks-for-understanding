## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What is the entry at the command line to create a new rails app?
`rails new <filename>`

2. What do Models generally inherit from in rails?
`ActiveRecord::Base`

3. What do Controllers generally inherit from in a rails project?
`ApplicationController`

4. How would I create a route if I wanted to see a specific horse in my routes fitle assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
`get '/horse/:id', to: 'horses#show' as: :horse`

5. What rake task is useful when looking at routes, and what information does it give you?
`rake routes`; it gives you the prefix, verb, URI pattern, and Controller#Action for each route

6. What is an example of a route helper? When would you use them?
`horse_path`; you would use them when you use the link_to method in erb which translates it into the correct HTML format for a link (e.g. `link_to horse.name horse_path(@horse)`)

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
appending `_url` gives you the absolute path (that you would enter in your browser), while appending `_path` gives you the relative path within your project

8. What are strong params and why are the necessary?
Strong params are ones that you explicitly allow access to within your project; they're necessary because Rails has built-in protections that don't allow you to access a nested hash within the params method hash in order to prevent malicious params-altering which can defect your db.

9. What role does `form_for` play in helping us create our forms?
It's a form helper; it allows you to pass an object in & use the form for either adding new or editing a current object based on its evaluation of `record_new?` on the object. It provides shortcuts that translate to proper HTML, allows you to base your form structure on the object's attributes & automatically labels your submit button according to the model name and type of form (new or edit).

10. How does `form_for` know where to submit the user's input?
It knows based on whether the object is a new record; if so, it submits to the #create method; if not, it submits to the #update method.

11. Create a form using a `form_for` helper to create a new `Horse`. 
```ruby
<%= form_for(@horse) do |f| %>
  <%= f.label :name %>
  <%= f.text_field :name %>
  
  <%= f.label :history %>
  <%= f.text_area :history %>
  
  <%= f.submit %>
<% end %>
```

12. Why do we want to validate our models?
Validating models is important because we want to make sure that any essential attribute is given a value before it enters our database (e.g. if there wasn't a number in an address, it would be an invalid address & would mess with things when accessing/manipulating/implementing our db- the letter would be returned if we tried to send an envelope with an invalid address & the postage payment would be wasted)
