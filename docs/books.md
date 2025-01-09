# Books DB 

## Authors 

The authors table records persons who have authored books. Every author corresponds to at least one book in the database.

| column | type | description |
| :--- | :---- | :---- | 
| author_id | integer | unique identifier for the author | 
| name | character string | full name of the author | 
| birth | date | birth date of the author, if known | 
| death | date | death date of the author, if known |

## Books 

The books table records works of fiction, non-fiction, poetry, etc. by a single author. Each book corresponds to a single author from the authors table, and may correspond to many editions of the book listed in the editions table.

| column | type | description | 
| :---| :---- | :---- | 
| book_id | integer | unique identifier for the book |
| author_id | integer | author_id of book’s author from authors table | 
| title | character string | the book’s title |
| publication_year | integer | year the book was first published | 

## Editions 

The editions table records specific publications of a book. Each edition corresponds to a single book from the books table. For space reasons, the editions table only includes data on four books by J.R.R. Tolkien.

| column | type | description | 
| :---- | :----- | :---- |
| edition_id | integer | unique identifier for the edition |
| book_id | integer | book_id of the book (from books table) published as this edition |
| publication_year | integer | year this edition was published |
| publisher | character string | name of the publisher | 
| publisher_location | character string | city or other location(s) where the publisher is located |
| title | character string | title this edition was published under | 
| pages | integer | number of pages in this edition |
| isbn10 | character string | 10-digit international standard book number |
| isbn13 | character string | 13-digit international standard book number | 

## Awards 

The awards table records various author and/or book awards.

| column | type | description | 
| :--- | :--- | :--- |
| award_id | integer | unique identifier for the award | 
| name | character string | name of the award | 
| sponsor | character string | name of the organization giving the award | 
| criteria | character string | what the award is given for |

## Authors Awards 

The authors_awards table is a cross-reference table (explained in Chapter 1.4) relating authors and awards; each entry in the table records the giving of an award to an author (not for any particular book) in a particular year.

| column | type | description | 
| :--- | :---- | :----- |
| author_id | integer | author_id of the author receiving the award |
| award_id | integer | award_id of the award received |
| year | integer | year the award was given |

## Book Awards 

The books_awards table is a cross-reference table relating books and awards; each entry in the table records the giving of an award to an author for a specific book in a particular year.

| column | type | description |
| :---- | :---- | :--- |
| book_id | integer | book_id of the book for which the award was given |
| award_id  | integer | award_id of the award given | 
| year | integer | year the award was given | 

# Bookstore Inventory DB

## Bookstore Inventory

The `bookstore_inventory` table contains information on new and used books for sale.

| column | type | description |
| :---- | :---- | :--- |
| stock_number | integer | unique key for a particular copy of a book | 
| author | string | author of book |
| title | string | title of book | 
| condition | string | condition (new, good, fair, etc. ) | 
| price | fixed-point | price in some unit of currency | 

## Bookstore Sales

The `bookstore_sales` table gives information about the sales of books from `bookstore_inventory`.

| column | type | description |
| :---- | :---- | :--- |
| receipt_number | integer | unique key for a sale | 
| stock_number | integer | key for sold book  | 
| date_sold | date | date of sale | 
| payment | string | method of payment (cash,credit, etc) | 


