# CMPS 2200 Assignment 5
## Answers

**Name:** Devin Gutierrez


Place all written answers from `assignment-05.md` here for easier grading.





- **1a.**

def make_change(n):
    """
    Given number n in dollars, returns the min num of coins in Geometrica currency which sum to n
    """
    denominations = **[2**k for k in range(32)]  # 32 is an upper bound on the number of coins needed for any value of n
    denominations.reverse()  # start with largest first
    coins = []
    for d in denominations:
        while n >= d:
            coins.append(d)
            n -= d
    return coins**

Algorithm produces the optimal (minimum) amount of coins needed given N dollars.

- **1b.**

W(n) = O(logN)
S(n) = O(logN)



- **2a.**

Using this example: We have the following denominations: {1, 3, 4} and  want to make change for $6. 
The greedy algorithm would first choose 4, leaving us with 2 dollars to make change for. Then, the algorithm would choose two 1's to make the total of 6 dollars. This results in a total of 3 coins.

However, it would be more optimal if we  make change for 6 dollars using just two coins: two 3's.

The reason why the greedy algorithm fails is that it always chooses the largest denomination that is less than or equal to the remaining amount to make change for. But in Fortuito, this may not necessarily be the best choice in terms of producing the fewest number of coins. There may be a combination of smaller denominations that sum up to the same amount with fewer coins. Therefore, in general, we cannot rely on the greedy algorithm to produce the optimal solution in Fortuito. Instead, we need to use a different approach, such as dynamic programming, to find the minimum number of coins needed to make change for a given amount.

- **2b.**

k = # of denominations
n = dollar amount

Therefore, Work: W(n) = O(nk); Span: S(n): O(n)



