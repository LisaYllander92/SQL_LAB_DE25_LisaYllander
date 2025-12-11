# SQL LAB explorating sakila database

## Films in sakila

### Movies longer than 3 hours:
```sql film_length
    SELECT title, length as length_in_minutes
    FROM film
    WHERE length > 180
    ORDER BY length DESC
```

### Movies with the word "LOVE" in title:
```sql film_title
    SELECT title, rating, length, description
    FROM film
    WHERE title ILIKE '% love %' 
    OR title ILIKE  'love %'
    OR title ILIKE '% love'
```

### Desctiptive statistics on movies length:
```sql film_statistics
SELECT
    MIN(length) AS Shortest_movie_length,
    ROUND(AVG(length)) AS Average_movie_length,
    MEDIAN(length) AS Median_movie_lenth,
    MAX(length) AS Longest_movie_length
    FROM film
```

### Top 10 most expensive movies to rent per day:
```sql rental_rate
SELECT title, 
    rental_rate,
    rental_duration,
    (rental_rate/rental_duration) AS rental_cost_per_day
    FROM film
    ORDER BY rental_cost_per_day DESC
    LIMIT 10
```

### Top 10 actors played in most movies:
```sql actors
SELECT actor,
COUNT(film_id) as number_films
FROM actors
GROUP BY actor
ORDER BY number_films DESC
LIMIT 10
```

### Top 5 most rented movie categorys:
```sql top_categorys
    SELECT
        category,
         ROUND(((CAST(COUNT(rental_id) AS DOUBLE) * 100.0) / (
             SELECT
                 COUNT(rental_id)
             FROM
                 rental)), 2) AS percentage_rental
    FROM categorys
    GROUP BY category
    ORDER BY percentage_rental DESC
```

