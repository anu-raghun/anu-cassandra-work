# Successful build of ETL pipeline and database schema for Sparkify's Data Analytics team.

A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app.A proiorty for the team is understanding what song users are listening to. Currently, there is no easy way to query the data to generate the results, since the data reside in a directory of CSV files on user activity on the app.

I've created an Apache Cassandra database which can create queries to answer specific questions about song play and user activity. The database successfully outputs results for each of the queries.

## Querying
The tables below succesfully output results for the following queries:
<ol>
<li> Query 1: Give me the artist, song title and song's length in the music app history that was heard during  sessionId = 338, and itemInSession  = 4 </li>
<li> Query 2: Give me only the following: name of artist, song (sorted by itemInSession) and user (first and last name) for userid = 10, sessionid = 182 </li>
<li> Query 3: Give me every user name (first and last) in my music app history who listened to the song 'All Hands Against His Own' </li>
</ol>



## Tables

(Clustering columns in bold, composite primary key in italics):

<ol>

<li> artist_details </li>
    + artist_name, song_title, song_length, <em> session_id, item_in_session </em>
    
<li> user_song_library </li>
    + artist_name, song_title, first_name, last_name, <em> user_id, item_in_session, <b> session_id </b> </em>
    
<li> user_history </li>
    + first_name, last_name, <em> song_title </em>

</ol>
