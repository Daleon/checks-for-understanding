## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What is the entry at the command line to create a new rails app?
  rails g new app_name
2. What do Models generally inherit from in rails?
  ActiveRecord::Base
3. What do Controllers generally inherit from in a rails project?
  ActionController::Base
4. How would I create a route if I wanted to see a specific horse in my routes fitle assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
  resources :horses only: [:view]
5. What rake task is useful when looking at routes, and what information does it give you?
  bundle exec rake routes
6. What is an example of a route helper? When would you use them?
  root_url or root_path 
7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
  "_path" will only stay on the server, based upon the controller & router setup.  If we use the _url version, then we end up
  giving/using the acutal IP address, server information, and a lot of other highly detailed information which is not generally
  needed when building route helpers.
8. What are strong params and why are the necessary?
  they are used to establish paramerters which can & cannot be changed.  We establish which ones in our private methods, which
  are in the controller.
9. What role does `form_for` play in helping us create our forms?
  Mostly, when we want to nest an html.erb file into another; however, it can also be used as a sort-of helper, if you use a
  ../new.html.erb & ../edit.html.erb files for instance.  
10. How does `form_for` know where to submit the user's input?
  We need to place an instance variable after our form_for to tell rails what the form is actually for...  The instance 
  variable is of course, created in the respective controller file, prior to passing the object into the html.erb file we've 
  built for it.
11. Create a form using a `form_for` helper to create a new `Horse`. 
  <%= form_for @something do |f| %>
  <%= f.title :title %>
  <%= f.text_field :title %>
  <% end %>
12. Why do we want to validate our models?
  We do not want to create incomplete, or inaccurate ActiveRecord files we are looking to manipulate down the line.  If the 
  data is not there to manipulate, it can cause a lot of other errors during and after the build.
