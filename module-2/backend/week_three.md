## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

1. What is the entry at the command line to create a new rails app?
* rails new

2. What do Models generally inherit from in rails?
* ApplicationRecord

3. What do Controllers generally inherit from in a rails project?
* ApplicationController

4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
```
def show
  @horse = Horse.find(params[:id])
end
```

5. What rake task is useful when looking at routes, and what information does it give you?
* rails routes / rake routes

6. What is an example of a route helper? When would you use them?
* horse_path(@horse)
* horses_path

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
* I'm not at all sure what this question is even asking, but perhaps you what the diffence between the uri and the route helper?
the uri would look like '/horses/id/edit' where the path would be edit_horse_path(horse)

8. What are strong params and why are they necessary?
* Strong params are a way of only passing to the database form info that we are specifically asking for.

9. What role does `form_for` play in helping us create our forms?
* It's a helper method that allows us to create forms more easily and abstract some of the html and http protocols away from the form.

10. How does `form_for` know where to submit the user's input?
* From the helper paths and the origin of how the information is being sent to the form.

11. Create a form using a `form_for` helper to create a new `Horse`.
<%= form_for @horse do |f| %>
<%= f.label :name %>
<%= f.text_field :name %>
<%= f.label :breed %>
<%= f.text_field :breed %>
...etc...
<%= f.submit %>



12. Why do we want to validate our models?
* To make sure records in the database don't contain nil or anything that will cause an error.

13. What are the steps of the DNS lookup?
* First it looks in local cache, then at your router, then at the ISP router, and finally at the DNS servers.

### Review Questions
14. How would you call the method `prance` from within the method `move` on a `Horse` instance?
* horse = Horse.new
* horse.move.prance

15. Given the following hash:

```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```
What is the different between how you would return true vs returning 3?  
* furniture[:purchased] => true
* furniture[:table][:height] => 3

16. What is inheritance?
* inheritance is an idea in object oriented programming where an object can have access to methods and attributes defined in a superclass or parent class.

### Self Assessment:
Choose One:

* I was able to answer most questions independently, but utilized outside resources for a few
## More so that I think i just wasn't sure what some questions were asking. (specifically number 14 (I've definitely never come across that - definitely not review), and question 7.)


Choose One:

* I feel comfortable with the content presented this week
 ## Except for CSS/Static Challenges
