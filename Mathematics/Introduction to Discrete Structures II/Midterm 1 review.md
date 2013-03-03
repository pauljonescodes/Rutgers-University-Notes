Introduction to Discrete Structures <small>Midterm 1 Review</small>
===================================================================

Axioms of Probability - Self Test Problems and Exercises
--------------------------------------------------------

1.  A cafeteria offers a three-course meal consisting of an entree, a
    starch, and a dessert. The possible choices are given in the
    following table:

        Course          Choices
        Entree          Chicken or roast beef
        Starch          Pasta or rice or potatoes
        Dessert         Ice cream or Jello or apple pie or a peach

    A person is to choose one course from each category.
    1.  How many outcomes are in the sample space?
        -   There are there points a person gets to choose something.
        -   At each of those points, there are 2, 3, and 4 choices.
        -   So I think it's $2! + 3! + 4!$, but I'm pretty bad at math.
        -   In hindsight, that's about putting things in order, and has
            nothing to do with this problems.
        -   It's simply: $2 \cdot 3 \cdot 4$

    2.  Let A be the event that ice cream is chosen. How many outcomes
        are in A?
        -   This only says something about the final decision.
        -   Therefore, the previous number still holds, with a
            restriction on the final choice.
        -   Therefore, $2 \cdot 3$

    3.  Let B be the event that chicken is chosen. How many outcomes are
        in B?
        -   Similar formula.
        -   $3 \cdot 4$

    4.  List all the outcomes in the event AB.
        1.  Chicken
        2.  (Pasta|Rice|Potatoes)
        3.  Ice cream
            -   More formally, {(chicken, x, ice cream) | x $\in$
                {pasta, rich, potatoes}

    5.  Let C be the event that rice is chosen. How many outcomes are in
        C?
        -   $2 \cdot 3$

    6.  List all the outcomes in the event ABC.
        -   {(Chicken, rice, ice cream)}

2.  A customer visiting the suit department of a certain store will:
    -   purchase a suit, $.22$
    -   purchase a shirt, \$ .30\$
    -   purchase a tie, $.28$
    -   both a suit and a shirt, \$ .11\$
    -   both a suit and a tie, $.14$
    -   both a shirt and a tie, $.10$
    -   all 3 items with probability \$ .06\$

    What is the probability that a customer purchases

    -   none of these items?
        -   I think it's too easy for them to just give us the .06 
            number and then have us calclate the complement.
            But that's my first guess, .94. (I know this is wrong.)
        -   We're interested in the union of purchasing a suit,
            purchasing a shirt, and purchasing a tie.
        -   The probability of buying all of these items is:
            $$P(A \cap B \cap C) = .22 + .30 + .28 + .11 + .14 + .10 + .06$$
        -   Subtract one from this to get the probability of buying none.
        -   I worry that I would not see this on a test.
    -   exactly 1 of these items?
        -   Add the probabilities that correspond *to* the sample space.
        -   Subtract the probabilities that *do not* correspond to this event.
            $$.22 + .30 + .28 - .11 - .14 - .10 - .06$$
        -   Of course, this is totally wrong.
        -   Right, so formally, where A is "purchase suit", B is "purchase shirt",
            and C is "purchse tie." We want:
            $$P(AB \cup AC \cup BC)$$

3.  A deck of cards is dealt out. What is the probability that the 14th
    card dealt is an ace? What is the probability that the first ace
    occurs on the 14th card?
    -   So there are four aces in a deck, meaning there are 48 that
        aren't.
    -   But every card is equally likely to be pulled at any time.
    -   This is called **symmetry**.

4.  Let A denote the event that the midtown temperature in Los Angeles
    is 70◦F, and let B denote the event that the midtown temperature in
    New York is 70◦F. Also, let C denote the event that the maximum of
    the midtown temperatures in New York and in Los Angeles is 70◦F. If
    P(A) = .3, P(B) = .4, and P(C) = .2, find the probability that the
    minimum of the two midtown temperatures is 70◦F.
    -   A is "the temp of LA is 70F", .3
    -   B is "the temp of NY is 70F", .4
    -   $P(A \cap B) = .3 + .4 - P(AB)$
    -   Call D "the minimum of the two is 70F"
    -   Observe that $A \cap B = D \cap C$, and therefore $AB = DC$.
    -   $P(D \cap C) = P(D) + .2 - P(DC)$
    -   $P(D) + .2 - P(DC) = .3 + .4 - P(AB)$
    -   $P(D) + .2 = .3 + .4$
    -   $P(D) = .3 + .4 - .2 = .5$

5.  An ordinary deck of 52 cards is shuffled. What is the probability
    that the top four cards have
    1.  different denominations?
        -   There are $52!$ total possibilities.
        -   I think that each of the four top cards can be counted as
            $13 \choose 1$.
        -   Wait no.
        -   You're picking four cards, ignore the rest of the deck.
        -   There are $52 \cdot 51 \cdot 50 \cdot 49$ total ways.
        -   Denomiation means 1 or 2 or 3 or ... or King or Ace.
        -   After each is picked, there are four less cards that are
            "available."
            $$\frac{52 \cdot 48 \cdot 44 \cdot 40}{52 \cdot 51 \cdot 50 \cdot 49}$$

    2.  different suits?
        -   Like the last problem, there are
            $52 \cdot 51 \cdot 50 \cdot 49$ total ways.
        -   But this time, each time a card is picked, there are 13 less
            choices.
            $$\frac{52 \cdot 39 \cdot 26 \cdot 13}{52 \cdot 51 \cdot 50 \cdot 49}$$

6.  Urn A contains 3 red and 3 black balls, whereas urn B contains 4 red
    and 6 black balls. If a ball is randomly selected from each urn,
    what is the probability that the balls will be the same color?
    -   R = "both balls were red."
    -   B = "both balls were black."
    -   There is a probability of zero that both these events happen.
    -   $P(R \cup B) = P(R) + P(B) - 0$
    -   $P(R) = \frac{3 \cdot 4}{6 \cdot 10}$
    -   $P(R) = \frac{3 \cdot 6}{6 \cdot 10}$

7.  In a state lottery, a player must choose 8 of the numbers from 1 to
    40. The lottery commission then performs an experiment that selects
    8 of these 40 numbers. Assuming that the choice of the lottery
    commission is equally likely to be any of the $40 \choose 8$
    combinations, what is the probability that a player has
    -   all 8 of the numbers selected by the lottery commission?
        -   They can only have one of the combinations.
            $$\frac{1}{40 \choose 8}$$

    -   7 of the numbers selected by the lottery commission?
        -   I think that there are $40 \cdot 39 ... \cdot 32$ total
            combinations.
        -   Having one of them would mean, I think,
            $$\frac{40 \cdot 39 ... \cdot 33}{40 \cdot 39 ... \cdot 32}$$
        -   Unfortunately, this is very wrong. The better way to think
            of this is there are 8 choose 7 ways of picking 7 numbers.
        -   I can't work out on my own what you need to multiply this
            by, I think it has something to do with the number of 7
            combination choices in a 40 choice pool.

    -   at least 6 of the numbers selected by the lottery commission?

8.  From a group of 3 freshmen, 4 sophomores, 4 juniors, and 3 seniors a
    committee of size 4 is randomly selected. Find the probability that
    the committee will consist of
    1.  1 from each class
        $$\frac{3 \times 4 \times 4 \times 3}{14 \choose 4}$$
        -   Every number in the numerator is like "number in class"
            choose 1, which is just "number in class."
    2.  2 sophomores and 2 juniors
        $$\frac{{4 \choose 2} \times {4 \choose 2}}{14 \choose 4}$$
        -   You have to pick two out of each 4, and then divide it by
            the entire sample space.
    3.  only sophomores or juniors
        $$\frac{8 \choose 4}{14 \choose 4}
        -   It could be all sophomores or all juniors, or a combination
            thereof, so just count them as one group with 8 choose 4.

9.  For a finite set A, let N(A) denote the number of elements in A.
    Show that:
    $$ N(A \cup B) = N(A) + N(B) − N(AB) $$

		     +-------------+      +-------------+
		    /               \    /               \
		   /                 \  /                 \
		  /                   \/                   \
		 /                    /\                    \
		|                    /  \                   | 
		|          A        | AB |       B          |
		|                   |    |                  |
		 \                   \  /                   /
		  \                   \/                   /
		   \                  /\                  /
		    \                /  \                /
		     +--------------+    +--------------+

    -   $A \cup B$ is equal to those elements in A plus all the elements
        in B.
    -   But that's double counting! Region AB is both in A and B, so you
        need to substract one instance of AB from the outcome.
    -   Therefore, $N(A \cup B) = N(A) + N(B) - N(AB)$
    
10.  Consider an experiment that consists of six horses, numbered 1 
     through 6, running a race, and suppose that the sample space 
     consists of the 6! possible orders in which the horses finish. 
     Let A be the event that the number-1 horse is among the top three 
     finishers, and let B be the event that the number-2 horse comes in 
     second. How many outcomes are in the event $A \cup B$?
     -   $A = $ "the number-1 horse is among the top three finishers"
     -   $B = $ "B be the event that the number-2 horse comes in second"
     -   $A \cup B = $ "the number-1 horse is among the top three
         finishers and the number-2 horse came second."
     -   For $B$, only one outcome is necessary, that the number-2 horse
         is second, the rest are totally variable.
     -   I think this means that the possible outcomes are therefore:
         $$\frac{5!}{6!}$$
         because you're only taking one of the choices "off the table."
     -   Similarly, there are $5!$ ways of specifying the position of
         horse one.
     -   So what is $N(AB)$?
         -   There is only one way for the number two horse to be in 
             the second position.
         -   There are two options for the first horse to be in the
             top three, then, in position one and position three.
         -   For each of these options, there are 6 choices for the
             unclaimed spot.












