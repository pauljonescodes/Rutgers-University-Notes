Principles of Information and Data Management <small>with Tomasz Imielinski</small>
===================================================================================

Description
-----------

Describing and querying various forms of information such as structured
data in relational databases, unstructured text (IR), semi-structured
data (XML, web), deductive knowledge. Conceptual modeling and schema
design. Basics of database management system services (transactions,
reliability, security, optimization). Advanced topics: finding patterns
in data, information mapping and integration. The course focuses on a
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
    -   will be prepared to contribute to a rapidly changing field by
            acquiring a thorough grounding in the core principles and
            foundations of computer science (e.g., techniques of program
            design, creation, and testing; key aspects of computer hardware;
            algorithmic principles).

    -   will acquire a deeper understanding on (elective) topics of more
            specialized interest, and be able to critically review, assess,
            and communicate current developments in the field.

    -   will be prepared for the next step in their careers, for
            example, by having done a research project (for those headed to
            graduate school), a programming project (for those going into
            the software industry), or some sort of business plan (for those
            going into startups).

September 4th, 2013 <small>Reading, SQL, pages 243-273</small>
--------------------------------------------------------------

-   SQL stands for "structured query language."

### Simple Queries in SQL

-   The simplest form of query in SQL asks for those tuples of some one
        relation that satisfy a condition.

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
    1.  The `SELECT` clause tells which attributes of the tuples
            matching the condition are produced as part of the answer.

        -   The `*` in our case gets all the tuples.

    2.  The `FROM` clause gives the relation or relations to which the
            query refers.

        -   Getting "Movies" means you get all the movies …

    3.  The `WHERE` clause is a condition, much like a
            selection-condition in rela­tional algebra.

        -   This uses predicate logic.

-   A trick for reading and writing queries, read them in the following
        order:

    1.  the `FROM` clause, to learn which relations are involved;
    2.  the `WHERE` clause, to learn what about the tuples is important
    3.  the `SELECT` clause to see what the output is

#### Projection in SQL

-   If you only wanted to see qualities about the movie in the example
        above instead of all of the information, that would be in the
        `SELECT` clause, you could change it to just `title, length`, for
        instance.

-   If you want to change the title header for a column, you can do so
        with the `AS` keyword,

        SELECT title AS name

-   If you want to change the value of all the elements in a column, you
        can add expressions to `SELECT`s:

        SELECT length*0.016667 AS lengthlnHours

-   SQL is case-insensitive.

#### Selection in SQL

-   Six comparison operators:

        =, <>, <, >, <=, and >=

    -   `<>` is the SQL symbol for “not equal to”

-   The concatenation operator in SQL is `||`:

        ’foo’ || ’bar’ = ’foobar’

#### Comparison of Strings

-   When you compare strings with the operators, you are asking about
        lexicographic values.

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
-   You can combine the two with timestamps:
        `TIMESTAMP '1948-05-14 12:00:00'`

#### Null Values and Comparisons Involving `NULL`

-   There are three reasons that SQL will return a `NULL`:
    1.  **Value unknown**: that is, “I know there is some value that
            belongs here but I don’t know what it is.”

        -   There's an answer *in principle* but this database doesn't
                have one *in practice*.

    2.  **Value inapplicable**: “There is no value that makes sense
            here.”

        -   It's possible to have an answer, it just happens that there
                isn't here.

    3.  **Value withheld**: “We are not entitled to know the value that
            belongs here.”

-   If you operate on `NULL`, the return value will always be `NULL`.
-   If you compare on `NULL`, the return value will always be `UNKNOWN`.
    -   This is a SQL truth value.

-   Interestingly enough, if you place `NULL` in a variable name, you
        can get these legal comparisons and operations. However, if you do
        the operation on `NULL` directly, it is not valid SQL.

#### The Truth-Value `UNKNOWN`

> 1.  The `AND` of two truth-values is the minimum of those values. That
>         is, x `AND` y is `FALSE` if either x or y is `FALSE`; it is
>         `UNKNOWN` if neither is `FALSE` but at least one is `UNKNOWN`, and
>         it is `TRUE` only when both x and y are `TRUE`.
>
> 2.  The `OR` of two truth-values is the maximum of those values. That
>         is, x `OR` y is `TRUE` if either x or y is `TRUE`; it is `UNKNOWN`
>         if neither is `TRUE` but at least one is `UNKNOWN`, and it is
>         `FALSE` only when both are `FALSE`.
>
> 3.  The negation of truth-value v is 1 —v. That is, `NOT` x has the
>         value `TRUE` when x is `FALSE`, the value `FALSE` when x is
>         `TRUE`, and the value `UNKNOWN` when x has value `UNKNOWN`.
>
> #### Ordering the Output

-   You can add a fourth clause the the `SELECT-FROM-WHERE` semantic to
        order the output.

    -   Aptly named, `ORDER BY` and it accepts a list of attributes.
    -   The default is ascending, and you can make it descending by
            adding the keyword `DESC`.

-   To order movies by length and then alphabetically from the running
        example, you'd use this clause:

        ORDER BY length, title;

### Queries Involving More Than One Relation

-   The set-theoretic operations — union, intersection, and difference —
        appear directly in SQL.

-   It seems as though the names of table headers must be unique, as if
        you wanted any information from multiple columns, you can do this:

        WHERE title = ’Star Wars’ AND producerC# = cert#;

    -   This returns the producers of Star Wars, whatever you select
            from it.

#### Disambiguating Attributes

-   Ah! No, you do not have to have them unique across tables, and the
        book covers this next.

