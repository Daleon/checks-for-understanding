## Week Two - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!). 

Note: When you're done, submit a PR. 

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
  A database which can utilize relationships between sets of data.
  
2. What kind of methods are `belongs_to`, and `has_many`? (i.e. class or instance) Give an example.
  ActiveRecord Methods

3. What do they allow you to do?
  Establish relationships between sets of data, based upon the assumption that there is only one of something to many of
  another.  These methods allow us to automatically make those connections within the ActiveRecord Database.

4. What's the difference between agile workflow and waterfall method?
   Agile workflow works on all aspects of the project at small intervals.  Whereas, waterfall does each portion of the process
   in signifigantly larger "chunks".
  
5. What is the difference between `#new` and `#create`?
  #new creates and instance of an ActiveRecord object, but is not saved to ther database.  Whereas #create does just that.  It
  both creates a new instance Object of the data, and also saves it in one command.

6. At a basic level, what does cURL allow you to do?
   Data transfer by script...?  I think ... ?
  
7. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
  One student for every teacher.  Many students for every teacher.  Thus...  Teacher has_many :students, and Students
  belongs_to :teachers
  
8. Define foreign key, primary key, and schema.
  Foreign Key is the key associated with the direct relationship between two sets of data in ActiveRecord.  Primary key is the
  key associated with the appropriate data object within a set of data - this is the id number...   Schema file is
  automatically generated when we perform a rake db:migrate - NEVER MANUALLY CHANGE THIS FILE!!!!

9. Describe the relationship between a foreign key on one table and a primary key on another table.
  The foreign key is only used for the relationship from one set of data to another.  If you have a primary key, it will only
  give you information within that ActiveRecord set of data.  All tables generate the same numbers, but are directly connected
  to thir respective sets, preventing confusion.
  
10. What are the parts of an HTTP response?
  Request, Authentication, Response, Permission .... ?   ...  I have no idea ...  

11. Describe some techniques to make our Sinatra code more DRY. Give an example of when you would use these techniques.
  When you have relatively small databases.

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
