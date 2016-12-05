## Week One - Module 2 Recap - Kyle

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

#### 1. List the five common HTTP verbs and what the purpose is of each verb.

GET: display /read a page
DELETE: delete from a page / database
POST: add to a page / database
PUT: edit a page / database
HEAD: similar to GET but without the message body (just headers)


#### 2. What is Sinatra?
#### 3. What is MVC?
#### 4. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
#### 5. What types of variables are accessible in our view templates without explicitly passing them?
#### 6. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
  
  ```ruby
  get '/horses' do
    erb :index
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed`?
9. What's the purpose of ERB?
10. Why do I need a development AND test database?
11. What's responsive design?
12. What is CRUD and why is it important?
13. What does HTTP stand for? 
14. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
15. What's an ORM?
16. What's the most commonly used ORM?
17. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
18. What's a migration? 
19. When you create a migration, does it automatically modify your database?
20. How does a model relate to a database?
21. What's the difference between agile workflow and waterfall method?
22. What is the difference between `#new` and `#create`?
New makes the object but does not store it in the database. Create makes the object and then stores it in the database.
