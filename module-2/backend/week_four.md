## Week Four Recap

### Instructions
Fork this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

* What is a cookie?

A cookie is a hash-like object sent along an HTTP request and also stored locally on the browser.

* What’s the difference between a session and a cookie?

A session is a secure type of cookie. A session hashed when sent in an HTTP request / response.

* What’s a flash and when do you want to use flashes?

A flash is a hash that is used to show messages to a user. We use it to send messages like "name can't be blank."

* Why do people say “HTTP is stateless”?

Every HTTP request / response does not depend on any that came before it. The previous requests / responses do not matter - only the current one. This is why we need cookies.

* What’s authentication? Explain.

Authentication is answering the question who are you? It is a website verifying that you are who you say you are.

* What’s the difference between authentication and authorization?

Authentication is who are you? Authorization is who gets what privileges on the site?

* What’s a before filter?

Before all actions in a controller do this other action / filter.

* How do we keep track of a user once they’ve logged in?

We start a session like this `session[user_id] = @user.id`.

* When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?

We nest resources when both are objects in the database. For example, users are objects / rows in the database and so are ideas. But ideas are specific to a user so we so we would nest ideas under users. We namespace when the outer "name" is not an object. For example there is no admin table in the database so we might namespace categories under admin.

* At a high level, what tools can you use to implement authorization? How would you use them?

We can use before_filters to verify there is a session started and that the user id in the session matches the user id in the url. These before_filters can redirect us to a page that a visitor has access to if a visitor trieds to go to a page they are not authorized to visit.

* What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?

An enum maps an integer to a string. It offers the advantage of easy comparisons and clear differentiation. An integer needs to be in the database to use an enum. We declare an enum in the model file (like `idea.rb`). 

* What are some strategies you can use to keep your views DRY?

We can use partials to extract repeated code or use helper methdos for repeated ruby. 