-   Imagine this:

        MovieStar(name,address, gender, birthdate) 
        MovieExec(name, address, cert#, netWorth)

    -   The way that you disambiguate them is with the following
            semantic:

            WHERE MovieStar.address = MovieExec.address;

    -   The relation name, followed by a dot, is permissible even in
            situations where there is no ambiguity.

#### Tuple Variables

-   You may want to select from the same table twice, and you can do
        this with aliases.

        FROM MovieStar Starl, MovieStar Star2

### Subqueries

September 5th, 2013 <small>Introduction to SQL</small>
------------------------------------------------------

### Why SQL?

-   SQL is a very-high-level language.
    -   Say “what to do” rather than “how to do it.”
    -   Avoid a lot of data-manipulation details needed in procedural
            languages like C++ or Java.

        -   In systems like MangoDB, you do a lot of data manipulation
                yourself.

        -   The name of the game now is scalabilty and millions and
                millions of users.

        -   SQL scales very well with ad-hoc, indeterminate number of
                queries.

    -   Why not? Database management systems figures out best way to
            executre queiry.

        -   Called **query manipulation**.

### Select-From-Where Statements

-   `SELECT` desired attributes.
-   `FROM` one or more tables.
-   `WHERE` condition about tuples of the tables.

### Our Running Examples

-   All our SQL queries will be based on the following database schema.

        Beers(name, manf) 
        Bars(name, addr, license)
        Drinkers(name, addr, phone) 
        Likes(drinker, beer) 
        Sells(bar, beer, price) 
        Frequents(drinker, bar)

-   From this you can find out who sells Heineken, you can find people
        who only frequent bars that sell beers they like.

    -   This is the "heart of the matter."

-   **Ad-hoc queries** are unpredictable, and this is where SQL shines.
    -   You can find any objects in the database, you don't have to
            write code. ... Very difficult, you write it, and a week later
            to think, "What the hell did I do?"

#### Example <small>What beers are made by Anheuser-Busch</small>

-   Query:

    SELECT name FROM Beers WHERE manf = ’Anheuser-Busch’;

-   Result:

    Bud Bud Lite Michelob ...

### Meaning of Single-Relation Query

-   Begin with the relation in the `FROM` clause.
-   Apply the selection indicated by the `WHERE` clause.
-   Apply the extended projection indicated by the `SELECT` clause.

### `NULL` Values in SQL

-   The logic of conditions in SQL is really 3-valued logic: `TRUE`,
        `FALSE`, `UNKNOWN`.

-   Comparing any value (including `NULL` itself) with `NULL` yields
        `UNKNOWN`.

-   A tuple is in a query answer if and only if the `WHERE` clause is
        `TRUE` (not `FALSE` or `UNKNOWN`).

September 17th, 2013 <small>Keywords for Quiz 1</small>
-------------------------------------------------------

-   `JOIN`: used to combine rows from two or more tables, based on a
        common field between them.

        SELECT Orders.OrderID, Customers.CustomerName, Orders.OrderDate 
        FROM Orders
        INNER JOIN Customers
        ON Orders.CustomerID=Customers.CustomerID;

-   `UNION`: combines the result of two or more SELECT statements.

        SELECT column_name(s) FROM table1
        UNION
        SELECT column_name(s) FROM table2;

-   `INTERSECT`: allows you to return the set theoretic intersection of
        the results of 2 or more "select" queries

        select field1, field2, . field_n
        from tables
        INTERSECT
        select field1, field2, . field_n
        from tables;

-   `MINUS`: returns all rows in the first SQL SELECT statement that are
        not returned in the second SQL SELECT statement

        select field1, field2, ... field_n
        from tables
        MINUS
        select field1, field2, ... field_n
        from tables;

-   `EXISTS`: this is a "to be met condition," where the select
        statement of the super query operates on the returned table.

        SELECT *
        FROM suppliers
        WHERE EXISTS (  select *
                        from orders
                        where suppliers.supplier_id = orders.supplier_id);

-   `NOT EXISTS`: the `NOT` operator can be combined with the `EXISTS`
        operator to operate on a subquery does not satisfy it's where
        condition.

-   `ALL`: used as a union that allows duplicates

        SELECT column_name(s) FROM table_name1
        UNION ALL
        SELECT column_name(s) FROM table_name2

-   `ORDER BY (DESC)`: When sorting your result set in descending order,
        you use the DESC attribute in your ORDER BY claus

        SELECT supplier_city
        FROM suppliers
        WHERE supplier_name = 'IBM'
        ORDER BY supplier_city DESC;

-   `COUNT`: returns the number of rows in a query

        SELECT COUNT(expression)
        FROM tables
        WHERE predicates;

September 24th, 2013 <small>Chapter 2, Relational Model</small>
---------------------------------------------------------------

### An Overview of Data Models

-   A **data model** is a notation for describing data. It has three
        parts:

    1.  *Structure of the data*.
    2.  *Operations on the data*.
    3.  *Constraints on the data*.

-   There are two preeminent database systems:
    1.  *The relation model*, include object-relational extensions.
    2.  *The semistructured-data model*, including XML and related
            standards.

        -   In brief, this is a way to represent data by hierarchically
                nested tags.

        -   Often talked about as a tree with parents and children
                nodes.

### Basics of the Relational Model

#### Attributes

-   The columns of a relation are named **attributes**.
    -   For example, `title`, `year`, `length`, and `genre` if the the
            relation was `Movies`.

#### Schemas

-   The name of a relation and the set of attributes for a relation is
        called the **schema** for that relation.

    -   In the case of movies,

            Movies(title, year, length, genre)

-   Attributes are a set, not a list.

#### Tuples

-   The rows of a relation, other than the header row, are called
        **tuples**.

    -   A tuple has one **component** for each attribute of the
            relation.

#### Domains

-   The relation model requires that each component of each tuple be
        atomic;

    -   It must be of some elementary type (integer, string, etc.)
    -   It is *not* permitted for it to be a record structure, set,
            list, array, or anything that can be broken into smaller
            elements.

-   It is further assumed that associated with each attribute of a
        relation is a **domain**, a particular elementary type.

        Movies(title:string, year:integer, length:integer, genre:string)

#### Keys of Relations

-   A set of attributes forms a **key** for a relation if we do not
        allow two tuples in a relation instance to have the same values in
        all attributes of the key.

### Defining a Relation Schema in SQL

-   SQL is the principal language used to describe and manipulate
        relational databases. There are two parts:

    1.  The *Data-Definition* sublanguage for declaring schemas;
    2.  The *Data-Manipulation* sublanguage for **querying** and
            modifying the database.

#### Relations in SQL

-   SQL makes a distinction between three kinds of relations:
    1.  Stored relations, called **tables**.
        -   These are the kind we deal with typically.
        -   Can be modified by changing it's tuples and queried.

    2.  **Views**, which are relations defined by a computation.
        -   These relations are not stored, but are constructed.

    3.  **Temporary tables**, which are constructed by the SQL language
            processor when it performs its job of executing queries and data
            modifications.

        -   These relations are not stored.

#### Data Types

1.  Character string of fixed or varying length.
2.  Bit string of fixed or varying length.
3.  The type `BOOLEAN`, `TRUE`, `FALSE`, and `UNKNOWN`.
4.  The type `INT` or `INTEGER`.
5.  Floating point numbers, `FLOAT` or `REAL`.
6.  Dates and times can be represented with the types `DATE` and `TIME`.

#### Simple Table Declarations

    CREATE TABLE Movies (
        title       CHAR(IOO), 
        year        INT, 
        length      INT,
        genre       CHAR(10), 
        studioName      CHAR(30), 
        producerC#      INT
    );

### An Algebraic Query Language <small>Set Operations on Relations</small>

-   There are four broad classes of operations:
    1.  The usual set operations;
        1.  The **union** of R and S, is the set of elements that are in
                R or S or both. Elements appear only once despite being in
                multiple times;

            *R* ∪ *S*

        2.  The **intersection** of R and S, is the set of elements that
                are in both R and S;

            *R* ∩ *S*

        3.  The **difference** of R and S, is the set of elements that
                are in R but not in S.

            *R* − *S*

    2.  Operations that remove parts of a relations;
        1.  **Selection**, produces a new relation with a subset of R's
                tuples, filter tuples, where *C* is a condition:

            *σ*<sub>*C*</sub>*R*

        2.  **Projection** is used to produce from a relation R a new
                relation that has only some of R's columns, filter
                attributes:

            *π*<sub>*A*<sub>1</sub>, *A*<sub>2</sub>, …, *A*<sub>*n*</sub></sub>*R*

    3.  Operations that remove parts of the relation;
        1.  **Cartesian product**, combines relations in all possible
                ways,

        2.  **Joins**, selectively pair tuples from two relations,

    4.  **Renaming**, which changes the attributes and/or name of
            relation.

-   These are **queries**.

-   We want to use these operations for queries, but there are these
        constraints:

    -   R and S must have schemas with identical sets of attributes.
    -   Before we compute the set-theoretic union, intersection, or
            difference of sets of tuples, the columns of R and S must be
            ordered so that the order of attributes is the same for both
            relations.

September 24th, 2013 <small>Project 1</small>
---------------------------------------------

Your objective will be to extend significantly the famous db scheme with
new attributes and new relations. It has to be realistic and
interesting. Add info about facebook friends of drinkers? Offer
information about bar’s annual sales? Provide more geo-location data
about drinkers and bars? Temporal data? Sky is the limit –). Once you
settle of the db scheme, you will have to populate it with realistic
tuples. By realistic, I mean names of bars, drinker names, dollar
figures etc when appropriate. No a1, b1, c1! No drinker X and drinker Y!
Generate and load your db with the large number of synthetic tuples, may
be 10,000? May be more. It is your choice. But your instances should not
be completely random. On the contrary – you should think of a few
patterns which will have business significance. For example, the larger
the bar, the less it charges for a beer (most of the time). The older
the drinker, the less frequently s/he goes to a bar. Evening beer sales
are higher than afternoon beer sales. Embed a number of such patterns in
your data and construct SQL queries which would prove that indeed your
db satisfies such pattern. Your patterns should be intuitive and have
actionable business value either for a bar o for a drinker.

