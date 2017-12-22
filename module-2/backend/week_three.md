## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What is the entry at the command line to create a new rails app?
  rails new name -T -d="postgres"
2. What do Models generally inherit from in rails?
  From the Database
3. What do Controllers generally inherit from in a rails project?
  from the model
4. How would I create a route if I wanted to see a specific horse in my routes fitle assuming I'm sticking to standard
 conventions and that I didn't want other CRUD functionality?
5. What rake task is useful when looking at routes, and what information does it give you?
  rake routes is helpful as it gives you the CRUD functionality table along with the route helpers
6. What is an example of a route helper? When would you use them?
  An example of a route helper is when you use something like horse_path(horse) instead of "/horses/:id"
  you would use them not only when writing tests but in controller actions such as destroy and create
  as a redirect (e.g. redirect_to horse_path(horse))
7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?

8. What are strong params and why are the necessary?
  strong params are necessary for security purposes. You create a method that takes the params hash
  and calls on the table we are creating, then only permits the selected keys to be assigned or reassigned
9. What role does `form_for` play in helping us create our forms?
  as a helper method, it takes one or two arguments and a block with the form fields
  which renders the form itself and allows us to create those values for the keys in the params
10. How does `form_for` know where to submit the user's input?
  based on the arguments we pass it and the instance variables we set in the controller
11. Create a form using a `form_for` helper to create a new `Horse`.
  <%= form_for @horse do |f|%>
  <%= f.label :name %>
  <%= f.text :name %>
  <%= f.label :breed %>
  <%= f.text :breed %>
  <%= f.submit %>
  <% end %>
12. Why do we want to validate our models?
  to make sure we have the expected information for each table
