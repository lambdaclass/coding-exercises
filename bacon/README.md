# Six degrees of Bacon

The [Bacon number](https://en.wikipedia.org/wiki/Six_Degrees_of_Kevin_Bacon#Bacon_numbers) of an actor is defined as the number of degrees of separation he or she has from Kevin Bacon.

It is computed following these rules:

- Kevin Bacon himself has a Bacon number of 0.
- Those actors who have worked directly with Kevin Bacon have a Bacon number of 1.
- If the lowest Bacon number of any actor with whom `X` has appeared in any movie is `N`, `X`'s Bacon number is `N+1`.


## Example

**Ian McKellen**:

1. Ian McKellen was in X-Men: Days of Future Past (2014) with Michael Fassbender and James McAvoy
2. McAvoy and Fassbender were in X-Men: First Class (2011) with Kevin Bacon
3. Therefore, McAvoy and Fassbender have Bacon numbers of 1, and McKellen has a Bacon number of 2

## Exercise

You will write a program that computes the Bacon number for a given starting actor to another.

Write a function `bacon_number` that takes a file name as input and outputs the Bacon numbers correctly.

The input file is formated as follows:

```
<starting_actor1>|<ending_actor1>
<starting_actor2>|<ending_actor2>
<starting_actor3>|<ending_actor3>
...
```

Your function will print out the correct Bacon numbers each on a newline.

```
3
5
6
...
```

You will use the data provided in `data/movie-actors.txt`. On each line, it will show a `movie_id` and an `actor_id` corresponding to an actor that played in that movie. The fields are separated by `|`.

```
1|2
1|3
1|5
1|4
2|10
2|7
2|8
2|9
3|12
...
```

You can find the data matching actor names to ids in `data/actors.txt.`.

```
2|Tim Allen
3|Tom Hanks
4|Don Rickles
5|Jim Varney
7|Jonathan Hyde
8|Bradley Pierce
9|Robin Williams
10|Kirsten Dunst
...
```
 
Similarly, though not needed for the exercise, the data matching `movie_id`'s to movie titles is in `data/movies.txt`.

```
1|Toy Story (1995)
2|Jumanji (1995)
3|Grumpier Old Men (1995)
4|Waiting to Exhale (1995)
5|Father of the Bride Part II (1995)
6|Heat (1995)
7|Sabrina (1995)
8|Tom and Huck (1995)
9|Sudden Death (1995)
...
```

The data and inspiration for this exercise taken from https://www.cs.dartmouth.edu/~cbk/10/hws.php?hw=PS-4.  
You can test your solution by checking if your values match the ones from http://oracleofbacon.org.
