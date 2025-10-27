---
title: 'relationships in adelphos'
---

# Relationships in adelphos

In adelphos we have two basic relationships between users: the warrant and the
trust, one implies the other, but not viceversa.


## Warrant


In adelphos, if Alice warrants Bob for 100$ it means that Alice not only trusts
Bob but that she is willing to pay his debts up until 100$.

It is a **public** statement, and this is the basis of the routing of the
credit in adelphos. Alice is willing to do that because she gains a price for
this service, as we will see later.

In a graph the warrant is drawn by a thick line from Alice to Bob.

## Trust


Instead if Alice trusts Bob for 100$ it means that Alice is willing to accept a
cheque signed by Bob up until 100$ and that she won't claim to anybody if Bob
does not pay it on its due date.

This is a **private** statement. Alice tells it to the system but the other
users do not need to see it. Adelphos will use this information to compute a
route for the money between two users.

In a graph the trust is drawn by a dashed line from Alice to Bob.


## Example of routing.

The routing of the money goes is this way.

Suppose that Alice wants to send to John 100$ due in 6 months.


Suppose that we have a graph in whih

Bob warrants Alice for 200$, Charles warrants Bob for 200$ and John trusts Charles for 200$


The system does this algorithm in pseudocode, it is a recursive descent in the graph

    start_node := Alice
    end_node := John
    trust_set := compute the set of all people $end_node trusts
    amount := 200$

    if (trust_set empty)
        /* if trust set is empty there is no point in searching */
        return false
    

    boolean res = find_route(start node, amount, trust_set);
    return res;

    where find_route is this recursive function.


    function find_route(start_node, amount, trust_set): boolean
    begin

        if (start_node is in trust_set) begin
            /* found !*/
            return true;
        end

        /* the start node is not in the trust set, so
        let's search in all the peobple who warrant $start_node*/


        set_warrant = compute set of people who warrant $start_node

        foreach ( $warranter in $set_warrant) begin

            /* recursive call */
            res := find_route($warranter, $amount, $trust_set);

            if res == true
                return true; /* found */

        end

        /* not found */
        return false;


    end;



As you can see the money can go from point A to point B __only__ if there is a warrant path
between the two points and only in the last step a simple trust is sufficient.

Let's see the situation after this transfer.

After this transfer from Alice to John, John has 200$ signed by Bob and by
Charles, whom he trusts.

At the end of the due period, John asks the 200$ from Charles.

Charles gives them to John, and receives the cheque.

But he has warranted Bob, so he asks them to Bob, and Bob asks them to Alice where
the cheque gets destroyed because Alice has filled her debt.


In this case we have not shown the gains that John and Charles get from this
service, but it should be straightforward, simply Alice will give a cheque not
of 200, but of 205$ (say), to Bob, Bob gives a cheque of 203$ to Charles who
will give a cheque of 200$ to Bob.

At the end of the period, Charles will refund 200 to John, but he will be refunded
203 from Bob, who will be refunded 205 from Alice.

Alice will have spent 205$, Charles will have gained 3$, Bob 2$ and John will have
received 200$, as he requested.

This transfer has been done without using a bank in between, but only using the
trust between people.
