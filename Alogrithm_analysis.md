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
                                           
