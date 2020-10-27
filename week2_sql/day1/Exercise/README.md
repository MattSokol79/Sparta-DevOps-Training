# Exercise - Film Tables
Creates a film table with Borat as the example

```sql
SP_HELP films

CREATE TABLE films (
    film_name VARCHAR(168),
    film_type VARCHAR(15),
    date_released DATE,
    director VARCHAR(20),
    writer VARCHAR(20),
    star VARCHAR(20),
    film_language VARCHAR(20),
    website VARCHAR(max),
    plot_summary VARCHAR(max)
);

INSERT INTO films (
    film_name,
    film_type,
    date_released,
    director,
    writer,
    star,
    film_language,
    website,
    plot_summary
) 
VALUES (
    'Borat',
    'Comedy',
    '20061102',
    'Larry Charles',
    'Sacha Baron Cohen',
    '5',
    'English',
    'http://www.boratonline.co.uk/',
    'Outrageous situations occur when Borat, a popular reporter (Sacha Baron Cohen) from Kazakhstan, comes to the United States to film a documentary on what makes America a great nation. Along the way, he manages to offend just about everyone he meets, fall in love with actress Pamela Anderson, and set forth on a cross-country journey to make her his wife.'
);


--Change the star to a rating
UPDATE films
    SET star = '5'

ALTER TABLE films
    ALTER COLUMN star INT

SELECT * FROM films;
```
