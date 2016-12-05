## Week One - Module 2 Recap - Kyle

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

1. List the five common HTTP verbs and what the purpose is of each verb.

  GET: display /read a page

  DELETE: delete from a page / database

  POST: add to a page / database

  PUT: edit a page / database

  HEAD: similar to GET but without the message body (just headers)

2. What is Sinatra?

  Sinatra is a domain specific language (specific to Ruby) used to create web applications. It has built in methods to easily specify paths and parameters and make HTTP requests.

3. What is MVC?

  M: Models,
  V: Views,
  C: Controller

  MVC is an organizational framework to build a web application. Models are the objects. Views are the erb files. Controller handles the paths / requests.

4. Why do we follow conventions when creating our actions/path names in our Sinatra routes?

  We follow conventions to more easily catch errors and so users can manually edit a URL and not be surprised.

5. What types of variables are accessible in our view templates without explicitly passing them?

  Instance variables

6. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
  
  ```ruby
  get '/horses' do
    @count = 1
    erb :index
  end
  ```
  
8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed`?

  ```ruby
  get '/horses' do
    erb :index, :locals => {:count => 1}
  end
  ```

9. What's the purpose of ERB?

  Embedded Ruby lets us use Ruby inside a file mainly written in HTML.

10. Why do I need a development AND test database?

  The development database gives us access to Tux and lets us seed and check things out with shotgun. The test database should reset for each test so we can test parts in isolation. The development database only resets when we manually do it.

11. What's responsive design?

  Design ensure a webpage adjusts sensibly when a browser changing size.
  
12. What is CRUD and why is it important?

  CRUD: Create, Read, Update, Delete

  It is important because those are all common functions a user needs on a website to interact with a database.

13. What does HTTP stand for? 

  Hyper Text Transfer Protocol

14. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?

  `<%= ruby %>` will output to the screen.
  `<% ruby $>` will just run the ruby.

15. What's an ORM?

  Object Relational Model

16. What's the most commonly used ORM?

  ActiveRecord

17. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.

18. What's a migration? 

  A migration is a blueprint for an update to a database. For example, to create a table in a database we would make a migration.
  
19. When you create a migration, does it automatically modify your database?

  No. You need to `rake db:migrate`.
  
20. How does a model relate to a database?

  A database stores instances of a model.
  
21. What's the difference between agile workflow and waterfall method?

  Waterfall builds all the same parts of an application at the same time. So all like parts are done at the same time and then you move on to a new part. For example, make all the erb files at once.
  
  Agile workflow has short sprints that build functional components or features. These components or features then build into the whole application. For example, build CRUD functionality for one model and only make the erb files needed for that model.

22. What is the difference between `#new` and `#create`?

  `#new` makes the object but does not store it in the database. `#create` makes the object and then stores it in the database.
