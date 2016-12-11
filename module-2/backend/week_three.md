## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What is the entry at the command line to create a new rails app?

 `rails new project_name -T --database=postgresql --skip-turbolinks --skip-spring`

2. What do Models generally inherit from in rails?

 `< ApplicationRecord`

3. What do Controllers generally inherit from in a rails project?

 `< ApplicationController`

4. How would I create a route if I wanted to see a specific horse in my routes fitle assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?

 `get '/show', to: 'articles#show'`
 
5. What rake task is useful when looking at routes, and what information does it give you?

 `rake routes`
 It lists all the routes in the controller with their prefix, verb, URI pattern, and controller method.

6. What is an example of a route helper? When would you use them?

 An example is `article_path(article`. We se them to specify a route outside of the router, like in an erb file.

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?

 `_url` gives a path from the root (including whole url) and `_path` gives a relative path.

8. What are strong params and why are the necessary?

 Strong params are params that a developer has explicitly allowed using the permit and require methods in the controller. They are necessary so a site does not blindly accept any params inputted.
 
9. What role does `form_for` play in helping us create our forms?

 `form_for` is a helper method that takes an argument of a model instance that makes it easier to make forms with a params hash formatted as we'd like, and with the attributes of the model passed in.
 
10. How does `form_for` know where to submit the user's input?

 It knows to put it in the params hash. The key of the inputs is the name of the model (like `:article`) and then there are nested arrays of types specified in the enumerable like  `f.label :title`.
 
11. Create a form using a `form_for` helper to create a new `Horse`.

 ```ruby
 <% form_for(@horse) do |f| %>
  <p>
   <%= f.label :Name %><br />
   <%= f.text_field :name %>
  </p>
  <p>
   <%= f.label :Age %><br />
   <%= f.text_field :age %>
  </p>
  <p>
   <%= f.label :Description %><br />
   <%= f.text_area :description %>
  </p>
  <p>
   <%= f.submit %>
  </p>
 <% end %>
 ```

12. Why do we want to validate our models?
 If a model does not have any validations then it could just have an id. Sometime there are essential attributes to a model so we would want to validate that any instance of the model has that attributes. Also, if we are displaying the attributes on the page, nothing would appear for `@article.name` if the article did not have a `name`.
