Principles of Information and Data Management <small>with Tomasz Imielinski</small>
===================================================================================

Description
-----------

Describing and querying various forms of information such as 
structured data in relational databases, unstructured text (IR), 
semi-structured data (XML, web), deductive knowledge. 
Conceptual modeling and schema design. Basics of database 
management system services (transactions, reliability, security, 
optimization). Advanced topics: finding patterns in data, 
information mapping and integration. The course focuses on a 
user's perspective, rather than how one implements DBMS.

-   Credits: 4

-   Prerequisites:
    -   01:198:112; 01:198:205 or 14:332:312.

Please note that courses for which a student has received a grade of D 
cannot be used to satisfy prerequisite requirements.

-   Semesters Offered:
    -   Spring, summer and fall

-   Expected Work:
    -   Homework and programming assignments; project

-   Exams:
    -   Midterm exam
    -   Final exam

### Department Learning Goals:

-   Computer Science majors ...
    -   will be prepared to contribute to a rapidly changing field by acquiring a 
        thorough grounding in the core principles and foundations of computer 
        science (e.g., techniques of program design, creation, and testing; 
        key aspects of computer hardware; algorithmic principles).
    -   will acquire a deeper understanding on (elective) topics of 
        more specialized interest, and be able to critically review, 
        assess, and communicate current developments in the field.
    -   will be prepared for the next step in their careers, for
        example, by having done a research project (for those headed 
        to graduate school), a programming project (for those going 
        into the software industry), or some sort of business plan 
        (for those going into startups).
        
September 4th, 2013 <small>Reading, SQL, pages 243-273</small>
--------------------------------------------------------------

-   SQL stands for "structured query language."

### Simple Queries in SQL

-   The simplest form of query in SQL asks for those tuples 
    of some one relation that satisfy a condition.
