### Week 5 Questions

Re-pull from this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 5 Questions
1. How do we make flash messages display on a page?
We print them to the html page in the layout.html.erb by storing them as a hash that looks something like flash[:success] = "#{blah.name} added!"

2. Where is cart information/temporary information usually stored?
In a cookie.

3. What might be some reasons not to store a cart in our database? Are there any reasons why we would want to persist that information?
Because their nature is inherently not permanent, they are constantly changing, the attributes or items in them aren't consistent, etc.  Not specifically for the cart, you would want their eventual order information from the cart stored however.

4. What is the purpose of the asset pipeline?
To provide a more condensed format to pass information to the client.  It allows programmers to seperate our work by files and folders but then allows the compiling (and minimizing) of those documents to pass more quickly to the user.

5. Why do we precompile our assets?
In order to allow heroku(etc) to have access to them.

6. What do each of the following tags do?
```
<%= stylesheet_link_tag "application" %>
<%= javascript_include_tag "application" %>
<%= image_tag "rails.png" %>
```
They give the asset pipleline access to the specific assets in the tags. So the stylesheet_link_tag gives access to the application.css file, the javascript_include_tag gives access to the application.js file and both those files require the necessary files under them that need compiling.  The image_tag gives access to that image file.

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?
Organization, readability, setup, troubleshooting, base use scenario.  It gives us practice writing them.

8. What are the top four accessibility issues that we as developers should be aware of?
Did we ever discuss this?????

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?
It's an example of a callback.  We would find it at the top of our model and it (in the case of before_save would run whatever method before a save to the database.)

10. Given the following object, how would we create a scope for all users who are active?
User.where(active: true)

```ruby
User.create(name: "Happy", active: true)
```

11. What is the difference between a scope and a class method?
A scope is essentially a class method being run on a smaller subset of objects. We have seen this the most when dealing with objects that have relationships. IE we want to see what snacks are in a certain machine.


### Review Questions:  
12. Given the following hash:  

```ruby
{cart: {"17" => 4, "204" => 52, "29" => 22}}
```

  12a. How would you add item with id of 48 with a quantity of 4?  
  cart['48'] = 4
  12b. How would you increase the quantity of item 29?  
  cart["29"] += 1
  12c. How would you find out how many items your user is thinking about purchasing?   
  cart.values.sum

13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications?  
Polymorphis is the ability to send different types of things to something to get them to do different things based on what they are, you do this in rails by treating active record associations as arrays.

14. How would you clean the string "(630) 854-5483" to "630.854.5483"?
phone_number = "(630) 854-5483"
formatted_number = [num[1..3], num[6..8], num[10..13]].join('.')



### Self Assessment:
Choose One:

* I was able to answer most questions independently, but utilized outside resources for a few


Choose One:

* I feel comfortable with the content presented this week