Thus, there following tasks:

1.  Scheme definition
2.  Realistic db instance generation and db loading + Pattern embedding
        in the instance as well as validation of the pattern using sql query

3.  Simple DB GUI with search boxes which will find something
        interesting about your data.

October 1st, 2013 <small>Reading: pg. 125-171</small>
-----------------------------------------------------

### The Entity/Relationship Model

-   In the **E/R model**, the structure of data is represented
        graphically, as an "ER diagram", using three principal element
        types:

    1.  Entity sets,
    2.  Attributes, and
    3.  Relationships.

#### Entity Sets

-   An **entity** is an abstract object of some sort, a collection of
        similar entities is an **entity set**.

    -   An entity in some ways represents an "object" in the sense of
            OO-programming.

    -   Likewise, an entity set resembles a class of objects.

-   In the movie example, each movie is an entity, and the set of all
        movies constitute an entity set.

#### Attributes

-   Entity sets have associated **attributes**, which are properties of
        the entities in that set.

    -   The entity set *Movies* might be given attributes such as
            *title* and *length*.

#### Relationships

-   **Relationships** are connections among two or more entity sets.
    -   For instance, if *Movies* and *Stars* are two entity sets, we
            could have relationship *Stars-in* that connects movies and
            stars.

#### Entity-Relationship Diagrams

-   Entity sets are represented by rectangles.
-   Attributes are represented by ovals.
-   Relationships are represented by diamonds.
    -   "Is-a relationships" are special and represented with triangles.

-   Edges connect an entity set to its attributes and also connect a
        relationship to its entity set.

#### Multiplicity of Binary E/R Relationships

-   If each member of *E* can be connected by *R* to at most member of
        *F*, then we say that *R* is a **many-one** from *E* to *F*.

    -   Note that in a many-one relationship from *E* to *F*, each
            entity in *F* can be connected to many members of *E*.

-   If *R* is both many-one from *E* to *F* and many-one from *F* to
        *E*, then we say that *R* is **one-one**.

    -   In a one-one relationship an entity of either entity set can be
            connected to at most one entity of the other set.

-   If *R* is neither many-one from *E* to *F* or from *F* to *E*, then
        we say *R* is **many-many**.

#### Multiway Relationships

-   The E/R model makes it convenient to define relationships involving
        more than two entity sets. In practice, ternary or higher degree
        relationships are rare, but occasionally are necessary to represent
        the true state of affairs.

    -   They are represented with lines between all involved entity
            sets.

-   An arrow pointing to an entity set *E* means that if we select one
        entity from each of the other entity sets in the relationships,
        those entities are related to at most entity in *E*.

#### Roles in Relationships

-   It is possible that one entity sets appears two or more times in a
        single relationship.

    -   If so, we draw as many lines from the relationship to the entity
            sets as the entity set appears in the relationship.

    -   Each line to the entity set represents a different role that the
            entity set plays in that relationship.

### Design Principles

#### Faithfulness

-   First and foremost, the design should be faithful to the specs.
    -   The entity sets should reflect reality.

#### Avoid Redundancy

-   We should be careful to say everything once only.
-   This is dangerous because:
    1.  Doing so leads to repetition of fact, with the result that the
            extra space is required to represent the data.

    2.  There is an update-anomoly potential, since we might change the
            relationship but not the attribute.

#### Simplicity Counts