-   `SELECT`,`FROM`,and `WHERE` characterize SQL.
-   Here's an example scheme:

		Movies(title, year, length, genre, studioName, producerC#)
 		StarsIn(movieTitle, movieYear, starName) 
		MovieStar(name,address, gender, birthdate) 
		MovieExec(name,address, cert#, netWorth)
		Studio(name, address, presC#)

-   To get all movies by Disney, for instance, you'd query:

		SELECT *    // get all
		FROM Movies // the movies 
		WHERE studioName = ’Disney’ AND year = 1990; // from Disney in 1990 

-   Here's what each of the clauses do:
	1.  The `SELECT` clause tells which attributes of the tuples matching the condition are produced as part of the answer.
		-   The `*` in our case gets all the tuples.
	2.  The `FROM` clause gives the relation or relations to which the query refers.
		-   Getting "Movies" means you get all the movies … 
	3.  The `WHERE` clause is a condition, much like a selection-condition in rela­tional algebra.
		-   This uses predicate logic.

-   A trick for reading and writing queries, read them in the following order:
	1.  the `FROM` clause, to learn which relations are involved;
	2.  the `WHERE` clause, to learn what about the tuples is important
	3.  the `SELECT` clause to see what the output is

#### Projection in SQL

-   If you only wanted to see qualities about the movie in the example
	above instead of all of the information, that would be in the
	`SELECT` clause, you could change it to just `title, length`, 
	for instance.
-   If you want to change the title header for a column, you can do
	so with the `AS` keyword, 
		
		SELECT title AS name

-   If you want to change the value of all the elements in a column,
	you can add expressions to `SELECT`s:

		SELECT length*0.016667 AS lengthlnHours

-   SQL is case-insensitive.

#### Selection in SQL

-   Six comparison operators:

		=, <>, <, >, <=, and >=

	-   `<>` is the SQL symbol for “not equal to”

-   The concatenation operator in SQL is `||`:

		’foo’ || ’bar’ = ’foobar’

#### Comparison of Strings

-   When you compare strings with the operators, you are asking
	about lexicographic values.

#### Pattern Matching in SQL

-   To use patterns, you can add a `LIKE` statement to the `WHERE`
	clause. Example:

		WHERE title LIKE 'Star ____'

-   Returns Star Wars, Star Gate, Star Trek, ...

#### Dates and Times

-   SQL implementations are very specific about dates.
-   The format described here is the SQL standard.
-   `DATE '1948-05-14'` follows the required form.
-   There's also time, `TIME '15:00:02.5'` or `TIME '12:00:00-8:00'`
-   You can combine the two with timestamps: `TIMESTAMP '1948-05-14 12:00:00'`

#### Null Values and Comparisons Involving `NULL`

-   There are three reasons that SQL will return a `NULL`:
	1.  **Value unknown**: that is, “I know there is some value that 
		belongs here but I don’t know what it is.”
		-   There's an answer *in principle* but this database
			doesn't have one *in practice*.
	2.  **Value inapplicable**: “There is no value that makes sense
		here.”
		-   It's possible to have an answer, it just happens that
			there isn't here.
	3.  **Value withheld**: “We are not entitled to know the 
		value that belongs here.”

-   If you operate on `NULL`, the return value will always be `NULL`.
-   If you compare on `NULL`, the return value will always be `UNKNOWN`.
	-   This is a SQL truth value.

-   Interestingly enough, if you place `NULL` in a variable name,
	you can get these legal comparisons and operations. However,
	if you do the operation on `NULL` directly, it is not valid
	SQL.

#### The Truth-Value `UNKNOWN`

> 1. The `AND` of two truth-values is the minimum of those values. That is, x `AND` y is `FALSE` if either x or y is `FALSE`; it is `UNKNOWN` if neither is `FALSE` but at least one is `UNKNOWN`, and it is `TRUE` only when both x and y are `TRUE`.
> 2. The `OR` of two truth-values is the maximum of those values. That is, x `OR` y is `TRUE` if either x or y is `TRUE`; it is `UNKNOWN` if neither is `TRUE` but at least one is `UNKNOWN`, and it is `FALSE` only when both are `FALSE`.
> 3. The negation of truth-value v is 1 —v. That is, `NOT` x has the value `TRUE` when x is `FALSE`, the value `FALSE` when x is `TRUE`, and the value `UNKNOWN` when x has value `UNKNOWN`.

#### Ordering the Output

-   You can add a fourth clause the the `SELECT-FROM-WHERE` semantic
	to order the output.
	-   Aptly named, `ORDER BY` and it accepts a list of attributes.
	-   The default is ascending, and you can make it descending
		by adding the keyword `DESC`.

-   To order movies by length and then alphabetically from the
	running example, you'd use this clause:

		ORDER BY length, title;

### Queries Involving More Than One Relation

-   The set-theoretic operations — union, intersection, and difference — 
	appear directly in SQL.
-   It seems as though the names of table headers must be unique,
	as if you wanted any information from multiple columns, you
	can do this:

		WHERE title = ’Star Wars’ AND producerC# = cert#;
	
	-   This returns the producers of Star Wars, whatever you
		select from it.

#### Disambiguating Attributes

-   Ah! No, you do not have to have them unique across tables,
	and the book covers this next.
-   Imagine this:

		MovieStar(name,address, gender, birthdate) 
		MovieExec(name, address, cert#, netWorth)

	-   The way that you disambiguate them is with the following
		semantic:

			WHERE MovieStar.address = MovieExec.address;

	-   The relation name, followed by a dot, is permissible 
		even in situations where there is no ambiguity.

#### Tuple Variables

-   You may want to select from the same table twice,
	and you can do this with aliases.

		FROM MovieStar Starl, MovieStar Star2

### Subqueries
        
September 5th, 2013 <small>Introduction to SQL</small>
------------------------------------------------------

### Why SQL?

-   SQL is a very-high-level language.
    -   Say “what to do” rather than “how to do it.”
    -   Avoid a lot of data-manipulation details needed in 
        procedural languages like C++ or Java.
        -   In systems like MangoDB, you do a lot of data
            manipulation yourself.
        -   The name of the game now is scalabilty and millions
            and millions of users.
        -   SQL scales very well with ad-hoc, indeterminate number
            of queries.
    
    -   Why not? Database management systems figures out best
        way to executre queiry.
        -   Called **query manipulation**.
        
### Select-From-Where Statements

-   `SELECT` desired attributes.
-   `FROM` one or more tables.
-   `WHERE` condition about tuples of the tables.

### Our Running Examples

-   All our SQL queries will be based on the following
    database schema.
    
        Beers(name, manf) 
        Bars(name, addr, license)
        Drinkers(name, addr, phone) 
        Likes(drinker, beer) 
        Sells(bar, beer, price) 
        Frequents(drinker, bar)

-   From this you can find out who sells Heineken, you
    can find people who only frequent bars that sell beers
    they like.
    -   This is the "heart of the matter."
    
-   **Ad-hoc queries** are unpredictable, and this is where
    SQL shines.
    -   You can find any objects in the database, you don't have
        to write code. ... Very difficult, you write it, and a week
        later to think, "What the hell did I do?"
        
#### Example <small>What beers are made by Anheuser-Busch</small>

-   Query:

    SELECT name
    FROM Beers
    WHERE manf = ’Anheuser-Busch’;
    
-   Result:

    Bud
    Bud Lite 
    Michelob
    ...    

    
### Meaning of Single-Relation Query

-   Begin with the relation in the `FROM` clause.
-   Apply the selection indicated by the `WHERE` clause.
-   Apply the extended projection indicated by the `SELECT` clause.

### `NULL` Values in SQL

-   The logic of conditions in SQL is really 3-valued logic: `TRUE`, `FALSE`, `UNKNOWN`.
-   Comparing any value (including `NULL` itself) with `NULL` yields `UNKNOWN`.
-   A tuple is in a query answer if and only if the `WHERE` clause is `TRUE` (not `FALSE` or `UNKNOWN`).

September 17th, 2013 <small>Keywords for Quiz 1</small>
---------------------------------------------------------

* `JOIN`: used to combine rows from two or more tables, based on a common field between them.

	    SELECT Orders.OrderID, Customers.CustomerName, Orders.OrderDate 
		FROM Orders
		INNER JOIN Customers
		ON Orders.CustomerID=Customers.CustomerID;

* `UNION`: combines the result of two or more SELECT statements.

		SELECT column_name(s) FROM table1
		UNION
		SELECT column_name(s) FROM table2;

* `INTERSECT`: allows you to return the set theoretic intersection of the results of 2 or more "select" queries

		select field1, field2, . field_n
		from tables
		INTERSECT
		select field1, field2, . field_n
		from tables;

* `MINUS`: returns all rows in the first SQL SELECT statement that are not returned in the second SQL SELECT statement

		select field1, field2, ... field_n
		from tables
		MINUS
		select field1, field2, ... field_n
		from tables;

* `EXISTS`: this is a "to be met condition," where the select statement of the super query operates on the returned table.

		SELECT *
		FROM suppliers
		WHERE EXISTS (  select *
						from orders
						where suppliers.supplier_id = orders.supplier_id);

* `NOT EXISTS`: the `NOT` operator can be combined with the `EXISTS` operator to operate on a subquery does not satisfy it's where condition.
* `ALL`: used as a union that allows duplicates

		SELECT column_name(s) FROM table_name1
		UNION ALL
		SELECT column_name(s) FROM table_name2

* `ORDER BY (DESC)`: When sorting your result set in descending order, you use the DESC attribute in your ORDER BY claus

		SELECT supplier_city
		FROM suppliers
		WHERE supplier_name = 'IBM'
		ORDER BY supplier_city DESC;

* `COUNT`: returns the number of rows in a query

		SELECT COUNT(expression)
		FROM tables
		WHERE predicates;

September 23rd, 2013 <small>Homework 02A, Relational Model</small>
------------------------------------------------------------------

1.  Here is a table representing a relation named R:

        A	B	C
        0	1	2
        3	4	5
        6	7	8

-   Identify:
    -   The attributes of R.
    -   The schema of R.
    -   The tuples of R.
    -   The components of the tuples for each attribute of R.

-   Which of the following is NOT a true statement about relation R? 
    1. 	(A,B,C) is a tuple of R.
    2. 	(6,7,8) is a tuple of R.
    3.  (3,4,5) is a tuple of R.
    4.  B is an attribute of R.
 
2.  Suppose we are to design a registrar's database to store information about students, courses, the courses students have taken, and the grades students have gotten in these courses. Courses have a number, a department, and a title, for example, "CS101: Introduction to computing" has department = CS, number = 101, and title = "Introduction to Computing." Numbers are assigned by departments, and different departments may use the same number. Students are represented by their (unique) student ID and their name. "Enrollments" each consist of a course, a student who took that course, and the grade the student got in the course. If we created a relational schema for this database, which of the following would LEAST likely be an attribute of some relation?	  
    1.  studentID
    2.  grade
    3.  student
    4.  title

September 23rd, 2013 <small>Homework 02A, Classical Relational Algebra</small>
------------------------------------------------------------------------------

1.  	 Suppose relation R(A,B,C) has the tuples:
A	B	C
1	2	3
4	2	3
4	5	6
2	5	3
1	2	6
and relation S(A,B,C) has the tuples:

A	B	C
2	5	3
2	5	4
4	5	6
1	2	3
Compute (R - S) [union] (S - R), often called the "symmetric difference" of R and S. Then, identify from the list below, one of the tuples in the symmetric difference of R and S.

 
 		  a) 	 (2,5,3)	  		  b) 	 (2,5,4)	  		  c) 	 (1,5,6)	  		  d) 	 (1,2,3)
 
