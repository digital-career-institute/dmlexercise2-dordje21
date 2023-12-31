# DML exercise

Tables:

Albums:

Columns: AlbumID (Primary Key), Title, ReleaseYear, Genre, Price, StockQuantity
Artists:

Columns: ArtistID (Primary Key), ArtistName, Country

Exercise Tasks:
note: add some data entries before fetching it
# Select Queries:

Retrieve all album titles along with their release years.
Display the genres available in the store without repetition.
List all artists' names along with their respective countries.
Fetch the album titles released in a specific year.

# Insert Queries:

Add a new album titled "Greatest Hits" released in the year 2023 to the database with a price of $15 and a stock quantity of 50.
Insert a new artist named "New Artist" from "Canada" into the Artists table.
Update Queries:

# Update
the price of all albums in the "Pop" genre to $20.
Increase the stock quantity of the album titled "Thriller" by 10 units.

# Delete Queries:
Remove an album titled "Dangerous" from the database.
Delete an artist named "Old Artist" from the Artists table.



-- Retrieve all album titles along with their release years.
SELECT Title, ReleaseYear FROM Albums;

-- Display the genres available in the store without repetition.
SELECT DISTINCT Genre FROM Albums;

-- List all artists' names along with their respective countries.
SELECT ArtistName, Country FROM Artists;

-- Fetch the album titles released in a specific year.
SELECT Title FROM Albums WHERE ReleaseYear = 2020;

-- Add a new album titled "Greatest Hits" released in the year 2023 to the database with a price of $15 and a stock quantity of 50.
INSERT INTO Albums (Title, ReleaseYear, Genre, Price, StockQuantity) VALUES ('Greatest Hits', 2023, 'Various', 15, 50);

-- Insert a new artist named "New Artist" from "Canada" into the Artists table.
INSERT INTO Artists (ArtistName, Country) VALUES ('New Artist', 'Canada');

-- Update the price of all albums in the "Pop" genre to $20.
UPDATE Albums SET Price = 20 WHERE Genre = 'Pop';

-- Increase the stock quantity of the album titled "Thriller" by 10 units.
UPDATE Albums SET StockQuantity = StockQuantity + 10 WHERE Title = 'Thriller';

-- Remove an album titled "Dangerous" from the database.
DELETE FROM Albums WHERE Title = 'Dangerous';

-- Delete an artist named "Old Artist" from the Artists table.
DELETE FROM Artists WHERE ArtistName = 'Old Artist';