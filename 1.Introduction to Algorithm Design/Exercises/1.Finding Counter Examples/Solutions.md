### 1-1) Show that a + b can be less than min(a,b)
In a scenario where the __a__ and __b__ are always less than 0, then this case is valid.  
**Example:**  
a = -1 and b = -4  ,   
a + b = -(1+4) = -5  
min(a,b) = min(-1, -4) = -4

-5 < -4 Hence Proved

### 1-2) Show that a * b can be less than min(a,b)
In a scenario where the __a__ and __b__ are one positive and one negative numbers, then this case is valid.  
**Example:**  
a = -1 and b = 4  ,   
a * b = -1 * 4 = -4  
min(a,b) = min(-1, 4) = -1

-4 < -1 Hence Proved

 ### 1-3) Design/draw a road network with two points and such that the fastest route between and is not the shortest route.
This can only happen if the time taken to travel a road depends on more than just its length.  
Here there are 2 roads, where in 1 mile road the speed limit is __1 mile/hr__ and on the 2 mile road the __4 mile/hr__  

By the formulae Speed = Distance / Time  
We can find that the   
1 mile road takes **1hr** to complete the journey  
2 mile road takes **30 min** to complete the journey

Hence 2mile road is the solution
![soln](https://github.com/vamsimadhav/Algorithm-Design-Manual/blob/main/1.Introduction%20to%20Algorithm%20Design/Exercises/1.Finding%20Counter%20Examples/Supporting%20Resources/1-3.jpeg?raw=true)

 ### 1-4) Design / draw a road network with two points and such that the shortest route between and is not the route with the fewest turns.  
Suppose a = (0,0) and b = (0,10) .  
Let Route 1 go up to (0,100), right to (10,100), and back down to (0,10).  
So Route 1 has length 210 and has 3 turns (assuming you were originally facing right).  
Let Route 2 go up to (0,1), right to (1,1), down to (1, -1), right to (2,-1), up to (2,0), and right to (10,0).  
So Route 2 has length 14 and has 6 turns.  
Therefore Route 2 is shorter, but has more turns than Route 1.

### 1-5)  The knapsack problem is as follows: given a set of integers S = {s1, s2 ... sn}, and a target number T, find a subset of which adds up exactly to.  
#### Find counterexamples to each of the following algorithms for the knapsack problem.That is, giving an and such that the subset is selected using the algorithm does not leave the knapsack completely full, even though such a solution exists.
* Put the elements of in the knapsack in left to right order if they fit, i.e. the first-fit algorithm.
* Put the elements of in the knapsack from smallest to largest, i.e. the best-fit algorithm.
* Put the elements of in the knapsack from largest to smallest.
  ![Soln](https://github.com/vamsimadhav/Algorithm-Design-Manual/blob/main/1.Introduction%20to%20Algorithm%20Design/Exercises/1.Finding%20Counter%20Examples/Supporting%20Resources/1-5.png?raw=true)


#### 1-6) ![Question 1-6](https://github.com/vamsimadhav/Algorithm-Design-Manual/blob/main/1.Introduction%20to%20Algorithm%20Design/Exercises/1.Finding%20Counter%20Examples/Supporting%20Resources/1-6q.png?raw=true)  
Let **U = {1, 2, 3, 4, 5, 6}**  
Let S1 = {1,2,3}, S2 = {2,4}, S3 = {1,4}, S4 = {2,5}, S5 = {5}, S6 = {6}, S7 = {3,6}, S8 = {4}

As it is mentioned that the largest should be subset should be selected and remove them from U.  
We can Choose S1 + S8 + S5 + S6  -> 4 subsets

But we can choose S2 + S3 + S7 -> 3 subsets  
Therefore the algorithm failed to select the correct output, and so is incorrect.
