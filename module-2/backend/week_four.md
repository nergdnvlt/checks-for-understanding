## Week Four Recap

### Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

1. What is a cookie?
* It is effectively a way of creating a 'state' on a webapp, usually taking the form of a session. The app will tell the client's browser to write and store session info.
2. What’s the difference between a session and a cookie?
* The cookie is the session ID info stored in the client's browser.  The session is the collection of information stored on the server that the cookie/session id gives access to.
3. What’s a flash and when do you want to use flashes?
* Flash is a temporary notification system (in our case it disappears when the page is refreshed).  It allows us to give certain information to the user depending on the situation - ie something is saved, not saved, deleted successfully etc.
4. Why do people say “HTTP is stateless”?
* Because it does not inherently contain anything to create a state.  We add sessions to track users and their preferences/choices but having a stateless http protocol allows for less information stored permanently in memory and in theory for a user to not have their session information stored permanently so that each time they visit the site, they interact with a new instance of it.
5. What’s authentication? Explain.
* Authentication is the systems of ensuring the user is who they say are.

6. What’s the difference between authentication and authorization?
* Authorization is only giving access to what a user needs access to and limiting the scope of their route resources.

7. What’s a before filter?
* It's a way of setting permissions/authorization to specific actions in the controllers.

8. How do we keep track of a user once they’ve logged in?
* Sessions

9. When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
* Namespacing just gives you a better way to nest controllers that may or may not have full models.  Nesting resources ties models together in a way that one has to belong to the other.

10. At a high level, what tools can you use to implement authorization? How would you use them?
* Using methods in the application controller that can check whether someone is an admin/user/visitor.

11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
* An enum is a way of setting certain values for a database table - ie say you want a role column you can set an enum so that the first value would be default and because its an array it would be stored in the table as a zero, and admin in the array would be stored as a one. Then those 0/default and 1/admin become synonymous.

12. What are some strategies you can use to keep your views DRY?
* Moving if/else and logic to the controllers.


### Reviews Questions
13. Given the following array of hashes, how would I print an alphabetical list of holidays?
```ruby
holidays = [
 {holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]},
 {holiday: {name: "Halloween", supplies: ["Candy", "Costume"]},
 {holiday: {name: "Hanukkah", supplies: ["Menorah"]}
]
```
* holidays.sort_by { |:holiday| [:name] }

14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300?


### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few


Choose One:
* I feel comfortable with the content presented this week
