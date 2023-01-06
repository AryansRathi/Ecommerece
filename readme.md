# Probability distribution

# Contents

# Introduction[edit]

# General probability definition[edit]

# Terminology[edit]

# Basic terms[edit]

# Discrete probability distributions[edit]

# Absolutely continuous probability distributions[edit]

# Related terms[edit]

# Cumulative distribution function[edit]

# Discrete probability distribution[edit]

# Cumulative distribution function[edit]

# Dirac delta representation[edit]

# Indicator-function representation[edit]

# One-point distribution[edit]

# Absolutely continuous probability distribution[edit]

# Cumulative distribution function[edit]

# Kolmogorov definition[edit]

# Other kinds of distributions[edit]

# Random number generation[edit]

# Common probability distributions and their applications[edit]

# Linear growth (e.g. errors, offsets)[edit]

# Exponential growth (e.g. prices, incomes, populations)[edit]

# Uniformly distributed quantities[edit]

# Bernoulli trials (yes/no events, with a given probability)[edit]

# Categorical outcomes (events with K possible outcomes)[edit]

# Poisson process (events that occur independently with a given rate)[edit]

# Absolute values of vectors with normally distributed components[edit]

# Normally distributed quantities operated with sum of squares[edit]

# As conjugate prior distributions in Bayesian inference[edit]

# Some specialized applications of probability distributions[edit]

# Fitting[edit]

# See also[edit]

# Lists[edit]

# References[edit]

# Citations[edit]

# Sources[edit]

# External links[edit]

# Navigation menu

# 
Personal tools


# 
Namespaces


# 
Views


# 
Navigation


# 
Contribute


# 
Tools


# 
Print/export


# 
In other projects


# 
Languages


In probability theory and statistics, a probability distribution is the
mathematical function that gives the probabilities of occurrence of different
possible outcomes for an experiment.[1][2] It is a mathematical description of
a random phenomenon in terms of its sample space and the probabilities of
events (subsets of the sample space).[3]



