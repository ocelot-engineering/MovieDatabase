# Homework Assignment: Movie Database
In this assignment we will use a few classes to simulate the idea of a movie database. 

Note that while this assignment is doing things inefficiently, it gives you an idea of how objects interact with each other. 

For the purposes of this assignment, we will not worry about any kind of incorrect input. For example, if we incorrectly use the spelling “Meryl Streep” for one of the movies and “Meril Strep” in some other movie then we will have two entries in the database. In other words, we do not expect you to do any error checking.  

As with all the assignments, in order to pass our automated tests you have to have the same class names and method specifications (method signatures and return types) as the ones that we provide in this specification. 

First, we want you to make three classes (Make sure your classes are named exactly as shown here):

Actor

This class will have the following instance variables:
String name – the full name of the actor or actress.
ArrayList<Movie> movies – an Arraylist that has movies that this actor has acted in.
Add getters and setters for these instance variables.

Make sure to create a constructor that initializes your variables appropriately.

Movie
This class will have the following instance variables:
String name – the name of the movie
ArrayList<Actor> actors – an ArrayList of the actors in the movie. 
double rating – a freshness rating from rotten tomatoes (www.rottentomatoes.com)
Add getters and setters for these instance variables.

Make sure to create a constructor that initializes your variables appropriately.

 

MovieDatabase 
This class has two instance variables:
ArrayList<Movie> movieList – an ArrayList of movies
ArrayList<Actor> actorList – an ArrayList of actors

Note: Make sure to add getters for both these instance variables. That is, add a getMovieList() and a getActorList() method.

Add the following methods to this class:

MovieDatabase()
a constructor that just creates a new movieList and a new actorList. At the time of construction, both of these lists will be empty.

void addMovie(String name, String[] actors)

This method takes in the name of a movie that is not currently in the database along with a list of actors for that movie. 

If the movie is already in the database, your code ignores this request (this specification is an oversimplification). 

If the movie is a new movie, a movie object is created and added to the movieList. 

If any of the actors happen to be new, they will be added to the actorList.

void addRating(String name, double rating)

Add a rating for this movie. Assume that the name argument will definitely be a name that is currently in the database.

void updateRating(String name, double newRating)

Overwrite the current rating of a movie with this new rating. Again, assume that the name argument will definitely be a name that is currently in the database.

String getBestActor()

Returns the name of the actor that has the best average rating for their movies.

 

In the case of a tie, return any one of the best actors.

String getBestMovie()
Returns the name of the movie with the highest rating.

In the case of a tie, return any one of the best movies.

Main method
Finally, write a main method where:

You create a new instance of a movieDatabase.

Add all the movies in the file movies.txt.

Go through the ratings of the movies in the file ratings.txt and add the ratings for the movies.

Now call the methods that you created and print out the name of the best actor and the name of the highest rated movie.

movies.txt

ratings.txt

Note that both these files are contain data that you are free to modify. The full dataset we provide you with is deliberately "real-world"-like. It may be useful to start with a smaller version of these files by copying and pasting a few lines of the .txt files into a new file. Alternatively, you could stick to our file format (comma-separated) and create your own data from scratch.