-   Avoid introducing more elements into your design than is absolutely
        necessary.

#### Choosing the Right Relationships

-   Entity sets can be connected in various ways by relationships.
    -   However, adding

### Constraints in the E/R model

#### Keys in the E/R Model

-   A **key** for an entity set *E* is a set *K* of one or attributes
        such that, given any two distinct entities *e1* and *e2*, *e1* and
        *e2* cannot have identical values for each of the attributes in the
        key *K*.

    -   Every entity set must have a key, although in some cases,
            isa-hierarchies and "weak" entity sets, the key actually belongs
            to another entity set.

    -   There can be more than one possible key for an entity set.
            However, it is customary to pick one key as the "primary key,"
            and to act as if that were the only key.

    -   When an entity set is involved in an isa-hierarchy, we require
            that the root entity set have all the attributes needed for a
            key, and that the key for each endtity is found from its
            component in the root entity set, regardless of how many entity
            sets in the hierarchy have components for the entity.

#### Representing Keys in the E/R Model

-   In our E/R-diagram notation, we underline the attributes belonging
        to a key for an entity set.

#### Referential Integrity

-   The arrow notation in E/R diagrams is able to indicate whether a
        relationship is expected to support referential integrity in one or
        more directions.

    -   Suppose *R* is a relationship from entity set *E* to entity set
            *F*. A rounded arrow-head poring to *F* indicates not only that
            the relationship is many-one from *E* to *F*, but that the
            entity of set *F* related to a given entity of set *E* is
            required to exist.

        -   The same idea applies when *R* is a relationship among more
                than two entity sets.

#### Degree Constraints

-   In the E/R-model, we can attach a bounding number to the edges that
        connect a relationship to en entity set, indicating limits on the
        number of entities that can be connected to any one entity of the
        related entity set.

### Weak Entity Sets

-   It is possible for an entity set's key to be composed of attributes,
        some or all of which belong to another entity set.

    -   Such an entity set is called **weak entity set**.

#### Causes of Weak Entity Sets

-   There are two principle reasons we need weak entity sets.
    1.  Sometimes entity sets fall into a hierarchy based on
            classifications unrelated to "is-a hierarchy."

    2.  Connecting entity sets that as a way to eliminate a multiway
            relationship.

#### Requirements for Weak Entity Sets

-   If *E* is a weak entity set then its key consists of:
    1.  Zero or more of its own attributes.
    2.  Key attributes from entity sets that are reach by certain
            many-one relationships from *E* to other entity sets.

        -   These many-one relationsips are called \*\*supporting
                relationships\*\* for *E*, and the entity sets reach from
                *E* are **supporting entity sets**.

-   In order for *R*, a many-one relationship from *E* to some entity
        set *F*, to be a supporting relationship for *E*, the following
        conditions must be obeyed:

    1.  *R* must be binary, many-one relationship from *E* to *F*.
    2.  *R* must have referential integrity from *E* to *F*.
        -   For every *E*-entity, there must be exactly one existing
                *F*-entity related to it by *R*.

        -   Put another way, a rounded arrow from *R* to *F* must be
                justified.

    3.  The attributes that *F* supplies for the key of *E* must be key
            attributes of *F*.

    4.  However, if *F* is itself weak, then some or all of the key
            attributes of one or more entity sets *G* to which *F* is
            connected by a supporting relationship.

        -   Recursively, if *F* is weak, some key attributes of *F* will
                be supplied from elsewhere, and so on.

#### Weak Entity Set Notation

-   We shall adopt the following conventions to indicate that an entity
        set is weak and to declare its key attributes:

    1.  If an entity set is weak, it will be shown as a rectangle weit a
            double border.

    2.  Its supporting many-one relationships will be shown as diamonds
            with a double border.

    3.  If an entity set supplies any attributes for its own key, the
            those attributes will be underlines.

### From E/R Diagrams to Relational Designs

-   To a first approximations, converting an E/R design to a relational
        database schema is straightforward.

    -   Turn each entity set into a relation with the same set of
            attributes.

    -   Replace a relationship by a relation whose attributes are the
            keys for the connected entity sets.

-   While these etwo rules cover much of the ground, there are apse
        special situations that we need to deal with, including:

    1.  Weak entity sets cannot be translated straightforwardly to
            relations.

    2.  "Isa" relationship and subclasses require careful treatment.
    3.  Sometimes, we do well to combine two relations, especially the
            relation for an entity set *E* and the relation that comes from
            *E* to some other entity set.

### Summary

-   **The Entity-Relationship Model**: In the E/R model we describe
        entity sets, relationships among entity sets, and attributes of
        entity sets and relationships. Members of entity sets are called
        entities.

-   **Entity-Relationship Diagrams**: We use rectangles, diamonds, and
        ovals to draw entity sets, relationships, and attributes,
        respectively.

-   **Multiplicity of Relationships**: Binary relationships can be one-
        one, many-one, or many-many.

    -   In an one-one relationship, an entity of either set can be
            associated with at most one entity in the other set.

    -   In a many-one relationship, each entity in the "many" side is
            associated with at most one entity on the other side.

    -   In a many-many relationship, there is no restriction.

-   **Good design**: Designing databased effectively requires that we
        represent the real world faithfully, that we select appropriate
        elements, and that we avoid redundancy.

October 1st, 2013 <small>6.4 Full-Relation Operations</small>
-------------------------------------------------------------

### Eliminating Duplicates

-   SQL's notion of relations differs from the abstract notion.
    -   A relation, being a set, cannot have more than one copy of a
            given tuple.

    -   When a SQL query creates a new relation, the SQL system does not
            ordinarily eliminate duplicates.

        -   This, the SQL response to a query may list the same tuple
                several times.

-   One of the several equivalent definitions of the meaning of a SQL
        select-from-where query is that we begin with the Cartesian product
        of the relations referred to in the `FROM` clause.

    -   Each tuple of the product is tested by the condition in the
            `WHERE` clause.

    -   The ones that pass the test are given to the output for
            projection according to the `SELECT` clause.

-   If we do not wish duplicates in the result, then we may follow the
        keyword `SELECT` by the keyword `DISTINCT`.

    -   This word tells SQL to produce only one copy of any tuple.

### Aggregation Operators

