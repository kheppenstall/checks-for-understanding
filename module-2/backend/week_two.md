## Week Two - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!). 

Note: When you're done, submit a PR. 

1. At a high level, what is ActiveRecord? What does it do/allow you to do?

  Active Record is an object relational mapper. It maps Ruby objects to a SQL database. ActiveRecord also provides a set of methods (called on a Ruby class) to query a SQL database (translates the ruby method to SQL).
  
2. What kind of methods are `belongs_to`, and `has_many`? (i.e. class or instance) Give an example.

  They are class methods.
  ```ruby
  class Student
    has_many :classes
    belongs_to :school
   end
  ```
3. What do they allow you to do?

  They allow you to create relationships between objects by providing a set of instance methods.
  ```ruby
  Student.first.classes
  Student.first.school
  ```
4. What's the difference between agile workflow and waterfall method?

  Agile workflow is doing sprints to complete discrete features. At the end of every sprint something is produced in its entirety (even if it is small). Waterfall is to complete all like parts at the same time (like all erb files) and to slowly up to the whole product.

5. What is the difference between `#new` and `#create`?

  `#new` makes the object but does not save it in the database. `#create` makes and saves the object.
  
6. At a basic level, what does cURL allow you to do?

  cURL allows you to make an HTTP GET request from the command line and read the html response.

7. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.

  There is a many to many relationship between teachers and students.
  
  ```ruby
  class Student
    has_many StudentTeachers
    has_many Teachers, through: StudentTeachers
  end
  
  class StudentTeacher
    belongs_to Student
    belongs_to Teacher
   end
  
  class Teacher
    has_many StudentTeachers
    has_many Students, through: StudentTeachers
  end
  
  ```
  (I drew it out in my notebook)
  
8. Define foreign key, primary key, and schema.

  Foreign key: Key within an object that identifies a different object
  Primary key: Key that uniquely identifies an object (self)
  Schema: Blueprint to make the database (updated with migrations) 
  
9. Describe the relationship between a foreign key on one table and a primary key on another table.
  
  A foreign key on one table could be the same as a primary key on another table. They could both be pointing at the same object.

10. What are the parts of an HTTP response?

  An HTTP response has a head and a body. The head specifies the details of the message (VERB, protocol, status code, length...) and the body is directions for the browser (what to display or do).
  
11. Describe some techniques to make our Sinatra code more DRY. Give an example of when you would use these techniques.

  Sinatra code can be more DRY with partials. ERB files get repetitive and partials eliminiate the redundancy. Another way to make Sinatra code more DRY (at least than our project) would be to let the controller do its job as an intermediary. Writing Ruby in ERBs means that you often will have to write it more than once. Instead, extract the Ruby to a method in the controller and call it when you need it in the ERB.

### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
2. Name your three favorite ActiveRecord rake tasks and describe what they do.
4. What can you expect from a group as you begin working together? As you continue working together?
5. What two columns does `t.timestamps null: false` create in our database?
6. What cURL flag can you use to send a `POST` request?
7. What case does JSON (and JavaScript) use for multi-word variables?
8. What case does Ruby use for multi-word variables?
9. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
10. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
11. Give an example of when you might want to store information besides ids on a join table.
12. Describe and diagram the relationship between patients and doctors.
13. Describe and diagram the relationship between museums and original_paintings.
14. What are some examples of acceptable values for the parts of an HTTP response?
15. What types of output do we want to test when we test our controllers?
16. What could you see in your code that would make you think you might want to create a partial?
17. Why might you use a helper method?
