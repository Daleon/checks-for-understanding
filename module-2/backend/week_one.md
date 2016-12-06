## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

1. List the five common HTTP verbs and what the purpose is of each verb.
  POST, GET, PUT, DELETE

2. What is Sinatra?
  A lightweight version of Ruby on Rails.
  
4. What is MVC?
  Model View Controller
  
5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
  Consistency throughout the code.  Makes for easier debugging/troubleshooting.
  
6. What types of variables are accessible in our view templates without explicitly passing them?
  Instance, Local, and Class variables.

7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
  
  ```ruby
  get '/horses' do
    @count = 1
    erb :index
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed`?
    ```ruby
  get '/horses' do
    name = 'Mr. Ed'
    @count = 1
    erb :index
  end
  ```

9. What's the purpose of ERB?
  It is utilized by sinatra to allow Ruby code to be passed through CSS & HTML.
  
10. Why do I need a development AND test database?
  Such that you do not contaminate the test assertions by making permanant alterations to the database.

11. What's responsive design?
  When software looks for the client's display requirements and changes the display accordingly to the user's display needs.
  
12. What is CRUD and why is it important?
  It gives us a framework to build our main controller file.

13. What does HTTP stand for? 
  Hypertext Transfer Protocol
  
14. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
  Through the use of the <%= %> tag
  
15. What's an ORM?
  Object Relation Mapping
16. What's the most commonly used ORM?
  C++  ??

17. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full     CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
  
  ##See all restaurants.  It is a Read process.##
  get '/restaurants' do
    @restraunts = Restraunt.all
    erb :index.erb
  end
  
  ##See one restaurant.  It is a Read Process##
  get '/restaurants/:id' do |id|
    @restaurants = Restaurant.find(id)
    erb :show.erb
  end
  
  ##View Form to enter new Restaurant.  It is a Create Process.##
  get '/restaurants/new' do
    erb :new.erb
  end
  
  ##Submit and save new Restaurant.  It is a Create Process.##
  post '/restaurants' do
    Restaurant.create(params[:restaurant])
    redirect '/restaurants'
  end
  
  ##See Form to edit already existing Restaurant.  It is an Update Process.##
  get '/restaurants/:id/edit' do |id|
    @restaurants = Restaurant.find(id)
    erb :edit.erb
  end
  
  ##Click Submit to update a Restaurant.  It is an Update Process.##
  put '/restaurants/:id' do |id|
    Restaurant.update(params[:restaurant], id)
    redirect '/restaurants/:id'
  end
  
  ##Deletes a Restaurant.  It is a Delete Process.##
  delete '/restaurants/:id' do |id|
    Restaurant.delete(id)
    redirect '/restaurants'
  end
  
 
  
  
18. What's a migration? 
  It takes data (in key/value pairs) from ActiveRecord, and creates a semi-organized Table for the information specified.
  
19. When you create a migration, does it automatically modify your database?
  No..?  I think ...?  It affects HOW the data is entered INTO the database (which is done afterwards), by automatically
  creating files which fetch and store data based upon the criteria in the migration.
  
20. How does a model relate to a database?
  It stores methods and "rules" (if you will) about how the data IN the database is accessed.  It gives the rules and
  process, it doesn't actually do the fetching.  It has the methods for doing so...
  
21. What's the difference between agile workflow and waterfall method?
  Waterfall Workflow builds the program in large chunks.  This leaves little opportunity to catch a mistake early on in the
  development process.  Generally testing (if any) is done after the code is written.  This is a process I prefer to avoid.
  Agile Workflow builds the software in small stages, but includes all stages of the software be done for each "smaller"
  stage.  This can ensure signifigantly less major problems with the software throughout development.  It takes a little
  longer, and requires more disciplined coders but is my preffered process.
  
22. What is the difference between `#new` and `#create`?
  #new will make a new thing for the database, but will not save it.  You need to perform #save on whatever you created to
  have it be saved in the database.  If you use #create, you don't need to save.  It's automaticall saved into the database.
