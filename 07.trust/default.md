---
title: trust
content:
    items: '@self.modular'
---

# Trust in ἀδελφός

Trust, like love, escapes a formal definition. However in adelphos trust
is measured as the quantity of money that we are willing to postpone
for a certain person or a group of people.

That is, if Alice sells a used phone to Bob for 300$ and Bob
promises Alice that he will pay Alice in a month, Alice trusts
Bob for 300$ and a month.

That is, trust is a function defined in two variables, quantity
and time.

Of course there must be a greater trust to postpone a payment of
30 days or 1 year. This is usually corrected in real life by the
use of the **interest**.

Bob promises Alice that, if she waits one year, he will pay her
310$, with a interest of 3%.

We will later see how this is implemented in adelphos, for now we
focus on the monetary aspect of trust and how we can measure it.

## Definition of trust

Trust in adelphos is defined as the amount of delayed money that
we are willing to sacrifice in the present.

The definition of trust in adelphos is this:

The different approach of adelphos can be summarized as this:
when I receive a payment by A I give trust to A, and trust is
itself related to the amount of credit that I give to the other
party.


> Example: suppose we sell a used car to our wife’s best friend,
> Lucy. The real price for a stranger should be 4,000€. Lucy tells
> us that she has only 3,500€ in her bank account. We don’t want to
> really discount the price too much, nor do we want to put the car
> in the real market because we know that she needs that car;
> another option should be that we accept a mixed payment from her.
> 3,500€ in cash and 500€ as a credit that has a certain threshold
> date, an IOU (I Owe You). The amount of IOU received (in this
> case 500/4000 = 1/8 = 12.5%) is the measure of trust between us.

In this case the system would record the IOU and the trust
between we and Lucy has got a number.

# Definition of trust.

We have seen that in Adelphos trust is measured as the amount of
credit that I am willing to get from an external party. Adelphos
does not want (at least initially) to replace the national
currency in total; we know that a certain amount of real money is
necessary in every day life and we think that people should be
gradually brought from a scarcity theory of money to a credit
based.  In a certain sense we think that people should trust
first of all the system and then they will join it, because they
see that they aren’t risking too much.

As the percentage of IOUs that a person is willing to take in
exchange for a transaction is decided when he enters the system,
it risks only that amount.


## The axiom of adelphos 

To measure trust we have thought that a logarithmic measure is
more adapt to model the way in which we trust people, that is a
double measure of trust is not equal to a double amount of
credit, but of ten times.

The main axiom in adelphos is this:

_A unit of trust equals one unit of currency exchanged._

As we have many different currencies in the world in adelphos we
simply use the Greek letter Tao (τ) as the unit of real currency.

## The human unit.

Real world currencies comes in many shapes and sizes and not in
all countries the unit of currency correspond with a meaningful
amount of money.

For example, in Italy, before the Euro, the Lira was not a real
unit, because with 1 Lira you did not buy anything. The real
currency was the Lira, but the _human unit_ was One Thousand
Lire.

In a country with hyper inflation the _human unit_ could be _one
million_ of the real currency, wheter in ancient times, for
example in England, the Pound was of too much value as a _human
unit_.

In the past years there was the Big Mac Index, that is how much a
Big Mac cost in different states.

As the Dollar is for now the global currency, and as in USA you
can buy something _usable_ for one dollar, we could say that the
_human unit_ is more or less equivalent to one dollar (or one
Euro which is almost equal in value).

We will use the human unit of currency to compute the trust as an
adimensional value.

## The trust-bel, unit of measure of trust

We measure the trust as the logarith in base 10 of the amount of
currency which we are willing to postpone, divided by the amount
of ``human value'', TaoHV, times 10.

And we call this scalar the trust-bel:

In formula:

> trust-bel = 10 * log ( Tao / TaoHV)


Let's do two examples with two different scenarios.

In USA Alice is willing to lend Bob 100$, in USA the human value
of currency is 1$, so we have that the trust if Alice towards Bob
is

> trust-bel(Alice-Bob) = 10 * log ( 100$ / 1$ ) = 10 * log (100)
> = 10 * 2 = 20 tb
>

So Alice trusts Bob 20tb.

Second Example: we are in Italy, before the Euro. Anna is willing
to lend Bruno 1,000,000 Lire. It seems a lot, but in reality it
was only 500Euro. In Italy we could say that at the time the
``human value'' of the Lira was 1,000 because with one thousand
Lira you bought something valuable (for example a coffee).

So we can compute the trust between Anna and Bruno

> trust-bel(Anna-Bruno) = 10 * log (1,000,000 Lira / 1.000 Lira)
> = 10 log (1,000) = 30 tb

So Anna trusts Bruno 30tb

You can see from the two examples that the trust has raised of 10
units but the amount of money has raised more or less 5 times,
from 100$ to 500 Euros.

## Trust in adelphos.

This measure of trusts will be used in all adelphos where the
Human Value, for now, is simply the averaged Exchange rate
between the Dollar and the Currency (we do not need the exact
value, just a rough one).

For example we will use 100Yen as the Human Value for Yen because
the Dollar is more or less one hundred times more valuable.
