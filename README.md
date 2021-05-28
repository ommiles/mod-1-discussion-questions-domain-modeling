# Domain Modelling Discussion Questions

### Discuss these questions with your fellow table mates and try to model some solutions to the questions  


##### Using Netflix as your model, think about/try to model some solutions for the following questions:

![](https://curriculum-content.s3.amazonaws.com/module-1/discussion-questions/domain-modeling/Image_116_UsersAndMovies.png)

**1 . What would a Users table look like? What columns do you think would be in the table?**

Users has many profiles, has many movies.

Users and profiles have many movies.

Queue (joiner table) belongs to movies and belongs to profiles.

> User > - Queue - < Movies

USER TABLE: name

PROFILE TABLE: name, user_id,location

MOVIE TABLE: plot, title, rating, duration, actors, reviews

QUEUE TABLE: profile_id, movie_id

**2 . As a user you should be able to look at a list of movies and select any individual movies to add to your Queue. How would you model the relationship between a User and their Queue of Movies? What kind of properties would a Queue have? What kind of relationships would a Queue have with other tables? _Be sure to be very clear about on which table(s) the foreign keys are found. Be sure your domain allows the same Movie to appear on many different user's queues_**

Answer above.

**3 . A Movie has a plot, title, rating, duration, actors/actresses, and reviews. How would you model each of these relationships with a Movie? What would would you call the relationship between an Actor and a Movie?**

Actor and movie would each have their own table. Rating and reviews would be retrieved from the User tables, actors would be matched by id via a has many through relationship.

**4 . As a user you should be able to leave a Review on a Movie. Would a Review be a property of a User or its own table? Why? If a Reviewer does not have a direct relationship to a Movie, how can a Movie list the names of its Reviewers? What would you call this relationship?**



