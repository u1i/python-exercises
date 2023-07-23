## Movie Recommendation Engine

### Learnings

- Functions
- Data Structures
- User Input
- Algorithm Implementation

### Description

You are tasked with building a simple movie recommendation engine that suggests movies based on user preferences. The system will allow users to rate movies, and then recommend similar movies based on those ratings.

### Requirements

#### 1: Design the data structure

- Each movie should be represented as a dictionary.
- The dictionary should contain the following key-value pairs:

  - "title": The title of the movie (string).
  - "genre": The genre of the movie (string).
  - "rating": The average rating of the movie (float).
  - "similar_movies": A list of titles of movies similar to this movie (list of strings).

#### 2: Implement the following functionalities

a) Adding movie ratings:

- Implement a function `add_movie_rating(movies, movie_title, rating)` that takes a list of movies (a list of dictionaries), a movie title (string), and a rating (float) as input and adds the rating to the movie's data in the data structure.

b) Movie recommendation:

- Implement a function `get_movie_recommendations(movies, movie_title)` that takes a list of movies and a movie title (string) as input and returns a list of similar movie titles based on their ratings. The recommendation should include at least three movies with the highest average ratings from the list of similar movies.

c) View movie details:

- Implement a function `view_movie_details(movies, movie_title)` that takes a list of movies and a movie title (string) as input and displays the details of the specified movie, including its title, genre, and average rating.

d) List all movies:

- Implement a function `list_all_movies(movies)` that takes a list of movies as input and displays the titles of all movies available in the system.

e) User interface:

- Implement a function `user_interface()` that provides a user-friendly interface for users to interact with the movie recommendation system. The user interface should display clear instructions and prompt the user to rate movies, get movie recommendations, view movie details, list all movies, and exit the system. The user interface should repeatedly ask the user for input and call the appropriate functions based on their choices until the user decides to exit the system.

### Example

Suppose the movie data structure is as follows:

`movies = [
{
"title": "Movie A",
"genre": "Action",
"rating": 4.5,
"similar_movies": ["Movie B", "Movie C", "Movie D"]
},
{
"title": "Movie B",
"genre": "Drama",
"rating": 4.8,
"similar_movies": ["Movie A", "Movie C", "Movie E"]
},
]`


**User Flow Example 1 - Adding Movie Ratings**

1. User chooses to rate a movie.
2. The system prompts the user to enter the movie title and their rating for the movie.
3. User inputs:
   - Movie title: "Star Wars"
   - Rating: 3.5
4. The system adds the rating to the movie data.

**User Flow Example 2 - Movie Recommendation**

1. User chooses to get movie recommendations.
2. The system prompts the user to enter the movie title for which they want recommendations.
3. User inputs:
   - Movie title: "The Negotiator"
4. The system calculates and displays the recommended movies based on their ratings.

**User Flow Example 3 - Viewing Movie Details**

1. User chooses to view movie details.
2. The system prompts the user to enter the movie title they want to view.
3. User inputs:
   - Movie title: "Jurassic Park"
4. The system displays the details of "Jurassic Park" including its title, genre, and average rating.

**User Flow Example 4 - Listing All Movies**

1. User chooses to list all movies.
2. The system displays the titles of all available movies.

**User Flow Example 5 - Exiting the System**

1. User chooses to exit the system.
2. The system terminates the user interface and ends the program.

### Note

You can use a list of dictionaries to represent the movies, but feel free to use any other data structure that you think is appropriate for this exercise.