-   SQL uses five aggregative operators `SUM`, `AVG`, `MIN`, `MAX`, and
        `COUNT`.

    -   `SUM` adds up up the field it's given.
    -   `AVG` gets the average of the field given.
    -   `MIN` finds the smallest
    -   `COUNT` gets the number of fields

### Duplicates in Unions, Intersections, and Differences

-   Unlike the `SELECT` statement, which preserves duplicates as a
        default and only eliminates them when instructed to by the
        `DISTINCT` keyword, the union, intersection, and difference
        operations normally eliminate duplicates.

    -   If you *want* to include duplicates, you can do so by including
            the `ALL` keyword.

### Grouping

-   To group tuples, we use a `GROUP BY` clause following the `WHERE`
        clause.

### Grouping, Aggregating, and Nulls

-   The value NULL is ignored in any aggregation.
    -   It *does not* contribute to sum, average, or count of an
            attribute.

    -   Nor can it be the minimum or maximum of a column.

-   `NULL` is treated as an ordinary value when forming groups.
    -   That is, we can have a group in which one or more of the
            grouping attribute are assigned the value `NULL`.

-   When we perform any aggregation exception count over an empty bag,
        the result is `NULL`. The count of an empty bag is 0.

October 8th, 2013 <small>Study</small>
--------------------------------------

    bars (name, addr, license, phone)
    likes (drinker, beer)
    frequents (drinker, bar)
    sells (bar, beer, price)
    beer (manf, name)

### Questions 1

-   From Beers (name, manf), find those beers that are the only beer by
        their manufacturer.

        SELECT name
        FROM Beers b1
        WHERE _____ _____ ( -- NOT EXISTS
            SELECT *
            FROM ______ -- Beers
            WHERE manf = ______ -- b1.manf 
            AND ______    ______ b1.name -- name <>
        );

-   Find the drinkers and beers such that: The drinker likes the beer,
        and the drinker frequents at least one bar that sells the beer.

        (SELECT * FROM Likes)
        ________ -- intersect
        (SELECT ______,  _______ -- drinker, beer
        FROM Sells, Frequents
        WHERE _______ = _______); -- Frequents.bar == Sells.bar

-   From Sells (bar, beer, price) and Beers (name,manf), find the
        average price of those beers that are either served in at least
        three bars or are manufactured by Pete’s.

        SELECT beer, ______ -- AVG(Sells.price)
        FROM Sells
        GROUP BY beer
        ______ COUNT (bar) >= _____  -- WHERE, 3
            ______ beer _______ (SELECT name -- OR, IN
                                FROM Beers
                                WHERE manf = ______); -- "Pete's"

-   Find the average price for each beer that is sold by more than one
        bar in New Brunswick:

        SELECT beer, ______ -- AVG(price)
        FROM Sells
        WHERE address = ‘New Brunswick’
        _____   _____ beer -- GROUP BY
        HAVING _____ > 1 -- COUNT(bar)

-   Drinkers who live together frequent same bar(0/1).

        SELECT IF (COUNT (*)>0, 1, 0)
        FROM (SELECT ______, d1.addr 
                FROM drinkers d1, drinkers d2
                WHERE d1.name_____     _____ -- <> d2.name
                    AND ____=_____) d, frequents -- d1.addr, d2.addr
        WHERE ______=frequents.drinker

### Questions 2

-   Find bars where either Tim or John drink.

        SELECT bars
        FROM frequents f1
        WHERE f1.drinker = 'Tim'
        UNION
        SELECT bars
        FROM frequents f2
        WHERE f2.drinker = 'John'

-   Which bar sells cheapest 'Bud' ?

        SELECT bar
        FROM Sells
        WHERE beer = "Bud" AND (
            SELECT MIN(price)
            FROM Sells
            WHERE beer = "Bud"
        )

-   For each bar that serve both 'heineken' and 'bud', count the number
        of drinkers that frequent that bar.

        SELECT bar, COUNT(DISTINCT f.drinker)
        FROM frequents f
        WHERE EXISTS (SELECT 
                FROM Sells s1, Sells s2
                WHERE s1.beer == "Heineken"
                    AND s2.beer == "Bud"
                    AND s1.bar == s2.bar
        )
        GROUP BY bar

-   Find the average price of common beers (where "common" means those
        that are served in more than two bars).

        SELECT beer, AVG(price)
        FROM Sells
        GROUP BY beer
        HAVING COUNT(Sells.bar) > 2

-   Bars having common drinkers must have common beers (false/true)

-   There is at least one beer which is sold at all bars. (true/false)

### Questions 3

-   Beer that has the maximum average price over the bars.

        SELECT s.beer 
        FROM sells s 
        __________ __________ __________ -- GROUP BY BEER
        HAVING AVG(price) __________  __________ ( -- >= ALL
            SELECT beer, __________ (price) AS av_p -- AVG
            FROM sells 
            __________ __________ __________) -- GROUP BY BEER

October 10th, 2013 <small>Lecture: Design Theory for Relational Databases</small>
---------------------------------------------------------------------------------

### Functional Dependency

-   `X -> Y` is an assertion about a relation *R* that whenever two
        types of *R* agree on all the attributes of *X*, then they must also
        agree on all attributes in set *Y*.

    -   Say "`X -> Y` holds in *R*."
    -   Convention: *X*, *Y*, and *Z* represent sets of attributes.

#### Splitting Right Sides of FDs

-   `X -> A_1, A)2, ... A_n` holds for *R* exactly when each of the
        expressions of for *R*.

#### Example

    Drinkers(name, addr, beersLiked, manf, favBeer)

-   Reasonable FDs to assert:
    1.  `name -> addr favBeer`
    2.  `beersLiked -> manf`

October 21st, 2013 <small>Quiz 4 Study</small>
----------------------------------------------

### Relational Model

-   The **relational model** for database management is a database model
        based on first-order predicate logic.

    -   all data is represented in terms of **tuples**
    -   grouped into **relations**

-   A **table** in an SQL database schema corresponds to \*a predicate
        variable\*;

    -   the contents of a table to a **relation**;
    -   key constraints, other constraints, and SQL queries correspond
            to **predicates**

> What is the core limitation of relational model?

#### Application to Databases

-   A **data type** as used in a typical relational database might be
        the set of integers, the set of character strings, the set of dates,
        or the two boolean values true and false, and so on.

-   **Attribute** is the term used in the theory for what is commonly
        referred to as a **column**.

    -   Similarly, **table** is commonly used in place of the
            theoretical term **relation**.

