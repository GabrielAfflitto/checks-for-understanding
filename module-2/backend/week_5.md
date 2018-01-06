1. How do we make flash messages display on a page?
  flash messages are displayed on the page by being rendered in the view by using the flash.each method. They are also defined in the controller with flash[:notice] = "notice"
2. Where is cart information/temporary information usually stored?
  Cart information is usually stored in a PORO(plain old ruby object) called Cart, which is essentially a class that returns a hash with an items id as they keys and the quantity as the values
3. What might be some reasons not to store cart in our database? Are there any reasons why we would want to persist that information?
  We may not want to store cart in our database because the database should be used for finalized information, and when a user adds things to their cart, it doesn't mean they will actually buy anything or checkout or change the inventory, so it's not until checkout that we should actually put the cart information in the database.
4. What is the purpose of the asset pipeline?
  The purpose of the asset pipeline is to embed Javascript
5. Why do we precompile our assets?
  For readability purposes
6. What do each of the following tags do?
  image_tag lets us render an image to a page
ruby
<%= stylesheet_link_tag "application" %>
<%= javascript_include_tag "application" %>
<%= image_tag "rails.png" %>

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?
  A great read me should have code snippets, clear instructions, history of the project, list of collaborators. Updating the readme is beneficial in the sense that it helps us be able to explain our code, talk about our thought process and help someone look at this project with a better understanding of how everything works
8. What are the top four accessibility issues that we as developers should be aware of?
  visual, mobility, cognition
9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?
  'before_save' is a callback, a 'before_save' can be found in the models, but they should be used be used very rarely
10. Given the following object, how would we create a scope for all users who are active?

```ruby
User.create(name: "Happy", active: true)
```

11. What is the difference between a scope and a class method?
a class method is a method that is called on the entire class and a scope is called before a class is instantiated
