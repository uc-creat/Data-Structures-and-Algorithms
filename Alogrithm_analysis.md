# Need to analyse an algorithm:
The basic reason to analyse any algorithm, is mainly to check which algorithm is faster and which one is slower. Most of the time we need such algorithm which takes minimum
amount of time for execution. But we cannot compare any code/algorithm, just by running the code on pc/any hardware. To understand this point in a better way, let us consider an example:

Person A have a supercomputer, while Person B have an ordinary computer. If we run the a slower algorithm on supercomputer and faster algorithm on normal computer, still supercomputer will execute the algorithm way earlier than that of normal computer. Now by just comparing the two algorithm on the basis of the execution time taken by the two different computers, one cannot decide out of the two algorithms, which one is faster. The systems on which we are running the code must be exactly same for conducting such experiment. 
So, in order to avoid such tedious task, there are two ways through which we can easily compare any algorithm, regardless of which hardware we are using. This because, for this type of analysis, we donot consider the hardware part, we only look and analyse the code-part. 
The two ways are -
* Time Complexity
* Space Complexity

## Time Complexity:
Time complexity in simple words is that - how much time will a code take for execution.
* Point to remember:

    Statements which take constant time of execution are -
    1. Declaration
    1. Assignment
    1. Comparison
    1. Arithmetic operations
    1. Calling of a function
    1. Accessing of a function
    1. Returning of a function


Eg:
```py
int x = 0  # int x --> declaration statement -- taking constant amount of time = 1, x = 0 --> assignment operation -- constant time = 1, total time = 2
int y = 1  # int y --> declaration statement -- taking constant amount of time = 1, y = 1 --> assignment operation -- constant time = 1, total time = 2  
while(y <= n):  # Comparsion -- (y<=n), but this comparison takes place until y>n, therefore it runs (n+1) times
   x += 1  # arithmetic operation -- as each arithmetic operation takes constant amount of time = 1, and it will run for n times, therefore time taken = n*1 = n
   y += 1  # arithmetic operation -- as each arithmetic operation takes constant amount of time = 1, and it will run for n times, therefore time taken = n*1 = n
   
# Total time = ( 2 + 2 + n + n + (n+1)) = (3n + 5)
```

## Order of Growth:
* Constant                                
* log(n)                                  
* Linear - (n)                           
* nlog(n)                                   
* quadratic - (n^2)                      
* cubic - (n^3)                           
* exponential - (c^n), where c = constant     

## Asymtotic Notations:
The main idea of asymptotic analysis is to have a measure of efficiency of algorithms that doesn’t depend on machine specific constants, and doesn’t require algorithms to be implemented and time taken by programs to be compared.
There can be 3 possible cases for any algorithm - 

1. Best Case    --->  minimum amount of time taken for execution
1. Average Case --->  Average amount of time taken for execution
1. Worst Case   --->  maximum amount of time taken for execution
These 3 case can be represented in terms of notations called, Asymtotic Notations. So there are 3 main notations - 

### Big Ω - Notation: (Best Case)
 


![](https://media.geeksforgeeks.org/wp-content/uploads/AlgoAnalysis-3.png)



**Ω(g(n)) = { f(n): there exist positive constants c and n0 such that 0 ≤ cg(n) ≤ f(n) for all n ≥ n0 }**
   
   
Terms to understand:
n0 - n0 is that point after which g(n) <= f(n). 
n0 >= 1, this because any input atleast requires a minimum of time = 1.

There are two functions depicted in the graph, g(n) and f(n). We can also write cg(n), where c = constant > 0 .
Big - Ω is way through which we can find the best case / the lower bound of f(n).
Consider the above picture, after n0, g(n) < f(n), which means that, after certain point n0, g(n) is always < f(n) and for any value of c we cannot exceed the 
the value of f(n). But we can get any value below that. For eg:
   
   consider f(n) = 5n + 4 
    Therfore, according to Big - Ω notation, f(n) >= g(n)
    =>  5n + 4 >= cn
        here one such value for c = 1, such that -->  5n + 4 >= n, similarly there can be many such values for c like = 2, 3 ,4 .. until it satisfies
        the condition of f(n) >= g(n).

This means that the maximum value of g(n) after n0 can be of the order 'n' , although below this order all other order like log(n) can be accepted but we look for the closest
possible value/order. This implies that, Ω(n) is the the best case possible for f(n) when compared with the function g(n).
Here, it measures the best amount of time an algorithm can take to complete an execution
Therefore, Big - Ω acts as a lower bound for an algorithm, as it calculates the minimum amount of time that an algorithm can take.
We consider the closest possible order because, then we can confidently say that, above this order the algorithm cannot exceed, i.e. this is the best possible order
for which an algorithm can run/ this is the lower bound of the algorithm and it cannot take execution time which is above this order, for the best case possible.

*NOTE: There can be many orders which satisfies the condition f(n)>=g(n), but the closest order is to be considered. *


### Big O - Notation: (Worst Case)

   ![](https://media.geeksforgeeks.org/wp-content/uploads/AlgoAnalysis-2.png)


**O(g(n)) = { f(n): there exist positive constants c and n0 such that 0 ≤ f(n) ≤ cg(n) for all n ≥ n0 }**


Similar to the Big - Ω, there are two functions, cg(n) and f(n) along with a point n0, after which f(n) >= g(n).
Big - O says that, after the intersection point n0, f(n), cannot exceed the order of cg(n). 
There can be any order of f(n) until and unless it is lesser than that of g(n), after n0. But the closest order is to be considered.
For eg:
if f(n) = 5n + 4, then cg(n) can be of order -- n, n^2, n^3... but the closest order to the given function is of the order n, therefore it is considered.
This means that, atleast order of n is required for the execution of the given function.
Because it bounds the upper condition, therefore it is also called as upper bound of f(n) or the worst, as in the worst condition possible, the 
given algorithm will take an order of n to complete the execution.


### Θ - Notation: (Average Case)

  
   ![](https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcRksnIUnxFeSADh2ZsfsaiFN56a4HZ_LVy1gw&usqp=CAU)
   
   
**Θ(g(n)) = { f(n): there exist positive constants c1, c2 and n0 such that 0 ≤ c1g(n) ≤ f(n) ≤ c2g(n) for all n ≥ n0 }**


It basically encloses the function from above and below. Since it represents the upper and the lower bound of the running time of an algorithm, it is used for analyzing the average case complexity of an algorithm.


---
---

There are two more asymtotic notations - 
1. **Little O**
1. **Little Ω** 

![](https://media.geeksforgeeks.org/wp-content/uploads/Analysis-of-Algorithms-little-o-omega.png)

In the case of little O, cg(n) > f(n), which means that cg(n) is strickty greater than f(n), while in the case of little - Ω , cg(n) < f(n) whic implies
that cg(n) is stricktly smaller than f(n).
Equalilty sign is removed in case of littel O and little Ω .

For eg:
if f(n) = 2(n^2) + n, then possible outcomes of cg(n) for little O can be ---> n^3, n^4... but not n^2
similarly if we consider the same eg as for little Ω , possible outcomes for cg(n) can be ---> n, log(n).. but not n^2.

---
---

## NOTE:

Generally we use Big - O, for algorithm analysis, as we are interested in finding the worst case an algorithm can run for a given condition.
By finding out Big - O of any algorithm, we can get an idea of -- as maximum of how much time can an algorithm take for execution. 