-   A **tuple** is basically the same thing as a row

#### Keys

-   A **primary key** *uniquely specifies a tuple within a table*.

##### Method for finding keys

1.  If the letter is in the relation and not in the FDs, it must be a
        key.

2.  If the letter appears on the left but never on the right in the FDs,
        then it must be in the key.

3.  If the letter appears *on the right but never on the left*, then it
        **cannot** be in the key.

4.  If the letter is *on both sides*, you **cannot** not use this
        method.

#### Superkeys

-   A **superkey** is defined in the relational model of database
        organization *as a set of attributes of a relation variable for
        which it holds that in all relations assigned to that variable,
        there are no two distinct tuples (rows) that have the same values
        for the attributes in this set*.

#### Closure of a set of Attributes

### Normal Forms

> Why normal forms? Do they always work and when they do not work?

#### BCNF

-   A relational schema R is in **Boyce–Codd normal form** if and only
        if for every one of its dependencies X → Y, *at least one* of the
        following conditions hold:

    -   X → Y is a trivial functional dependency (Y ⊆ X)
    -   X is a **superkey** for schema R

##### Decomposition to BCNF

#### Third Normal Form

> synthesis of 3NF from the minimal base of given family of functional
> dependencies

-   Codd's definition states that a table is in **3NF** \*if and only if
        both of the following conditions hold\*:

    -   The relation R (table) is in second normal form (2NF)
    -   Every non-prime attribute of R is non-transitively dependent
            (i.e. directly dependent) on every superkey of R.

#### 1NF

-   A relation is in **first normal form** if \*the domain of each
        attribute contains only atomic values*, and *the value of each
        attribute contains only a single value from that domain\*.

### Functional Dependencies

-   A **functional dependency** is a constraint between two sets of
        attributes in a relation from a database.

-   Given a relation R, a set of attributes X in R is said to
        **functionally determine** another set of attributes Y, also in R,
        (written X → Y) if and only if each X value is associated with
        precisely one Y value; R is then said to satisfy the functional
        dependency X → Y.

October 26th, 2013 <small>Reading, pages 350-359</small>
--------------------------------------------------------

### Indexes in SQL

Index
:   An index on an attribute *A* of a relation is a data structure that
    makes it efficient to find those tuples that have a fixed value for
    attribute *A*.
:   We could think of the index as a binary search tree of (key, value)
    pairs, in which a key a (one of the values that attribute *A* may
    have) is associated with a "value" that is the set of locations of
    the tuples that have a in the component for attribute *A*.
:   A database index is a data structure that improves the speed of data
    retrieval operations on a database table at the cost of additional
    writes and the use of more storage space to maintain the extra copy
    of data. Indexes are used to quickly locate data without having to
    search every row in a database table every time a database table is
    accessed.

Index key
:   Note that the key for the index can be *any attribute* or \*set of
    attributes\*, and need not be the key for the relation on which the
    index is built.
:   We shall refer to the attributes of the index as the *index key*
    when a distinction needs to be made.

#### Motivation for Indexes

-   When relations are very large, it becomes expensive to scan all the
        tuples of a relation to find those (perhaps very few) tuples

-   Without indexes, we have to look at every tuple of the two
        relations.

#### Declaring Indexes

-   most commercial systems have a way for the database designer to say
        that the system should create an index on a certain attribute for a
        certain relation.

        CREATE INDEX YearIndex ON Movies(year);

### Selection of Indexes

-   Two important factors to consider are:
    -   The existence of an index on an attribute may speed up greatly
            the execution of those queries in which a value, or range of
            values, is specified for that attribute, and may speed up joins
            involving that attribute as well.

    -   On the other hand, every index built for one or more attributes
            of some relation makes insertions, deletions, and updates to
            that relation more complex and time-consuming.

#### Some Useful Indexes

-   Often, the most useful index we can put on a relation is an index on
        its key. There are two reasons:

    1.  Queries in which a value for the key is specified are common.
            Thus, an index on the key will get used frequently.

    2.  Since there is at most one typle with a given key value, the
            index returns either nothing or one location for a typle. Thus,
            at most one page must be retrieved to get that tuple into main
            memory.

#### Automatic Selection of Indexes to Create

1.  The first step is to establish the query workload. Since a DBMS
        normally logs all operations anyway, we may be able to examine the
        log and find a set of representative queries and database
        modifications for the database at hand. Or it is possible that we
        know, from the application programs that use the database, what the
        typical queries will be.

2.  The designer may be offered the opportunity to specify some
        constraints, e.g., indexes that must, or must not, be chosen.

3.  The tuning advisor generates a set of possible candidate indexes,
        and evaluates each one. Typical queries are given to the query
        optimizer of the DBMS. The query optimizer has the ability to
        estimate the running times of these queries under the assumption
        that one particular set of indexes is available.

4.  The index set resulting in the lowest cost for the given workload is
        suggested to the designer, or it is automatically created.

November 9th, 2013 <small>Study Guide to Quiz</small>
-----------------------------------------------------

### Data Access

#### I/Os

> Assume: Tables Sells, Likes and Drinker. Sells has 100,000 records,
> Likes has 1 million records and Drinker has also 100,000 records.
> Assume that each block of data (page) holds 100 records.

block
:   the smallest addressable unit on the hard disk.

-   Assume average seek time is 10ms. and average block transfer time is
        5ms.

-   Take the largest table, Likes.
-   Time to read Likes:

    > Transfer + Seek time = 10,000 blocks x 5ms = 50 seconds + 10ms

-   Time to find a specific record by sequentially scanning the file
        (does Joe like Sam Adams?) - on average half of all the blocks will
        have to be transferred and read, thus it is \> 5,000 blocks x 5ms =
        25 seconds + 10ms (seek time)

-   Now, lets assume that table Drinker has an index on the key
        attribute which is the Drinker’s name. Lets assume that index is
        organized as binary search tree and that drinkers table is ordered
        by drinker’s names. There is 1000 blocks and 1000 index entries. If
        there was miniscule amount of RAM – technically accessing each level
        in the binary search tree would generate a disk seek, for 1000
        entries, around 12!
         But realistically, the whole index would easily fit to RAM even 20
        years ago. So it would be 1 seek time and probably several blocks of
        data to transfer the index to RAM. Then perhaps 1 seek time + 1
        transfer for the block which may contain the record in drinker’s
        file. Thus, realistically we would need the total of few transfer
        times and 2 x seek time = milliseconds!

