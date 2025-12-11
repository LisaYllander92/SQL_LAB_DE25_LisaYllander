# SQL LAB explorating sakila database

## Films in sakila

### Movies longer than 3 hours:
```films
    SELECT title, length as length_in_minutes
    FROM film
    WHERE length > 180
    ORDER BY length DESC
```

### 