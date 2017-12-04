## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

1. List the five common HTTP verbs and what the purpose is of each verb.
  Get - retrieves a resource or information
  Post - creates a resource, submits information for processing
  Put - Updates a resource
  Delete - deletes a resource
  Patch - updates only a piece of the resource
2. What is Sinatra?
  Sinatra is a ruby framework for creating web apps
4. What is MVC?
  Model, View, Controller is the convention by which web apps are built. Starting at the Controller,
  the user makes a request, then the controller looks to the model for the information as the model
  interacts with the database and handles the logic, then the Model send that information back to the Controller
  which then updates the views and what is on the views appears on the browser.
5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
  It keeps our code organized and decreases the chances of having bugs.
6. What types of variables are accessible in our view templates without explicitly passing them?
  Instance Variables
7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb`
template


  ```ruby
  get '/horses' do
    @count = Horse.all.count
    name = Horse.where(:name = 'Mr. Ed')
    erb :index
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
9. What's the purpose of ERB?
  Embedded Ruby or erb is a way of being able to implement some ruby code in an HTML file
10. Why do I need a development AND test database?
  The test database might be smaller so it can make running test a lot faster
11. What is CRUD and why is it important?
  Create, Read, Update and Delete. CRUD is the what we call the functionality that is executed through the model and the controller.
12. What does HTTP stand for?
  Hyper Text Transfer Protocol
13. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
  <%= %> and <% %>. The code inside of the equal sign will actually be outputted to the browser
14. What's an ORM?
  Object Relational Mapper is a way to communicate with different data sources such as our database. That is what Active Record is for
15. What's the most commonly used ORM in ruby (Sinatra & Rails)?
  Activerecord
16. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.

17. What's a migration?
  Moving the database information from one database from one platform to another
18. When you create a migration, does it automatically modify your database?
  Not until you seed the database
19. How does a model relate to a database?
  The model is the one that actually interacts with the database and pulls information from it, then sends it to the controller
20. What is the difference between `#new` and `#create`?
  #new will create a new instance and #create will create a new resource
Review Questions:  
21. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?  
  Film.create(:id = row[:id], :title = row[:title], :description = row[:description])
22. Given the following hash:
```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone'],
  brunch: {cost: $35, supplies: ['mimosa flutes'],
  antiquing: {cost: $200, supplies: ['list of antique stores']
}
```
How would I add 'granola bar' to things you should have when hiking?
  activities.values[-1].values.map do |supplies|
    supplies.shift("granola bar")
  end
23. What are the 4 Principles of OOP? Give a one sentence explanation of each.
  abstraction - using a method without having to know all of the inner details, similar to the relationship between controller and model
  encapsulation - hiding data implementation by restricting access to public methods
  inheritance - taking certain attributes or methods from a parent class
  polymorphism - many forms from one name