2.  	 Suppose relation R(A,B) has the tuples:
A	B
1	2
3	4
5	6
and the relation S(B,C,D) has tuples:

B	C	D
2	4	6
4	6	8
4	7	9
Compute the theta-join of R and S with the condition R.A < S.C AND R.B < S.D. Then, identify from the list below one of the tuples in R |><|R.A < S.C AND R.B < S.D S. You may assume the schema of the result is (A, R.B, S.B, C, D).

 
 		  a) 	 (5,6,2,4,6)
 		  b) 	 (3,4,5,7,9)
 		  c) 	 (5,6,4,6,9)
 		  d) 	 (3,4,2,4,6)
 
3.  	 Compute the union of the relation R(A,B,C):
A	B	C
1	2	3
4	2	3
4	5	6
2	5	3
1	2	6
and relation S(A,B,C):

A	B	C
2	5	3
2	5	4
4	5	6
1	2	3
Which of the following tuples DOES NOT appear in R [union] S?

 
 		  a) 	 (2,5,4)	  		  b) 	 (4,5,3)	  		  c) 	 (4,5,6)	  		  d) 	 (1,2,3)
 
4.  	 Suppose relation R(A,B) has the tuples:
A	B
1	2
3	4
5	6
and the relation S(B,C,D) has tuples:

B	C	D
2	4	6
4	6	8
4	7	9
Compute the natural join of R and S. Then, identify which of the following tuples is in the natural join R |><| S. You may assume each tuple has schema (A,B,C,D).

 
 		  a) 	 (3,4,6,8)
 		  b) 	 (1,4,7,9)
 		  c) 	 (3,4,2,6)
 		  d) 	 (5,6,4,6)
 
5.  	 Compute the intersection of the relations R(A,B,C):
A	B	C
1	2	3
4	2	3
4	5	6
2	5	3
1	2	6
and relation S(A,B,C:

A	B	C
2	5	3
2	5	4
4	5	6
1	2	3
Which of the following tuples appears in R ∩ S?

 
 		  a) 	 (2,4,3)	  		  b) 	 (2,5,3)	  		  c) 	 (2,5,4)	  		  d) 	 (1,2,4)
 
6.  	 Suppose relation R(A,B,C) has the tuples:
A	B	C
1	2	3
4	2	3
4	5	6
2	5	3
1	2	6
Compute the projection πC,B(R), and identify one of its tuples from the list below.

 
 		  a) 	 (3,2)	  		  b) 	 (2,3)	  		  c) 	 (5,6)	  		  d) 	 (4,2,3)