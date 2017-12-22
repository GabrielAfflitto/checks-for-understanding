## Week Four Recap

### Instructions
Fork this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

* What is a cookie?
  A cookie is a small piece of data that is stored on the client side and has information about each request the user makes
* What’s the difference between a session and a cookie?
  The cookie is informations about the request and a session is the transaction itself which allows for the information to be stored
* What’s a flash and when do you want to use flashes?
  A flash is a type of notice you get during a session, that lets the user know when resources are being CRUDed, for example when something is created or destroyed,
  having a flash notice letting the user know what happened is helpful
* Why do people say “HTTP is stateless”?
  HTTP is stateless because it doesn't save any information abut any request on it's own, thats why we implement sessions and cookies to give it state
* What’s authentication? Explain.
  Authentication is what happens when creating an account or logging in to an account, it's like saying I am who I say I am
* What’s the difference between authentication and authorization?
  Authorization is another step above authentication because it has to do with having access to certain things that a regular user does not have access to.
* What’s a before filter?
  In a controller, a before filter allows you to run a certain method before calling on any action in the controller.
* How do we keep track of a user once they’ve logged in?
  With a session, you start a session once the user is logged in. Using the users primary ID and setting it to current_user
* When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
  namespacing a resource should be done for authorization purposes, for example if you namespace any resource under admin, only an admin should have access to those resources.
  nesting resources should be done depending on the relationship, if a resource belongs to another resource, that resource belonging to the other resource should be nested.
* At a high level, what tools can you use to implement authorization? How would you use them?
  Sessions, cookies, and the role column. Under user, the role column can be used to label a user with a number that can be defined by authorization status
* What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
  an enum lets you label the role column with a string instead of an integer value which gives readability to the user and their authorization status. An enum is declared in the user model
* What are some strategies you can use to keep your views DRY?
  partials, navigations inside of the application.html.erb folder
