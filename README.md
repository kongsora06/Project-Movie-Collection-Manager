# Project-Movie-Collection-Manager
📝 Files you’ll create:

Movie.java — A class to represent a single movie.
MovieCollection.java — A class to store and manage a collection of movies.
MovieCollectionManager.java — A class for reading from and writing to files.
📄 Movie.java

Fields:
title (String)
director (String)
rating (double) — IMDb-style rating out of 10
Constructors:
A constructor that takes all three fields as parameters.
Getters & Setters:
getTitle(), getDirector(), getRating()
setTitle(), setDirector(), setRating()
toString() method:
Returns the movie as a string like "Inception, Christopher Nolan, 8.8"
compareTo(Movie other, char sortBy) method:
't' sorts by title
'd' sorts by director
'r' sorts by rating (high to low)
equals(Movie other):
Movies are equal if the title and director match, and ratings are very close.
📚 MovieCollection.java

Fields:
Movie[] movies — An array of Movie objects
int nextEmpty — Tracks the next empty slot
Constructors:
Default constructor — Initializes the array to size 20.
Constructor that takes an int size and initializes the array to that size.
Methods:
public boolean add(Movie newMovie) — Adds a movie to the first empty spot; returns true if successful and false if full.
public MovieCollection getMoviesByDirector(String director) — Returns a new collection with only movies by the given director.
public void sort(char sortBy) — Sorts movies by title, director, or rating.
public String toString() — Lists all movies, one per line.
📂 MovieCollectionManager.java

public static MovieCollection readMoviesFromFile(String fileName) — Reads from a CSV and populates the collection.
public static void writeCollectionToFile(MovieCollection collection, String fileName) — Writes the collection to a file.
public static void main(String[] args):
Reads movies from "movies.csv".
Sorts by rating.
Writes sorted movies to "output.txt".
