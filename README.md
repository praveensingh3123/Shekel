# Shekel - Cash Settlement App

<h2> Try it for yourself: https://praveensingh3123.github.io/Shekel/ </h2>

# Welcome to Shekel!  

The idea is to use Shortest path algorithm where at every step, settle all amounts of one person and recur for remaining n-1 persons.  

  
# Getting Started  
  
For example, if the following weighted directed graph represents some people and the arrows represent debts between them (Praveen owes Dhriti Rs. 20 and Samir Rs. 5, Dhriti owes Samir Rs. 10, etc.):

How to pick the first person? To pick the first person, calculate the net amount for every person where net amount is obtained by subtracting all debts (amounts to pay) from all credits (amounts to be paid). Once net amount for every person is evaluated, find two persons with maximum and minimum net amounts. These two persons are the most creditors and debtors. The person with minimum of two is our first person to be settled and removed from list. Let the minimum of two amounts be x. We pay ‘x’ amount from the maximum debtor to maximum creditor and settle one person. If x is equal to the maximum debit, then maximum debtor is settled, else maximum creditor is settled.

![Problem Statement](https://raw.githubusercontent.com/praveensingh3123/Shekel/main/Graph.jpg)

There's no sense in Rs. 10 making its way from Praveen to Dhriti and then from Dhriti to Samir if Praveen could just give it to Samir directly.

The goal, then, in the general case is to take a debt graph and simplify it (i.e. produce a new graph with the same nodes but different edges).