-   In the class slides – the options A3 and A4 (and A5 and A6) all
        account for the height of the index (number of index levels, hi).
        But we need to be realistic. With current large RAM sizes I do not
        believe one would have to access index one block at a time, that is
        assuming that only one block of an index fits to the main memory.
         This time is long gone. I am assuming that there is enough RAM to
        hold all index there. Thus, to access index only one seek time is
        needed (assuming index is located contiguously) and several block
        transfers to move to index from the disk to the main memory.

-   So there are really only two cases worth comparing: the primary and
        the secondary indexes. If index is primary all records with that
        index value are consecutive on the disk. If index is secondary they
        are not. This is particularly important for attributes which are not
        key attributes. Consider two hypothetical attributes of Drinker
        table: Zip Code and Gender. Lets assume there is 1000 drinkers per
        zip code. And lets assume that there is roughly the same number of
        male and female drinkers.

-   Lets start with index on zip code. Assume that zip code index is
        primary. In that case data on the disk is arranged by zip codes.
         There is ten blocks of “drinkers” per zip code. Thus we will need
        one seek for index to bring it from the disk and transfer several
        blocks of index (negligible) plus another seek time for the first
        block of zipcode 08901 and transfer time for ten blocks of data.
        Total: \> 2 x seek time = 20 ms \> 20 block transfers = 100 ms \>
        Total of 120 ms

-   Now assume that index on zip code is not primary (clustering).
        Drinkers in 08901 zip code may now be located on different blocks of
        the Drinker file. While Index transfer and seek time remains
        unchanged, we may now have to seek and transfer 1000 blocks from the
        hard disk since in the worst case each of the drinkers may be on
        different block. This time will dominate the overall performance
        since it will be \> 1000 x (10ms +5ms) = 15 seconds

-   Now, just imagine what would happen if we repeated the same
        reasoning for much less selective index on “Gender”! All in all, the
        overall performance of a simple select from one table query is
        determined by whether there is an index, how selective is an
        attribute and if index is primary (clustering) or secondary.
        Selectivity of an index and proximity of records on the disk are the
        main factors in determination of overall performance. As I said in
        class, using an index is not always a great idea. For example, if a
        query asks for all female drinkers and the index on gender is
        non-primary, one may need to access 50,000 drinkers and transfer
        blocks of data 50,000 times (assuming no caching of previously
        accessed blocks). This would be: \> 50,000 x 15ms = 750 seconds!

-   This is as opposed just to reading the file sequentially – roughly
        1000 x 10ms = 10 seconds (1000 blocks of data transferred and one
        additional seek)

#### Joins

-   This is where the real performance bottlenecks begin. One can easily
        choke the db system on joins. Even joining two tables may prove to
        be very expensive. But joins of more than two tables (even self
        joins) will quickly make your system unresponsive. Just to
        illustrate this points lets use calculations from the slides.

-   Suppose we make natural join of tables “sells” with “likes” on the
        beer attribute. For outer table always chose a smaller of the two
        tables – arguments of the natural join. Thus, our outer table will
        be the Sells table and our inner table will be Likes table.

-   In the worst case, if there is enough memory only to hold one block
        of each relation (OK, this is really not so realistic in this case!)
        the estimated cost is

$$nr ∗ bs + br$$

-   Which is $100,000 \times 10,000 + 1000$ block transfers = roughly
        one billon block transfers! That would be $5 x 10^6$ seconds! What
        is it, a few months or something?

-   And $100,000 + 1000$ seeks = $101,000$ seeks $= 1000 seconds$, very
        brisk comparing with the data transfer…..

-   Yes, true, very unrealistic, tuple at a time and practically no RAM.
        Below is a more realistic calculations with block nested loop join

-   Worst case estimate: $b_r \times b_s + b_r$ block transfers
        $+ 2 \times br  $seeks

