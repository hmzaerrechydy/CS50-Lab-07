Link: https://cs50.harvard.edu/x/2023/labs/7/


Provided to you is a file called songs.db, a SQLite database that stores data from Spotify about songs and their artists. This dataset contains the top 100 streamed songs on Spotify in 2018. In a terminal window, run sqlite3 songs.db so that you can begin executing queries on the database.

First, when sqlite3 prompts you to provide a query, type .schema and press enter. This will output the CREATE TABLE statements that were used to generate each of the tables in the database. By examining those statements, you can identify the columns present in each table.

Notice that every artist has an id and a name. Notice, too, that every song has a name, an artist_id (corresponding to the id of the artist of the song), as well as values for the danceability, energy, key, loudness, speechiness (presence of spoken words in a track), valence, tempo, and duration of the song (measured in milliseconds).

The challenge ahead of you is to write SQL queries to answer a variety of different questions by selecting data from one or more of these tables.


#### 1.sql 

```sql
select name from songs;
```


#### 2.sql 

```sql
select name from songs order by tempo asc;
```


#### 3.sql 

```sql
select name from songs order by 'duration ms' desc limit 5;
```

#### 4.sql 

```sql
select * from songs where danceability > 0.75 and energy > 0.75 and valence > 0.75;
```


#### 5.sql

```sql
select avg(energy) from songs;
```


#### 6.sql 

```sql
select * from songs where artist_id = 54;
```


#### 7.sql

```sql
select avg(energy) from songs where artist_id = 23;
```


#### 8.sql 

```sql
select name from songs where name like '%feat%';
```
