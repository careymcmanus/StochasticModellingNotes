# Week 3 notes

## Lecture

SAMPLING WITH REPLACEMENT, WITHOUT ORDERING
    Picking k objects from n distinct objects with replacement, recording result without regard to order

* How many different ways can you choose k objects from n, with replacement and ignoring order?
    The answer is the number of different sequences of k for X's and n-1 for '/'s

    To work this out, think back to Example 2.21
        - the no. of distinct permutations of k white balls, n-k black balls = $\big(_k ^n) = \big(_{n-l} ^n)$
    
    The total number of symbols is $\big(_k ^{n+k-1}) = \big(_{n-1} ^{n+k-1}$

### Condition Probability

The Conditional Probability of Event A given that event B occurs (or Conditional on B occurring) is 

$$P(A|B) = \frac{P(A \cap B)}{P(B)}$$

Sometimes $P(A|B) = P(A)$ ie. $P(Raining \ in \ Denmark | Wearing \ Socks \ in Melbourne )$, In this case one event does not affect the other as in they are independent events.

In General howver extra information changes the conditional prob of an event. ie:

$$P(it \ rains \ in \ hawthorn|it \ is \ cloudy)$$ 

in this case $P(A|B) > P(A)$ (fair assumption).In General,

$$P(A|B) \neq P(A)$$

for $P(A|B) = \frac{P(A\capB)}{P(B)}$ effectively, the sample sapce has been reduced to the outcomes in B

** Note **
    Remember to distinguish between independent and mutually exclusive events. Independent events do not affect each but can both occur at the same time whereas mutually exclusive events cannot occur at the same time.

If A and B are Independent then:

$$
\begin{aligned}
P(A|B) &= P(A) \\
P(B|A) &= P(A)P(B) \\
P(A \cap B) &= P(A)P(B) 
\end{aligned}
$$

#### Example 2.24
    Urn - 4 Balls $\rightarrow$ #1 and #2 are black, #3 and #4 are white.
        Select one ball.
            * A = black ball selected$ 
            * B = even-numbered ""$
            * C = no.on selected ball > 2

$$
\begin{aligned}
P(A) &= \frac{2}{4} = \frac{1}{2} \\
P(B) &= \frac{2}{4} = \frac{1}{2} \\
P(C) &= \frac{2}{4} = \frac{1}{2} 
\end{aligned}
$$

Probability of A given B

$$
\begin{aligned}
P(A|B) &= \frac{P(A \cap B)}{P(B)} = \frac{P(even numbered black ball)}{\frac{1}{2}} \\
       &= \frac{\frac{1}{4}}{\frac{1}{2}} = \frac{1}{2} 
\end{aligned}
$$

Since $P(A|B) = P(A)$ this means that A and B are independent

Probability of A given C

$$
\begin{aligned}
P(A|C) &= \frac{A \cap C}{P(C)} \\
        &= \frac{0}{1/2} \\
        &= 0
\end{aligned}
$$

Since $(P(A|C) \neq P(A))$ they are not independent

For two events A,B to be both independent and mutually exclusive,

$$
\begin{aligned}
P(A \cap B) &= P(A)P(B) = 0 \\
            & \rightarrow P(A) / or / P(B) / or / both = 0
\end{aligned}
$$

This means that for all practical purposes events can't be Independent and Mutually Exclusive.

If A,B are independent, are A and $\bar{B}$? $\rightarrow$ Yes

#### Example 2.25
    Urn with 2 Black Balls, 3 White Balls. Two balls selected at random w/o replacement, sequence of colours is noted. What is P(Both Balls Black)?

$$
\begin{aligned}
\frac{\big(_2 ^2) \big(_0 ^3)}{\big(_2 ^ 5)} &= \frac{\frac{2!}{2!0!}\cdot \frac{3!}{0!3!}}{\frac{5!}{2!3!}} \\
    &= \frac{1}{\frac{5!}{2!3!}} \\
    &= \frac{1}{10}
P(B_1 \cap B_2) &= P(B_1) \times P(B_2 | B_1) \\
&= \frac{2}{5} \times \frac{1}{4} \\
&= \frac{1}{10}
\end{aligned}
$$

Let $B_1, B_2, ..., B_n$ Be mutually exclusive events whose union equals the sample space S.
    Then these events (sets) are a PARTITION of S, i.e $S = B_1 \cup B_2 .... \cup B_n$

Any event A can be written as $A = A \cap S$ 

$$
\begin{aligned}
A &= (A \cap B_1) \cup (A \cap B_2) \cup (A \cap B_3) \cup ... \cup (A \cap B_n) \\
\end{aligned}
$$

## Wednesday

### Example 2.26

BINARY COMMUNICATION SYSTEM

User Inputs 0 or 1, a signal gets transmitted. Based on the signal received, receiver decides what the input was. Suppose that user sends 0 with prob. 1-p, 1 with a prob. p and that the reciever makes random decision errors with probability $\epsilon$. For $i=0,1$ let $A_i =$ "input was i", $B_i =$ "receiver decision = i". Find $P(A_i \cap B_j)$ for $i=0,1 , j=0,1$.
g
$$
\begin{aligned}
P(A_0 \cap B_0) &= P(A_0) \dot P(B_0 | A_0) = (1-p)(1-\epsilon) \\
P(A_0 \cap B_1) &= P(A_0) \dot P(B_1 | A_0) = (1-p)(\epsilon) \\
P(A_1 \cap B_0) &= P(A_1) \dot P(B_0 | A_1) = p \epsilon \\
P(A_1 \cap B_1) &= P(A_1) \dot P(B_1 | A_1) = p (1 - \epsilon) \\

P(B_j|A) &= \frac{(PA|B_j)P(B_j)}{\sum_{k=1}^{n} P(A|B_k) \dot P(B_k)} (BAYES RULE)
\end{aligned}
$$

### Example 2.5 - System Reliability

System has a controller and 3 peripheral units. System is "up" if the controller and at least 2 of the peripherals work. Assume that the controller and each peripheral fail(or don't fail) independently of each other. let p = Pr(controller fails), a = Pr(peripheral fails) Fin Pr(System is "up").

$$
\begin{aligned}
P(system / up) &= P(Controller / AND / exactly / 2 Peripherals / work) + P(C / AND / all / 3 / peripherals / work) \\
&= 3 \times P(C) \times P(P_1) \times P(P_2) \times P(\bar{P_3})  + P(C) \times P(P_1) \times P(P_2) \times P(P_3) \\
&= \big(_1 ^3) (1-p)(1-a)^2 a + (1-p)(1-a)^3 \\
&= (1-p)(1-a)^2 (2a+1)
\end{aligned}
$$

## BERNOULLI TRIALS

    An experimental trial where we can classify the outcomes into 2 groups, one a "succes", the other a "failure", and P(success) = p, P(failure) = 1-p.

Consider a sequence of n INDEPENDENT Bernoulli trials, and let X be the total no. of "successes" in the n trials, then X is the Binomial random variable with parameters n and p.

$$P(X=x) = \big(_x ^n) p^x(1-p)^{n-x}, x=0,1,2,...,n$$

$\big(_x ^n)$ is the BINOMIAL COEFFICIENT = # different orderings of x S's and (n-x) F's

where $\big(_x ^n) = \frac{n!}{x!(n-x)!}$