For instance, if X is used to denote the outcome of a coin toss ("the
experiment"), then the probability distribution of X would take the value 0.5
(1 in 2 or 1/2) for X = heads, and 0.5 for X = tails (assuming that the coin
is fair). Examples of random phenomena include the weather conditions at some
future date, the height of a randomly selected person, the fraction of male
students in a school, the results of a survey to be conducted, etc.[4]



A probability distribution is a mathematical description of the probabilities
of events, subsets of the sample space. The sample space, often denoted by Ω
{\displaystyle \Omega } , is the set of all possible outcomes of a random
phenomenon being observed; it may be any set: a set of real numbers, a set of
vectors, a set of arbitrary non-numerical values, etc. For example, the sample
space of a coin flip would be Ω = {heads, tails}.



To define probability distributions for the specific case of random variables
(so the sample space can be seen as a numeric set), it is common to
distinguish between discrete and absolutely continuous random variables. In
the discrete case, it is sufficient to specify a probability mass function p
{\displaystyle p} assigning a probability to each possible outcome: for
example, when throwing a fair die, each of the six values 1 to 6 has the
probability 1/6. The probability of an event is then defined to be the sum of
the probabilities of the outcomes that satisfy the event; for example, the
probability of the event "the die rolls an even value" is p ( 2 ) \+ p ( 4 )
\+ p ( 6 ) = 1 / 6 \+ 1 / 6 \+ 1 / 6 = 1 / 2\. {\displaystyle
p(2)+p(4)+p(6)=1/6+1/6+1/6=1/2.}



In contrast, when a random variable takes values from a continuum then
typically, any individual outcome has probability zero and only events that
include infinitely many outcomes, such as intervals, can have positive
probability. For example, consider measuring the weight of a piece of ham in
the supermarket, and assume the scale has many digits of precision. The
probability that it weighs exactly 500 g is zero, as it will most likely have
some non-zero decimal digits. Nevertheless, one might demand, in quality
control, that a package of "500 g" of ham must weigh between 490 g and 510 g
with at least 98% probability, and this demand is less sensitive to the
accuracy of measurement instruments.



Absolutely continuous probability distributions can be described in several
ways. The probability density function describes the infinitesimal probability
of any given value, and the probability that the outcome lies in a given
interval can be computed by integrating the probability density function over
that interval.[5] An alternative description of the distribution is by means
of the cumulative distribution function, which describes the probability that
the random variable is no larger than a given value (i.e., P ( X < x )
{\displaystyle P(X<x)} for some x {\displaystyle x} ). The cumulative
distribution function is the area under the probability density function from
− ∞ {\displaystyle -\infty } to x {\displaystyle x} , as described by the
picture to the right.[6]



A probability distribution can be described in various forms, such as by a
probability mass function or a cumulative distribution function. One of the
most general descriptions, which applies for absolutely continuous and
discrete variables, is by means of a probability function P : A → R
{\displaystyle P\colon {\mathcal {A}}\to \mathbb {R} } whose input space A
{\displaystyle {\mathcal {A}}} is related[clarification needed] to the sample
space, and gives a real number probability as its output.[citation needed]



The probability function P {\displaystyle P} can take as argument subsets of
the sample space itself, as in the coin toss example, where the function P
{\displaystyle P} was defined so that P(heads) = 0.5 and P(tails) = 0.5.
However, because of the widespread use of random variables, which transform
the sample space into a set of numbers (e.g., R {\displaystyle \mathbb {R} } ,
N {\displaystyle \mathbb {N} } ), it is more common to study probability
distributions whose argument are subsets of these particular kinds of sets
(number sets),[7] and all probability distributions discussed in this article
are of this type. It is common to denote as P ( X ∈ E ) {\displaystyle P(X\in
E)} the probability that a certain value of the variable X {\displaystyle X}
belongs to a certain event E {\displaystyle E} .[4][8]



The above probability function only characterizes a probability distribution
if it satisfies all the Kolmogorov axioms, that is:



The concept of probability function is made more rigorous by defining it as
the element of a probability space ( X , A , P ) {\displaystyle (X,{\mathcal
{A}},P)} , where X {\displaystyle X} is the set of possible outcomes, A
{\displaystyle {\mathcal {A}}} is the set of all subsets E ⊂ X {\displaystyle
E\subset X} whose probability can be measured, and P {\displaystyle P} is the
probability function, or probability measure, that assigns a probability to
each of these measurable subsets E ∈ A {\displaystyle E\in {\mathcal {A}}}
.[9]



Probability distributions usually belong to one of two classes. A discrete
probability distribution is applicable to the scenarios where the set of
possible outcomes is discrete (e.g. a coin toss, a roll of a die) and the
probabilities are encoded by a discrete list of the probabilities of the
outcomes; in this case the discrete probability distribution is known as
probability mass function. On the other hand, absolutely continuous
probability distributions are applicable to scenarios where the set of
possible outcomes can take on values in a continuous range (e.g. real
numbers), such as the temperature on a given day. In the absolutely continuous
case, probabilities are described by a probability density function, and the
probability distribution is by definition the integral of the probability
density function.[4][5][8] The normal distribution is a commonly encountered
absolutely continuous probability distribution. More complex experiments, such
as those involving stochastic processes defined in continuous time, may demand
the use of more general probability measures.



A probability distribution whose sample space is one-dimensional (for example
real numbers, list of labels, ordered labels or binary) is called univariate,
while a distribution whose sample space is a vector space of dimension 2 or
more is called multivariate. A univariate distribution gives the probabilities
of a single random variable taking on various different values; a multivariate
distribution (a joint probability distribution) gives the probabilities of a
random vector – a list of two or more random variables – taking on various
combinations of values. Important and commonly encountered univariate
probability distributions include the binomial distribution, the
hypergeometric distribution, and the normal distribution. A commonly
encountered multivariate distribution is the multivariate normal distribution.



Besides the probability function, the cumulative distribution function, the
probability mass function and the probability density function, the moment
generating function and the characteristic function also serve to identify a
probability distribution, as they uniquely determine an underlying cumulative
distribution function.[10]



Some key concepts and terms, widely used in the literature on the topic of
probability distributions, are listed below.[1]



In the special case of a real-valued random variable, the probability
distribution can equivalently be represented by a cumulative distribution
function instead of a probability measure. The cumulative distribution
function of a random variable X {\displaystyle X} with regard to a probability
distribution p {\displaystyle p} is defined as F ( x ) = P ( X ≤ x ) .
{\displaystyle F(x)=P(X\leq x).}



The cumulative distribution function of any real-valued random variable has
the properties:



Conversely, any function F : R → R {\displaystyle F:\mathbb {R} \to \mathbb
{R} } that satisfies the first four of the properties above is the cumulative
distribution function of some probability distribution on the real
numbers.[13]



Any probability distribution can be decomposed as the sum of a discrete, an
absolutely continuous and a singular continuous distribution,[14] and thus any
cumulative distribution function admits a decomposition as the sum of the
three according cumulative distribution functions.



A discrete probability distribution is the probability distribution of a
random variable that can take on only a countable number of values[15] (almost
surely)[16] which means that the probability of any event E {\displaystyle E}
can be expressed as a (finite or countably infinite) sum: P ( X ∈ E ) = ∑ ω ∈
A P ( X = ω ) , {\displaystyle P(X\in E)=\sum _{\omega \in A}P(X=\omega ),}
where A {\displaystyle A} is a countable set. Thus the discrete random
variables are exactly those with a probability mass function p ( x ) = P ( X =
x ) {\displaystyle p(x)=P(X=x)} . In the case where the range of values is
countably infinite, these values have to decline to zero fast enough for the
probabilities to add up to 1. For example, if p ( n ) = 1 2 n {\displaystyle
p(n)={\tfrac {1}{2^{n}}}} for n = 1 , 2 , . . . {\displaystyle n=1,2,...} ,
the sum of probabilities would be 1 / 2 \+ 1 / 4 \+ 1 / 8 \+ ⋯ = 1
{\displaystyle 1/2+1/4+1/8+\dots =1} .



A discrete random variable is a random variable whose probability distribution
is discrete.



Well-known discrete probability distributions used in statistical modeling
include the Poisson distribution, the Bernoulli distribution, the binomial
distribution, the geometric distribution, the negative binomial distribution
and categorical distribution.[3] When a sample (a set of observations) is
drawn from a larger population, the sample points have an empirical
distribution that is discrete, and which provides information about the
population distribution. Additionally, the discrete uniform distribution is
commonly used in computer programs that make equal-probability random
selections between a number of choices.



A real-valued discrete random variable can equivalently be defined as a random
variable whose cumulative distribution function increases only by jump
discontinuities—that is, its cdf increases only where it "jumps" to a higher
value, and is constant in intervals without jumps. The points where jumps
occur are precisely the values which the random variable may take. Thus the
cumulative distribution function has the form F ( x ) = P ( X ≤ x ) = ∑ ω ≤ x
p ( ω ) . {\displaystyle F(x)=P(X\leq x)=\sum _{\omega \leq x}p(\omega ).}



Note that the points where the cdf jumps always form a countable set; this may
be any countable set and thus may even be dense in the real numbers.



A discrete probability distribution is often represented with Dirac measures,
the probability distributions of deterministic random variables. For any
outcome ω {\displaystyle \omega } , let δ ω {\displaystyle \delta _{\omega }}
be the Dirac measure concentrated at ω {\displaystyle \omega } . Given a
discrete probability distribution, there is a countable set A {\displaystyle
A} with P ( X ∈ A ) = 1 {\displaystyle P(X\in A)=1} and a probability mass
function p {\displaystyle p} . If E {\displaystyle E} is any event, then P ( X
∈ E ) = ∑ ω ∈ A p ( ω ) δ ω ( E ) , {\displaystyle P(X\in E)=\sum _{\omega \in
A}p(\omega )\delta _{\omega }(E),} or in short, P X = ∑ ω ∈ A p ( ω ) δ ω .
{\displaystyle P_{X}=\sum _{\omega \in A}p(\omega )\delta _{\omega }.}



Similarly, discrete distributions can be represented with the Dirac delta
function as a generalized probability density function f {\displaystyle f} ,
where f ( x ) = ∑ ω ∈ A p ( ω ) δ ( x − ω ) , {\displaystyle f(x)=\sum
_{\omega \in A}p(\omega )\delta (x-\omega ),} which means P ( X ∈ E ) = ∫ E f
( x ) d x = ∑ ω ∈ A p ( ω ) ∫ E δ ( x − ω ) = ∑ ω ∈ A ∩ E p ( ω )
{\displaystyle P(X\in E)=\int _{E}f(x)\,dx=\sum _{\omega \in A}p(\omega )\int
_{E}\delta (x-\omega )=\sum _{\omega \in A\cap E}p(\omega )} for any event E .
{\displaystyle E.} [17]



For a discrete random variable X {\displaystyle X} , let u 0 , u 1 , …
{\displaystyle u_{0},u_{1},\dots } be the values it can take with non-zero
probability. Denote



Ω i = X − 1 ( u i ) = { ω : X ( ω ) = u i } , i = 0 , 1 , 2 , … {\displaystyle
\Omega _{i}=X^{-1}(u_{i})=\\{\omega :X(\omega )=u_{i}\\},\,i=0,1,2,\dots }



These are disjoint sets, and for such sets



P ( ⋃ i Ω i ) = ∑ i P ( Ω i ) = ∑ i P ( X = u i ) = 1\. {\displaystyle
P\left(\bigcup _{i}\Omega _{i}\right)=\sum _{i}P(\Omega _{i})=\sum
_{i}P(X=u_{i})=1.}



It follows that the probability that X {\displaystyle X} takes any value
except for u 0 , u 1 , … {\displaystyle u_{0},u_{1},\dots } is zero, and thus
one can write X {\displaystyle X} as



X ( ω ) = ∑ i u i 1 Ω i ( ω ) {\displaystyle X(\omega )=\sum
_{i}u_{i}1_{\Omega _{i}}(\omega )}



except on a set of probability zero, where 1 A {\displaystyle 1_{A}} is the
indicator function of A {\displaystyle A} . This may serve as an alternative
definition of discrete random variables.



A special case is the discrete distribution of a random variable that can take
on only one fixed value; in other words, it is a deterministic distribution.
Expressed formally, the random variable X {\displaystyle X} has a one-point
distribution if it has a possible outcome x {\displaystyle x} such that P ( X
= x ) = 1\. {\displaystyle P(X{=}x)=1.} [18] All other possible outcomes then
have probability 0. Its cumulative distribution function jumps immediately
from 0 to 1.



An absolutely continuous probability distribution is a probability
distribution on the real numbers with uncountably many possible values, such
as a whole interval in the real line, and where the probability of any event
can be expressed as an integral.[19] More precisely, a real random variable X
{\displaystyle X} has an absolutely continuous probability distribution if
there is a function f : R → [ 0 , ∞ ] {\displaystyle f:\mathbb {R} \to
[0,\infty ]} such that for each interval [ a , b ] ⊂ R {\displaystyle
[a,b]\subset \mathbb {R} } the probability of X {\displaystyle X} belonging to
[ a , b ] {\displaystyle [a,b]} is given by the integral of f {\displaystyle
f} over I {\displaystyle I} :[20][21] P ( a ≤ X ≤ b ) = ∫ a b f ( x ) d x .
{\displaystyle P\left(a\leq X\leq b\right)=\int _{a}^{b}f(x)\,dx.} This is the
definition of a probability density function, so that absolutely continuous
probability distributions are exactly those with a probability density
function. In particular, the probability for X {\displaystyle X} to take any
single value a {\displaystyle a} (that is, a ≤ X ≤ a {\displaystyle a\leq
X\leq a} ) is zero, because an integral with coinciding upper and lower limits
is always equal to zero. If the interval [ a , b ] {\displaystyle [a,b]} is
replaced by any measurable set A {\displaystyle A} , the according equality
still holds: P ( X ∈ A ) = ∫ A f ( x ) d x . {\displaystyle P(X\in A)=\int
_{A}f(x)\,dx.}



An absolutely continuous random variable is a random variable whose
probability distribution is absolutely continuous.



There are many examples of absolutely continuous probability distributions:
normal, uniform, chi-squared, and others.



Absolutely continuous probability distributions as defined above are precisely
those with an absolutely continuous cumulative distribution function. In this
case, the cumulative distribution function F {\displaystyle F} has the form F
( x ) = P ( X ≤ x ) = ∫ − ∞ x f ( t ) d t {\displaystyle F(x)=P(X\leq x)=\int
_{-\infty }^{x}f(t)\,dt} where f {\displaystyle f} is a density of the random
variable X {\displaystyle X} with regard to the distribution P {\displaystyle
P} .



Note on terminology: Absolutely continuous distributions ought to be
distinguished from continuous distributions, which are those having a
continuous cumulative distribution function. Every absolutely continuous
distribution is a continuous distribution but the converse is not true, there
exist singular distributions, which are neither absolutely continuous nor
discrete nor a mixture of those, and do not have a density. An example is
given by the Cantor distribution. Some authors however use the term
"continuous distribution" to denote all distributions whose cumulative
distribution function is absolutely continuous, i.e. refer to absolutely
continuous distributions as continuous distributions.[4]



For a more general definition of density functions and the equivalent
absolutely continuous measures see absolutely continuous measure.



In the measure-theoretic formalization of probability theory, a random
variable is defined as a measurable function X {\displaystyle X} from a
probability space ( Ω , F , P ) {\displaystyle (\Omega ,{\mathcal {F}},\mathbb
{P} )} to a measurable space ( X , A ) {\displaystyle ({\mathcal
{X}},{\mathcal {A}})} . Given that probabilities of events of the form { ω ∈ Ω
∣ X ( ω ) ∈ A } {\displaystyle \\{\omega \in \Omega \mid X(\omega )\in A\\}}
satisfy Kolmogorov's probability axioms, the probability distribution of X
{\displaystyle X} is the image measure X ∗ P {\displaystyle X_{*}\mathbb {P} }
of X {\displaystyle X} , which is a probability measure on ( X , A )
{\displaystyle ({\mathcal {X}},{\mathcal {A}})} satisfying X ∗ P = P X − 1
{\displaystyle X_{*}\mathbb {P} =\mathbb {P} X^{-1}} .[22][23][24]



Absolutely continuous and discrete distributions with support on R k
{\displaystyle \mathbb {R} ^{k}} or N k {\displaystyle \mathbb {N} ^{k}} are
extremely useful to model a myriad of phenomena,[4][6] since most practical
distributions are supported on relatively simple subsets, such as hypercubes
or balls. However, this is not always the case, and there exist phenomena with
supports that are actually complicated curves γ : [ a , b ] → R n
{\displaystyle \gamma :[a,b]\rightarrow \mathbb {R} ^{n}} within some space R
n {\displaystyle \mathbb {R} ^{n}} or similar. In these cases, the probability
distribution is supported on the image of such curve, and is likely to be
determined empirically, rather than finding a closed formula for it.[25]



One example is shown in the figure to the right, which displays the evolution
of a system of differential equations (commonly known as the
Rabinovich–Fabrikant equations) that can be used to model the behaviour of
Langmuir waves in plasma.[26] When this phenomenon is studied, the observed
states from the subset are as indicated in red. So one could ask what is the
probability of observing a state in a certain position of the red subset; if
such a probability exists, it is called the probability measure of the
system.[27][25]



This kind of complicated support appears quite frequently in dynamical
systems. It is not simple to establish that the system has a probability
measure, and the main problem is the following. Let t 1 ≪ t 2 ≪ t 3
{\displaystyle t_{1}\ll t_{2}\ll t_{3}} be instants in time and O
{\displaystyle O} a subset of the support; if the probability measure exists
for the system, one would expect the frequency of observing states inside set
O {\displaystyle O} would be equal in interval [ t 1 , t 2 ] {\displaystyle
[t_{1},t_{2}]} and [ t 2 , t 3 ] {\displaystyle [t_{2},t_{3}]} , which might
not happen; for example, it could oscillate similar to a sine, sin ⁡ ( t )
{\displaystyle \sin(t)} , whose limit when t → ∞ {\displaystyle t\rightarrow
\infty } does not converge. Formally, the measure exists only if the limit of
the relative frequency converges when the system is observed into the infinite
future.[28] The branch of dynamical systems that studies the existence of a
probability measure is ergodic theory.



Note that even in these cases, the probability distribution, if it exists,
might still be termed "absolutely continuous" or "discrete" depending on
whether the support is uncountable or countable, respectively.



Most algorithms are based on a pseudorandom number generator that produces
numbers X {\displaystyle X} that are uniformly distributed in the half-open
interval [0, 1). These random variates X {\displaystyle X} are then
transformed via some algorithm to create a new random variate having the
required probability distribution. With this source of uniform pseudo-
randomness, realizations of any random variable can be generated.[29]



For example, suppose U {\displaystyle U} has a uniform distribution between 0
and 1. To construct a random Bernoulli variable for some 0 < p < 1
{\displaystyle 0<p<1} , we define X = { 1 , if U < p 0 , if U ≥ p
{\displaystyle X={\begin{cases}1,&{\text{if }}U<p\\\0,&{\text{if }}U\geq
p\end{cases}}} so that Pr ( X = 1 ) = Pr ( U < p ) = p , Pr ( X = 0 ) = Pr ( U
≥ p ) = 1 − p . {\displaystyle \Pr(X=1)=\Pr(U<p)=p,\quad \Pr(X=0)=\Pr(U\geq
p)=1-p.}



This random variable X has a Bernoulli distribution with parameter p
{\displaystyle p} .[29] Note that this is a transformation of discrete random
variable.



For a distribution function F {\displaystyle F} of an absolutely continuous
random variable, an absolutely continuous random variable must be constructed.
F i n v {\displaystyle F^{\mathit {inv}}} , an inverse function of F
{\displaystyle F} , relates to the uniform variable U {\displaystyle U} : U ≤
F ( x ) = F i n v ( U ) ≤ x . {\displaystyle {U\leq F(x)}={F^{\mathit
{inv}}(U)\leq x}.}



For example, suppose a random variable that has an exponential distribution F
( x ) = 1 − e − λ x {\displaystyle F(x)=1-e^{-\lambda x}} must be constructed.



F ( x ) = u ⇔ 1 − e − λ x = u ⇔ e − λ x = 1 − u ⇔ − λ x = ln ⁡ ( 1 − u ) ⇔ x =
− 1 λ ln ⁡ ( 1 − u ) {\displaystyle {\begin{aligned}F(x)=u&\Leftrightarrow
1-e^{-\lambda x}=u\\\\[2pt]&\Leftrightarrow e^{-\lambda
x}=1-u\\\\[2pt]&\Leftrightarrow -\lambda x=\ln(1-u)\\\\[2pt]&\Leftrightarrow
x={\frac {-1}{\lambda }}\ln(1-u)\end{aligned}}} so F i n v ( u ) = − 1 λ ln ⁡
( 1 − u ) {\displaystyle F^{\mathit {inv}}(u)={\frac {-1}{\lambda }}\ln(1-u)}
and if U {\displaystyle U} has a U ( 0 , 1 ) {\displaystyle U(0,1)}
distribution, then the random variable X {\displaystyle X} is defined by X = F
i n v ( U ) = − 1 λ ln ⁡ ( 1 − U ) {\displaystyle X=F^{\mathit
{inv}}(U)={\frac {-1}{\lambda }}\ln(1-U)} . This has an exponential
distribution of λ {\displaystyle \lambda } .[29]



A frequent problem in statistical simulations (the Monte Carlo method) is the
generation of pseudo-random numbers that are distributed in a given way.



The concept of the probability distribution and the random variables which
they describe underlies the mathematical discipline of probability theory, and
the science of statistics. There is spread or variability in almost any value
that can be measured in a population (e.g. height of people, durability of a
metal, sales growth, traffic flow, etc.); almost all measurements are made
with some intrinsic error; in physics, many processes are described
probabilistically, from the kinetic properties of gases to the quantum
mechanical description of fundamental particles. For these and many other
reasons, simple numbers are often inadequate for describing a quantity, while
probability distributions are often more appropriate.



The following is a list of some of the most common probability distributions,
grouped by the type of process that they are related to. For a more complete
list, see list of probability distributions, which groups by the nature of the
outcome being considered (discrete, absolutely continuous, multivariate, etc.)



All of the univariate distributions below are singly peaked; that is, it is
assumed that the values cluster around a single point. In practice, actually
observed quantities may cluster around multiple values. Such quantities can be
modeled using a mixture distribution.



Probability distribution fitting or simply distribution fitting is the fitting
of a probability distribution to a series of data concerning the repeated
measurement of a variable phenomenon. The aim of distribution fitting is to
predict the probability or to forecast the frequency of occurrence of the
magnitude of the phenomenon in a certain interval.



There are many probability distributions (see list of probability
distributions) of which some can be fitted more closely to the observed
frequency of the data than others, depending on the characteristics of the
phenomenon and of the distribution. The distribution giving a close fit is
supposed to lead to good predictions.



- Probability Axioms


- Axioms


- Determinism System


- System


- Indeterminism


- Randomness



- Axioms



- System



- Probability space


- Sample space


- Event Collectively exhaustive events Elementary event Mutual exclusivity
Outcome Singleton


- Collectively exhaustive events


- Elementary event


- Mutual exclusivity


- Outcome


- Singleton


- Experiment Bernoulli trial


- Bernoulli trial


- Probability distribution Bernoulli distribution Binomial distribution Normal
distribution


- Bernoulli distribution


- Binomial distribution


- Normal distribution


- Probability measure


- Random variable Bernoulli process Continuous or discrete Expected value Markov
chain Observed value Random walk Stochastic process


- Bernoulli process


- Continuous or discrete


- Expected value


- Markov chain


- Observed value


- Random walk


- Stochastic process



- Collectively exhaustive events


- Elementary event


- Mutual exclusivity


- Outcome


- Singleton



- Bernoulli trial



- Bernoulli distribution


- Binomial distribution


- Normal distribution



- Bernoulli process


- Continuous or discrete


- Expected value


- Markov chain


- Observed value


- Random walk


- Stochastic process



- Complementary event


- Joint probability


- Marginal probability


- Conditional probability



- Independence


- Conditional independence


- Law of total probability


- Law of large numbers


- Bayes' theorem


- Boole's inequality



- Venn diagram


- Tree diagram



- v


- t


- e



- 1 Introduction


- 2 General probability definition


- 3 Terminology 3.1 Basic terms 3.2 Discrete probability distributions 3.3
Absolutely continuous probability distributions 3.4 Related terms


- 3.1 Basic terms


- 3.2 Discrete probability distributions


- 3.3 Absolutely continuous probability distributions


- 3.4 Related terms


- 4 Cumulative distribution function


- 5 Discrete probability distribution 5.1 Cumulative distribution function 5.2
Dirac delta representation 5.3 Indicator-function representation 5.4 One-point
distribution


- 5.1 Cumulative distribution function


- 5.2 Dirac delta representation


- 5.3 Indicator-function representation


- 5.4 One-point distribution


- 6 Absolutely continuous probability distribution 6.1 Cumulative distribution
function


- 6.1 Cumulative distribution function


- 7 Kolmogorov definition


- 8 Other kinds of distributions


- 9 Random number generation


- 10 Common probability distributions and their applications 10.1 Linear growth
(e.g. errors, offsets) 10.2 Exponential growth (e.g. prices, incomes,
populations) 10.3 Uniformly distributed quantities 10.4 Bernoulli trials
(yes/no events, with a given probability) 10.5 Categorical outcomes (events
with K possible outcomes) 10.6 Poisson process (events that occur
independently with a given rate) 10.7 Absolute values of vectors with normally
distributed components 10.8 Normally distributed quantities operated with sum
of squares 10.9 As conjugate prior distributions in Bayesian inference 10.10
Some specialized applications of probability distributions


- 10.1 Linear growth (e.g. errors, offsets)


- 10.2 Exponential growth (e.g. prices, incomes, populations)


- 10.3 Uniformly distributed quantities


- 10.4 Bernoulli trials (yes/no events, with a given probability)


- 10.5 Categorical outcomes (events with K possible outcomes)


- 10.6 Poisson process (events that occur independently with a given rate)


- 10.7 Absolute values of vectors with normally distributed components


- 10.8 Normally distributed quantities operated with sum of squares


- 10.9 As conjugate prior distributions in Bayesian inference


- 10.10 Some specialized applications of probability distributions


- 11 Fitting


- 12 See also 12.1 Lists


- 12.1 Lists


- 13 References 13.1 Citations 13.2 Sources


- 13.1 Citations


- 13.2 Sources


- 14 External links



- 3.1 Basic terms


- 3.2 Discrete probability distributions


- 3.3 Absolutely continuous probability distributions


- 3.4 Related terms



- 5.1 Cumulative distribution function


- 5.2 Dirac delta representation


- 5.3 Indicator-function representation


- 5.4 One-point distribution



- 6.1 Cumulative distribution function



- 10.1 Linear growth (e.g. errors, offsets)


- 10.2 Exponential growth (e.g. prices, incomes, populations)


- 10.3 Uniformly distributed quantities


- 10.4 Bernoulli trials (yes/no events, with a given probability)


- 10.5 Categorical outcomes (events with K possible outcomes)


- 10.6 Poisson process (events that occur independently with a given rate)


- 10.7 Absolute values of vectors with normally distributed components


- 10.8 Normally distributed quantities operated with sum of squares


- 10.9 As conjugate prior distributions in Bayesian inference


- 10.10 Some specialized applications of probability distributions



- 12.1 Lists



- 13.1 Citations


- 13.2 Sources



- Random variable: takes values from a sample space; probabilities describe
which values and set of values are taken more likely.


- Event: set of possible values (outcomes) of a random variable that occurs with
a certain probability.


- Probability function or probability measure: describes the probability P ( X ∈
E ) {\displaystyle P(X\in E)} that the event E , {\displaystyle E,}
occurs.[11]


- Cumulative distribution function: function evaluating the probability that X
{\displaystyle X} will take a value less than or equal to x {\displaystyle x}
for a random variable (only for real-valued random variables).


- Quantile function: the inverse of the cumulative distribution function. Gives
x {\displaystyle x} such that, with probability q {\displaystyle q} , X
{\displaystyle X} will not exceed x {\displaystyle x} .



- Discrete probability distribution: for many random variables with finitely or
countably infinitely many values.


- Probability mass function (pmf): function that gives the probability that a
discrete random variable is equal to some value.


- Frequency distribution: a table that displays the frequency of various
outcomes in a sample.


- Relative frequency distribution: a frequency distribution where each value has
been divided (normalized) by a number of outcomes in a sample (i.e. sample
size).


- Categorical distribution: for discrete random variables with a finite set of
values.



- Absolutely continuous probability distribution: for many random variables with
uncountably many values.


- Probability density function (pdf) or probability density: function whose
value at any given sample (or point) in the sample space (the set of possible
values taken by the random variable) can be interpreted as providing a
relative likelihood that the value of the random variable would equal that
sample.



- Support: set of values that can be assumed with non-zero probability by the
random variable. For a random variable X {\displaystyle X} , it is sometimes
denoted as R X {\displaystyle R_{X}} .


- Tail:[12] the regions close to the bounds of the random variable, if the pmf
or pdf are relatively low therein. Usually has the form X > a {\displaystyle
X>a} , X < b {\displaystyle X<b} or a union thereof.


- Head:[12] the region where the pmf or pdf is relatively high. Usually has the
form a < X < b {\displaystyle a<X<b} .


- Expected value or mean: the weighted average of the possible values, using
their probabilities as their weights; or the continuous analog thereof.


- Median: the value such that the set of values less than the median, and the
set greater than the median, each have probabilities no greater than one-half.


- Mode: for a discrete random variable, the value with highest probability; for
an absolutely continuous random variable, a location at which the probability
density function has a local peak.


- Quantile: the q-quantile is the value x {\displaystyle x} such that P ( X < x
) = q {\displaystyle P(X<x)=q} .


- Variance: the second moment of the pmf or pdf about the mean; an important
measure of the dispersion of the distribution.


- Standard deviation: the square root of the variance, and hence another measure
of dispersion.


- Symmetry: a property of some distributions in which the portion of the
distribution to the left of a specific value (usually the median) is a mirror
image of the portion to its right.


- Skewness: a measure of the extent to which a pmf or pdf "leans" to one side of
its mean. The third standardized moment of the distribution.


- Kurtosis: a measure of the "fatness" of the tails of a pmf or pdf. The fourth
standardized moment of the distribution.



- 


- F ( x ) {\displaystyle F(x)} is non-decreasing;


- 


- F ( x ) {\displaystyle F(x)} is right-continuous;


- 


- 0 ≤ F ( x ) ≤ 1 {\displaystyle 0\leq F(x)\leq 1} ;


- 


- lim x → − ∞ F ( x ) = 0 {\displaystyle \lim _{x\to -\infty }F(x)=0} and lim x
→ ∞ F ( x ) = 1 {\displaystyle \lim _{x\to \infty }F(x)=1} ; and


- 


- Pr ( a < X ≤ b ) = F ( b ) − F ( a ) {\displaystyle \Pr(a<X\leq b)=F(b)-F(a)}
.



- Normal distribution (Gaussian distribution), for a single such quantity; the
most commonly used absolutely continuous distribution



- Log-normal distribution, for a single such quantity whose log is normally
distributed


- Pareto distribution, for a single such quantity whose log is exponentially
distributed; the prototypical power law distribution



- Discrete uniform distribution, for a finite set of values (e.g. the outcome of
a fair die)


- Continuous uniform distribution, for absolutely continuously distributed
values



- Basic distributions: Bernoulli distribution, for the outcome of a single
Bernoulli trial (e.g. success/failure, yes/no) Binomial distribution, for the
number of "positive occurrences" (e.g. successes, yes votes, etc.) given a
fixed total number of independent occurrences Negative binomial distribution,
for binomial-type observations but where the quantity of interest is the
number of failures before a given number of successes occurs Geometric
distribution, for binomial-type observations but where the quantity of
interest is the number of failures before the first success; a special case of
the negative binomial distribution


- Bernoulli distribution, for the outcome of a single Bernoulli trial (e.g.
success/failure, yes/no)


- Binomial distribution, for the number of "positive occurrences" (e.g.
successes, yes votes, etc.) given a fixed total number of independent
occurrences


- Negative binomial distribution, for binomial-type observations but where the
quantity of interest is the number of failures before a given number of
successes occurs


- Geometric distribution, for binomial-type observations but where the quantity
of interest is the number of failures before the first success; a special case
of the negative binomial distribution


- Related to sampling schemes over a finite population: Hypergeometric
distribution, for the number of "positive occurrences" (e.g. successes, yes
votes, etc.) given a fixed number of total occurrences, using sampling without
replacement Beta-binomial distribution, for the number of "positive
occurrences" (e.g. successes, yes votes, etc.) given a fixed number of total
occurrences, sampling using a Pólya urn model (in some sense, the "opposite"
of sampling without replacement)


- Hypergeometric distribution, for the number of "positive occurrences" (e.g.
successes, yes votes, etc.) given a fixed number of total occurrences, using
sampling without replacement


- Beta-binomial distribution, for the number of "positive occurrences" (e.g.
successes, yes votes, etc.) given a fixed number of total occurrences,
sampling using a Pólya urn model (in some sense, the "opposite" of sampling
without replacement)



- Bernoulli distribution, for the outcome of a single Bernoulli trial (e.g.
success/failure, yes/no)


- Binomial distribution, for the number of "positive occurrences" (e.g.
successes, yes votes, etc.) given a fixed total number of independent
occurrences


- Negative binomial distribution, for binomial-type observations but where the
quantity of interest is the number of failures before a given number of
successes occurs


- Geometric distribution, for binomial-type observations but where the quantity
of interest is the number of failures before the first success; a special case
of the negative binomial distribution



- Hypergeometric distribution, for the number of "positive occurrences" (e.g.
successes, yes votes, etc.) given a fixed number of total occurrences, using
sampling without replacement


- Beta-binomial distribution, for the number of "positive occurrences" (e.g.
successes, yes votes, etc.) given a fixed number of total occurrences,
sampling using a Pólya urn model (in some sense, the "opposite" of sampling
without replacement)



- Categorical distribution, for a single categorical outcome (e.g. yes/no/maybe
in a survey); a generalization of the Bernoulli distribution


- Multinomial distribution, for the number of each type of categorical outcome,
given a fixed number of total outcomes; a generalization of the binomial
distribution


- Multivariate hypergeometric distribution, similar to the multinomial
distribution, but using sampling without replacement; a generalization of the
hypergeometric distribution



- Poisson distribution, for the number of occurrences of a Poisson-type event in
a given period of time


- Exponential distribution, for the time before the next Poisson-type event
occurs


- Gamma distribution, for the time before the next k Poisson-type events occur



- Rayleigh distribution, for the distribution of vector magnitudes with Gaussian
distributed orthogonal components. Rayleigh distributions are found in RF
signals with Gaussian real and imaginary components.


- Rice distribution, a generalization of the Rayleigh distributions for where
there is a stationary background signal component. Found in Rician fading of
radio signals due to multipath propagation and in MR images with noise
corruption on non-zero NMR signals.



- Chi-squared distribution, the distribution of a sum of squared standard normal
variables; useful e.g. for inference regarding the sample variance of normally
distributed samples (see chi-squared test)


- Student's t distribution, the distribution of the ratio of a standard normal
variable and the square root of a scaled chi squared variable; useful for
inference regarding the mean of normally distributed samples with unknown
variance (see Student's t-test)


- F-distribution, the distribution of the ratio of two scaled chi squared
variables; useful e.g. for inferences that involve comparing variances or
involving R-squared (the squared correlation coefficient)



- Beta distribution, for a single probability (real number between 0 and 1);
conjugate to the Bernoulli distribution and binomial distribution


- Gamma distribution, for a non-negative scaling parameter; conjugate to the
rate parameter of a Poisson distribution or exponential distribution, the
precision (inverse variance) of a normal distribution, etc.


- Dirichlet distribution, for a vector of probabilities that must sum to 1;
conjugate to the categorical distribution and multinomial distribution;
generalization of the beta distribution


- Wishart distribution, for a symmetric non-negative definite matrix; conjugate
to the inverse of the covariance matrix of a multivariate normal distribution;
generalization of the gamma distribution[30]



- The cache language models and other statistical language models used in
natural language processing to assign probabilities to the occurrence of
particular words and word sequences do so by means of probability
distributions.


- In quantum mechanics, the probability density of finding the particle at a
given point is proportional to the square of the magnitude of the particle's
wavefunction at that point (see Born rule). Therefore, the probability
distribution function of the position of a particle is described by P a ≤ x ≤
b ( t ) = ∫ a b d x | Ψ ( x , t ) | 2 {\textstyle P_{a\leq x\leq b}(t)=\int
_{a}^{b}dx\,|\Psi (x,t)|^{2}} , probability that the particle's position x
will be in the interval a ≤ x ≤ b in dimension one, and a similar triple
integral in dimension three. This is a key principle of quantum mechanics.[31]


- Probabilistic load flow in power-flow study explains the uncertainties of
input variables as probability distribution and provides the power flow
calculation also in term of probability distribution.[32]


- Prediction of natural phenomena occurrences based on previous frequency
distributions such as tropical cyclones, hail, time in between events,
etc.[33]



- Mathematics portal



- Conditional probability distribution


- Joint probability distribution


- Quasiprobability distribution


- Empirical probability distribution


- Histogram


- Riemann–Stieltjes integral application to probability theory



- List of probability distributions


- List of statistical topics



- den Dekker, A. J.; Sijbers, J. (2014). "Data distributions in magnetic
resonance images: A review". Physica Medica. 30 (7): 725–741.
doi:10.1016/j.ejmp.2014.05.002. PMID 25059432.


- Vapnik, Vladimir Naumovich (1998). Statistical Learning Theory. John Wiley and
Sons.



- "Probability distribution", Encyclopedia of Mathematics, EMS Press, 2001
[1994]


- Field Guide to Continuous Probability Distributions, Gavin E. Crooks.



- v


- t


- e



- Benford


- Bernoulli


- beta-binomial


- binomial


- categorical


- hypergeometric negative


- negative


- Poisson binomial


- Rademacher


- soliton


- discrete uniform


- Zipf


- Zipf–Mandelbrot



- negative



- beta negative binomial


- Borel


- Conway–Maxwell–Poisson


- discrete phase-type


- Delaporte


- extended negative binomial


- Flory–Schulz


- Gauss–Kuzmin


- geometric


- logarithmic


- mixed Poisson


- negative binomial


- Panjer


- parabolic fractal


- Poisson


- Skellam


- Yule–Simon


- zeta



- arcsine


- ARGUS


- Balding–Nichols


- Bates


- beta


- beta rectangular


- continuous Bernoulli


- Irwin–Hall


- Kumaraswamy


- logit-normal


- noncentral beta


- PERT


- raised cosine


- reciprocal


- triangular


- U-quadratic


- uniform


- Wigner semicircle



- Benini


- Benktander 1st kind


- Benktander 2nd kind


- beta prime


- Burr


- chi


- chi-squared noncentral inverse scaled


- noncentral


- inverse scaled


- scaled


- Dagum


- Davis


- Erlang hyper


- hyper


- exponential hyperexponential hypoexponential logarithmic


- hyperexponential


- hypoexponential


- logarithmic


- F noncentral


- noncentral


- folded normal


- Fréchet


- gamma generalized inverse


- generalized


- inverse


- gamma/Gompertz


- Gompertz shifted


- shifted


- half-logistic


- half-normal


- Hotelling's T-squared


- inverse Gaussian generalized


- generalized


- Kolmogorov


- Lévy


- log-Cauchy


- log-Laplace


- log-logistic


- log-normal


- log-t


- Lomax


- matrix-exponential


- Maxwell–Boltzmann


- Maxwell–Jüttner


- Mittag-Leffler


- Nakagami


- Pareto


- phase-type


- Poly-Weibull


- Rayleigh


- relativistic Breit–Wigner


- Rice


- truncated normal


- type-2 Gumbel


- Weibull discrete


- discrete


- Wilks's lambda



- noncentral


- inverse scaled


- scaled



- scaled



- hyper



- hyperexponential


- hypoexponential


- logarithmic



- noncentral



- generalized


- inverse



- shifted



- generalized



- discrete



- Cauchy


- exponential power


- Fisher's z


- Kaniadakis κ-Gaussian


- Gaussian q


- generalized normal


- generalized hyperbolic


- geometric stable


- Gumbel


- Holtsmark


- hyperbolic secant


- Johnson's SU


- Landau


- Laplace asymmetric


- asymmetric


- logistic


- noncentral t


- normal (Gaussian)


- normal-inverse Gaussian


- skew normal


- slash


- stable


- Student's t


- Tracy–Widom


- variance-gamma


- Voigt



- asymmetric



- generalized chi-squared


- generalized extreme value


- generalized Pareto


- Marchenko–Pastur


- Kaniadakis κ-exponential


- Kaniadakis κ-Gamma


- Kaniadakis κ-Weibull


- Kaniadakis κ-Logistic


- Kaniadakis κ-Erlangl


- q-exponential


- q-Gaussian


- q-Weibull


- shifted log-logistic


- Tukey lambda



- Rectified Gaussian



- Discrete:


- Ewens


- multinomial Dirichlet negative


- Dirichlet


- negative


- Continuous:


- Dirichlet generalized


- generalized


- multivariate Laplace


- multivariate normal


- multivariate stable


- multivariate t


- normal-gamma inverse


- inverse


- Matrix-valued:


- LKJ


- matrix normal


- matrix t


- matrix gamma inverse matrix gamma


- inverse matrix gamma


- Wishart normal inverse normal-inverse


- normal


- inverse


- normal-inverse



- Dirichlet


- negative



- generalized



- inverse



- inverse matrix gamma



- normal


- inverse


- normal-inverse



- Circular


- compound Poisson


- elliptical


- exponential


- natural exponential


- location–scale


- maximum entropy


- mixture


- Pearson


- Tweedie


- wrapped



- Category


- Commons



- v


- t


- e



- probability mass function (pmf)


- probability density function (pdf)


- cumulative distribution function (cdf)


- quantile function



- raw moment


- central moment


- mean


- variance


- standard deviation


- skewness


- kurtosis


- L-moment



- moment-generating function (mgf)


- characteristic function


- probability-generating function (pgf)


- cumulant


- combinant



- v


- t


- e



- Outline


- Index



- Mean Arithmetic Cubic Generalized/power Geometric Harmonic Heinz Lehmer


- Arithmetic


- Cubic


- Generalized/power


- Geometric


- Harmonic


- Heinz


- Lehmer


- Median


- Mode



- Arithmetic


- Cubic


- Generalized/power


- Geometric


- Harmonic


- Heinz


- Lehmer



- Average absolute deviation


- Coefficient of variation


- Interquartile range


- Percentile


- Range


- Standard deviation


- Variance



- Central limit theorem


- Moments Kurtosis L-moments Skewness


- Kurtosis


- L-moments


- Skewness



- Kurtosis


- L-moments


- Skewness



- Index of dispersion



- Contingency table


- Frequency distribution


- Grouped data



- Partial correlation


- Pearson product-moment correlation


- Rank correlation Kendall's τ Spearman's ρ


- Kendall's τ


- Spearman's ρ


- Scatter plot



- Kendall's τ


- Spearman's ρ



- Bar chart


- Biplot


- Box plot


- Control chart


- Correlogram


- Fan chart


- Forest plot


- Histogram


- Pie chart


- Q–Q plot


- Radar chart


- Run chart


- Scatter plot


- Stem-and-leaf display


- Violin plot



- Effect size


- Missing data


- Optimal design


- Population


- Replication


- Sample size determination


- Statistic


- Statistical power



- Sampling Cluster Stratified


- Cluster


- Stratified


- Opinion poll


- Questionnaire


- Standard error



- Cluster


- Stratified



- Blocking


- Factorial experiment


- Interaction


- Random assignment


- Randomized controlled trial


- Randomized experiment


- Scientific control



- Adaptive clinical trial


- Stochastic approximation


- Up-and-down designs



- Cohort study


- Cross-sectional study


- Natural experiment


- Quasi-experiment



- Population


- Statistic


- Probability distribution


- Sampling distribution Order statistic


- Order statistic


- Empirical distribution Density estimation


- Density estimation


- Statistical model Model specification Lp space


- Model specification


- Lp space


- Parameter location scale shape


- location


- scale


- shape


- Parametric family Likelihood (monotone) Location–scale family Exponential
family


- Likelihood (monotone)


- Location–scale family


- Exponential family


- Completeness


- Sufficiency


- Statistical functional Bootstrap U V


- Bootstrap


- U


- V


- Optimal decision loss function


- loss function


- Efficiency


- Statistical distance divergence


- divergence


- Asymptotics


- Robustness



- Order statistic



- Density estimation



- Model specification


- Lp space



- location


- scale


- shape



- Likelihood (monotone)


- Location–scale family


- Exponential family



- Bootstrap


- U


- V



- loss function



- divergence



- Estimating equations Maximum likelihood Method of moments M-estimator Minimum
distance


- Maximum likelihood


- Method of moments


- M-estimator


- Minimum distance


- Unbiased estimators Mean-unbiased minimum-variance Rao–Blackwellization
Lehmann–Scheffé theorem Median unbiased


- Mean-unbiased minimum-variance Rao–Blackwellization Lehmann–Scheffé theorem


- Rao–Blackwellization


- Lehmann–Scheffé theorem


- Median unbiased


- Plug-in



- Maximum likelihood


- Method of moments


- M-estimator


- Minimum distance



- Mean-unbiased minimum-variance Rao–Blackwellization Lehmann–Scheffé theorem


- Rao–Blackwellization


- Lehmann–Scheffé theorem


- Median unbiased



- Rao–Blackwellization


- Lehmann–Scheffé theorem



- Confidence interval


- Pivot


- Likelihood interval


- Prediction interval


- Tolerance interval


- Resampling Bootstrap Jackknife


- Bootstrap


- Jackknife



- Bootstrap


- Jackknife



- 1- & 2-tails


- Power Uniformly most powerful test


- Uniformly most powerful test


- Permutation test Randomization test


- Randomization test


- Multiple comparisons



- Uniformly most powerful test



- Randomization test



- Likelihood-ratio


- Score/Lagrange multiplier


- Wald



- Z-test (normal)


- Student's t-test


- F-test



- Chi-squared


- G-test


- Kolmogorov–Smirnov


- Anderson–Darling


- Lilliefors


- Jarque–Bera


- Normality (Shapiro–Wilk)


- Likelihood-ratio test


- Model selection Cross validation AIC BIC


- Cross validation


- AIC


- BIC



- Cross validation


- AIC


- BIC



- Sign Sample median


- Sample median


- Signed rank (Wilcoxon) Hodges–Lehmann estimator


- Hodges–Lehmann estimator


- Rank sum (Mann–Whitney)


- Nonparametric anova 1-way (Kruskal–Wallis) 2-way (Friedman) Ordered
alternative (Jonckheere–Terpstra)


- 1-way (Kruskal–Wallis)


- 2-way (Friedman)


- Ordered alternative (Jonckheere–Terpstra)


- Van der Waerden test



- Sample median



- Hodges–Lehmann estimator



- 1-way (Kruskal–Wallis)


- 2-way (Friedman)


- Ordered alternative (Jonckheere–Terpstra)



- Bayesian probability prior posterior


- prior


- posterior


- Credible interval


- Bayes factor


- Bayesian estimator Maximum posterior estimator


- Maximum posterior estimator



- prior


- posterior



- Maximum posterior estimator



- Correlation


- Regression analysis



- Pearson product-moment


- Partial correlation


- Confounding variable


- Coefficient of determination



- Errors and residuals


- Regression validation


- Mixed effects models


- Simultaneous equations models


- Multivariate adaptive regression splines (MARS)



- Simple linear regression


- Ordinary least squares


- General linear model


- Bayesian regression



- Nonlinear regression


- Nonparametric


- Semiparametric


- Isotonic


- Robust


- Heteroscedasticity


- Homoscedasticity



- Exponential families


- Logistic (Bernoulli) / Binomial / Poisson regressions



- Analysis of variance (ANOVA, anova)


- Analysis of covariance


- Multivariate ANOVA


- Degrees of freedom



- Cohen's kappa


- Contingency table


- Graphical model


- Log-linear model


- McNemar's test


- Cochran–Mantel–Haenszel statistics



- Regression


- Manova


- Principal components


- Canonical correlation


- Discriminant analysis


- Cluster analysis


- Classification


- Structural equation model Factor analysis


- Factor analysis


- Multivariate distributions Elliptical distributions Normal


- Elliptical distributions Normal


- Normal



- Factor analysis



- Elliptical distributions Normal


- Normal



- Normal



- Decomposition


- Trend


- Stationarity


- Seasonal adjustment


- Exponential smoothing


- Cointegration


- Structural break


- Granger causality



- Dickey–Fuller


- Johansen


- Q-statistic (Ljung–Box)


- Durbin–Watson


- Breusch–Godfrey



- Autocorrelation (ACF) partial (PACF)


- partial (PACF)


- Cross-correlation (XCF)


- ARMA model


- ARIMA model (Box–Jenkins)


- Autoregressive conditional heteroskedasticity (ARCH)


- Vector autoregression (VAR)



- partial (PACF)



- Spectral density estimation


- Fourier analysis


- Least-squares spectral analysis


- Wavelet


- Whittle likelihood



- Kaplan–Meier estimator (product limit)


- Proportional hazards models


- Accelerated failure time (AFT) model


- First hitting time



- Nelson–Aalen estimator



- Log-rank test



- Bioinformatics


- Clinical trials / studies


- Epidemiology


- Medical statistics



- Chemometrics


- Methods engineering


- Probabilistic design


- Process / quality control


- Reliability


- System identification



- Actuarial science


- Census


- Crime statistics


- Demography


- Econometrics


- Jurimetrics


- National accounts


- Official statistics


- Population statistics


- Psychometrics



- Cartography


- Environmental statistics


- Geographic information system


- Geostatistics


- Kriging



- Category


- Mathematics portal


- Commons


- WikiProject



- France (data)


- Germany


- Israel


- United States


- Japan


- Czech Republic



- Probability distributions


- Mathematical and quantitative methods (economics)



- CS1 maint: others


- Articles with short description


- Short description is different from Wikidata


- Wikipedia introduction cleanup from November 2022


- All pages needing cleanup


- Articles covered by WikiProject Wikify from November 2022


- All articles covered by WikiProject Wikify


- Wikipedia articles needing clarification from May 2022


- All articles with unsourced statements


- Articles with unsourced statements from May 2022


- Articles with excerpts


- Commons link is defined as the pagename


- Articles with BNF identifiers


- Articles with GND identifiers


- Articles with J9U identifiers


- Articles with LCCN identifiers


- Articles with NDL identifiers


- Articles with NKC identifiers



- Not logged in


- Talk


- Contributions


- Create account


- Log in



- Article


- Talk



- 

- Read


- Edit


- View history



- 

- Main page


- Contents


- Current events


- Random article


- About Wikipedia


- Contact us


- Donate



- Help


- Learn to edit


- Community portal


- Recent changes


- Upload file



- What links here


- Related changes


- Upload file


- Special pages


- Permanent link


- Page information


- Cite this page


- Wikidata item



- Download as PDF


- Printable version



- Wikimedia Commons



- العربية


- Asturianu


- বাংলা


- Беларуская


- Български


- Català


- Чӑвашла


- Čeština


- Cymraeg


- Deutsch


- Eesti


- Ελληνικά


- Español


- Esperanto


- Euskara


- فارسی


- Français


- Galego


- 한국어


- Հայերեն


- हिन्दी


- Bahasa Indonesia


- Italiano


- עברית


- ქართული


- Latina


- Lietuvių


- Magyar


- Македонски


- Bahasa Melayu


- Nederlands


- 日本語


- Norsk bokmål


- Norsk nynorsk


- Polski


- Português


- Română


- Русский


- සිංහල


- Simple English


- Slovenščina


- Српски / srpski


- Sunda


- Suomi


- Svenska


- Tagalog


- தமிழ்


- ไทย


- Türkçe


- Українська


- اردو


- Tiếng Việt


- 吴语


- 粵語


- 中文



- This page was last edited on 16 December 2022, at 19:20 (UTC).


- Text is available under the Creative Commons Attribution-ShareAlike License
3.0; additional terms may apply. By using this site, you agree to the Terms of
Use and Privacy Policy. Wikipedia® is a registered trademark of the Wikimedia
Foundation, Inc., a non-profit organization.



- Privacy policy


- About Wikipedia


- Disclaimers


- Contact Wikipedia


- Mobile view


- Developers


- Statistics


- Cookie statement



- 


- 