-   Each block in the inner relation s is read once for each block in
        the outer relation (instead of once for each tuple in the outer
        relation

-   Best case: $b_r + b_s$ block transfers $+ 2$ seeks.
-   Now we have $1000 \times 10,000 + 1000 = 10$ million block transfers
        this is merely just $50,000$ seconds.\

-   Finally suppose we have an index on “beer” which is an attribute we
        join both tables on Now the cost is:

-   Cost of the join: $b_r (t_T + t_S) + n_r ∗ c$
-   Where c is the cost of traversing index and fetching all matching s
        tuples for one tuple or r

-   c can be estimated as cost of a single selection on s using the join
        condition

-   Thus, on our case, it is 1000 block transfers and seeks (since now
        we bring one block at a time) for sells and then for each record in
        sells we will use index on beer 100,000 times just to retrieve the
        matching tuples in Likes in order to compute the natural join. Lets
        first assume there is 1000 beers so each of them is liked by 100
        drinkers on average. If the index on beer is a primary one that
        would be just 1 block of drinkers. Overall that would translate to
        roughly only 100,000 I/Os (transfer + seek time), 500 seconds
        overall. But if the index on beer was non-primary, that would be 100
        blocks and 10 million I/Os…..not nearly as good.

### Transactions <small>Chapter 6, pg. 296-</small>

#### Conflict-Serializability <small>pg. 800</small>

#### Atomicity

#### Transactions

#### Read-Only Transactions

#### Dirty Reads

#### Other Isolation Levels

### Concurrency Control

Concurrency control
:   ensures that correct results for concurrent operations are
    generated, while getting those results as quickly as possible.

Transaction
:   A transaction comprises a unit of work performed within a database
    management system (or similar system) against a database, and
    treated in
    a coherent and reliable way independent of other transactions.
    Transactions in a database environment have two main purposes: To
    provide reliable units of work that allow correct recovery from
    failures
    and keep a database consistent even in cases of system failure, when
    execution stops (completely or partially) and many operations upon a
    database remain uncompleted, with unclear status. To provide
    isolation
    between programs accessing a database concurrently. If this
    isolation is
    not provided, the program's outcome are possibly erroneous.

### Blocks

### Seeks

### Transfers

### Indexes

Indexes
:   While not part of the SQL standard, commercial SQL systems allow the
    declaration of indexes on attributes; the indexes speed up certain
    queries that involve specification of value, or range of values, for
    the indexed attribute(s).

Choosing indexes
:   While indexes speed up queries, they slow down database
    modifications, since the indexes on the modified relation must also
    be modified. Thus, the choice of indexes is a complex problem,
    depending on the actual mix of queries and modifications perfumed on
    the database.

Automatic index selection
:   Some DBMS's offer tools to choose indexes for a database
    automatically. They examine the typical queries and modifications
    performed on the database and evaluate the cost trade-off for
    different indexes that might be created.

November 11th, 2013 <small>Gradiance reading</small>
----------------------------------------------------

Scheduler
:   The timing of individual steps of different transactions needs to be
    regulated in some manner. This is the job of a *scheduler* component
    of a DBMS.

        +-----------------+
        | Transaction     |
        | Manager         |
        +-----------------+
            | Read/write
            | requests
            v
        +-----------------+
        | Scheduler       |
        |                 |
        +-----------------+
            | Reads and
            | writes
            V
        +-----------------+
        |||||||||||||||||||
        |||||||||||||||||||
        +-----------------+

Concurrency control
:   The general process of assuring that transactions preserve
    consistency when executing simultaneously.

Serializability
:   Assuring that concurrently executing transactions preserve
    correctness of the database state.

Conflict-serializability
:   A stronger conditions that most schedulers actually enforce.

### Serial and Serializable Schedules

> **(Correctness Principle)**: Every transaction, if executed in
> isolation (without any other transactions running concurrently), will
> transform any consistent state to another consistent state.

#### Schedules

Schedule
:   A sequence of the important actions taken by one or more
    transactions.

$T_1$ $T_2$

* * * * *

`READ(A, t)` `READ(A, s)`
`t := t + 100` `s := s * 2`
`WRITE(A, t)` `WRITE(A, s)`
`READ(B, t)` `READ(B, s)`
`t := t + 100` `s := s * 2`
`WRITE(B, t)` `WRITE(B, s)`

#### Serial Schedules

Serial
:   A *schedule* is *serial* if its actions consist of all the actions
    of one transaction, then all the actions of another transaction, and
    so on. No mixing of actions is allowed.

    |$T_1$|$T_2$|$A$|$B$|
    |-----|-----|---|---|
    |||$25$|$25$|
    |`READ(A,t)`||||
    |`t := t + 100`||||
    |`WRITE(A,t)`|$125$|||
    |`READ(B,t)`||||
    |`t := t + 100`||||
    |`WRITE(B, t)`|||$125$|
    ||`READ(A, s)`|||
    ||`s := s * 2`|||
    ||`WRITE(A, s)`|$250$||
    ||`READ(B, s)`|||
    ||`s := s * 2`|||
    ||`WRITE(B, s)`||$250$|

    For the transaction here, there are two serial schedules.
    There in $T_1$ which precedes $T_2$, and the initial state
    is $A = B = 25$. We shall take the convention that when displayed
    vertically, time process down the page. Also the values of $A$ and
    $B$ shown refer to their valleys in main-memory buffers, not
    necessarily to their values on disk.

#### Serializable Schedules

The Correctness Principle for Transactions
:   Every serial schedule will preserve consistency of the database
    state.

Serializable
:   In general, we say that a schedule $S$ is *serializable* if there
    is a serial schedule $S\prime$ such that for every initial database
    state, the effects of $S$ and $S\prime$ are the same.

    |$T_1$|$T_2$|$A$|$B$|
    |-----|-----|---|---|
    |||$25$|$25$|
    |`READ(A,t)`||||
    |`t := t + 100`||||
    |`WRITE(A,t)`|$125$|||
    ||`READ(A,s)`|||
    ||`s := s * 2`|||
    ||`WRITE(A, s)`|$250$||
    |`READ(B, t)`||||
    |`t := t + 100`||||
    |`WRITE(B, t)`|||$125$|
    ||`READ(B, s)`|||
    ||`s := s * 2`|||
    ||`WRITE(B, s)`||$250$|

    This shows a schedule of the transactions of the first example that
    is seriablizable but not serial. In this schedule, $T_2$ acts on
    $A$ after $T_1$ does, but before $T_1$ acts on $B$. However, we see
    that
    the effect of the two transactions scheduled in this manner is the
    same as
    for the serial schedule.

    To convince ourselves of the truth of this statement, we must
    consider not
    only the effect from the database state $A = B = 25$, but from any
    consistent database state.

#### The Effect of Transaction Semantics

> Any database element $A$ that a transaction $T$ writes is given
> a value that depends on the database state in such a way that
> no arithmetic coincidences occur.

#### A Notation for Transactions and Schedules

-   If we assume "no conincidences," the only the reads and writes
    performed
        by the transactions matter, not the actual values involved. 

    -   Thus, we shall represent transactions and schedules by a
        shorthand
            notation, in which the actions are $r_T (X)$ and $w_T (X)$,

        -   Meaning that transactions $T$ reads, or respectively writes,
                database element $X$.

-   The first table can be written:

$$T_1 : r_1(A); w_1(A); r_1(B); w_1(B)$$
$$T_2 : r_2(A); w_2(A); r_2(B); w_2(B)$$

-   To make notation precise:
    1.  A *action* is an expression of the form $R_i(X)$ or $w_i(X)$,
            meaning that transaction $T_i$ reads or writes, respectively,
            the database element $X$.

    2.  A *transaction* $T_i$ is a sequence of actions with subscript
        $i$.
    3.  A *schedule* $S$ is a set of transactions $T$ is a sequences
            of actions, in which each transaction $T_i$ in $T$, the actions of
            $T_i$ appear in $S$ in the same order that they appear in the
            definition of $T_i$ itself. We say that $S$ is an *interleaving* 
            of the actions of the transactions of which it is composed.

November 5th <small>Transactions and Concurrency Control</small>
----------------------------------------------------------------

November 7th <small>Transactions and Concurrency Control</small>
----------------------------------------------------------------

November 12th <small>Quiz on Concurrency Control & Indexing + NoSQL intro lecture</small>
-----------------------------------------------------------------------------------------

November 14th <small>NoSQL class</small>
----------------------------------------

November 19 <small>Redemption Quiz</small>
------------------------------------------

November 21 <small>The "Interview"</small>
------------------------------------------

December 3rd <small>TBD (I may be away)</small>
-----------------------------------------------

December 5th <small>Class Projects Presentations</small>
--------------------------------------------------------

December 10th <small>Project Finalists and Crowning of the Winner</small>
-------------------------------------------------------------------------
