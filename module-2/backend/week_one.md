## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 1 Questions

1. List the five common HTTP verbs and what the purpose is of each verb.

Post - Create
Get - Read
Put - Update/replace
Patch - Update
Delete - Delete/destroy

2. What is Sinatra?

Sinatra is a lightweight web framework that allows us to more easily use the Ruby language to handle http requests.

4. What is MVC?

MVC is an blueprint with regards to how one ought to go about using a framework and still implement single responsibility principles.  It is composed of three element Controller - manages traffic along paths, Model - performs the logic for specific repos and interacts with the database through activerecord. And lastly the views which provide a template to hold the information we want to pass to our clients.

5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?

To make things easily readable, maintainable, and improve performance.

6. What types of variables are accessible in our view templates without explicitly passing them?

Instance variables.

7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?

  ```ruby
  get '/horses' do
    @count = 1
    erb :index
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?

  @name = 'Mr. Ed'

9. What's the purpose of ERB?

Erb gives us a way to use the ruby programming language to display dynamic information to a webpage.

10. Why do I need a development AND test database?

To keep your tests from contaminating the development database.

11. What is CRUD and why is it important?

CRUD is the verbs listed in question 1.  It gives us a blueprint for what to consider building when it comes to how we want our web application to work.

12. What does HTTP stand for?

Hyper-text transfer protocol.

13. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
<%= %> simply prints ruby code from some other source.
<% %> Actually performs the logic in the view.

14. What's an ORM?

An ORM is an object relational module.  It allows us to pull a row from a database, turn that data into a ruby object where the column data is that object's attributes.

15. What's the most commonly used ORM in ruby (Sinatra & Rails)?

ActiveRecord

16. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
Get - index - view all.
Get - single - view one.
Get - create new form.
Post - send create new form.
Get - create edit one form.
Put/Patch - send edit form.
Delete/destroy - deletes one from database.

17. What's a migration?

A migration creaation is the auto-creation of a schema (database blueprint), or an update to the schema given new informtion/additional data/databases. A migrate itself implements the new table parameters for your database.

18. When you create a migration, does it automatically modify your database?

Possibly, it only changes the schema, and then the databsae layout - but does not change the data actually held in the database. Your tasks would be:
rake db:create, rake db:create_migration, rake db:migrate

19. How does a model relate to a database?

A model creates a ruby object that represents the data from a specific row of the database. The columns of the row are the attributes of the objects.

20. What is the difference between `#new` and `#create`?

New is the view of the form and create is when you actually submit the data, so they use two completely different.

### Review Questions:  
21. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?

CSV.foreach('films.csv', headers: true, header_converters: :symbol, converters: :numeric) do |row|
  Films.create(row.to_hash)
end

22. Given the following hash:
```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone'],
  brunch: {cost: $35, supplies: ['mimosa flutes'],
  antiquing: {cost: $200, supplies: ['list of antique stores']
}
```
How would I add 'granola bar' to things you should have when hiking?

activities[:hiking][:supplies] << "granola bar"

23. What are the 4 Principles of OOP? Give a one sentence explanation of each.
Encapsulation - keep certain data/method private.
Inheritance - idea of gaining attributes/methods from a superclass
Polymorphism - object can handle many things.
Abstraction - hide the details.



### Self Assessment:
Choose One:
* I was able to answer every question without relying on outside resources
This one, only maybe two with resources: * I was able to answer most questions independently, but utilized outside resources for a few
* I was able to answer a few questions independently, but relied heavily on outside resources

Choose One:
* I feel confident about the content presented this week
This one: * I feel comfortable with the content presented this week
* I feel overwhelmed by the content presented this week
* I feel quite lost by the content presented this week
