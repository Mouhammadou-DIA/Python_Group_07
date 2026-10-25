# Python_Group_07

# Reflection

## Who did what



- Aby BA :

In my code, I used two methods to calculate the square root of a number: Newton’s method and the bisection method. I added a counter to track the number of steps taken by each method. Both methods provide an approximation of the square root.


- Princilia DACI :

I first wrote my own complete version of the code. In it, I added the function convert, because we don't know what the user will type: it first turns the input into a number, keeps the minus sign aside, and cuts at the point to rebuild decimal numbers, so "0.25" or "-4" are accepted. I also added an if condition just after convert in newton_sqrt and bisection_sqrt, so the function stops and gives back a message when the input is not a number, instead of crashing. While testing, I fixed the minus sign that was lost for decimal numbers. Then I put my version together with the ideas of the others to finalize the code we submit.


- Mouhammadou DIA :

I’m thinking more along these lines: I wrote my own version of the code, adhering to the conditions specified in the context. In particular, I had to test negative values, such as -1, which triggered a `ZeroDivisionError`; this led me to implement `try` and `except` blocks to handle such cases. Furthermore, it should be noted that for `newton_cbrt`, I had to incorporate an additional condition specific to calculating a cube root, which differed from the logic used in the initial version. Finally, I completed the "think and explain" section in the `README.md` file and included the results for $a=2$ and $a=3$ for each method.


- Josué OMOLOHOSO :

Our project involved each of us working on our own computers and then discussing and comparing our results with the others. In my programs for the Newton method and the bisection method, I ran into a few problems: First, I had initially forgotten to include a condition to exclude negative real numbers (since they have no real square roots), and I got an error message—but I didn’t want an error message; I wanted a message like “no square root for this real number.” I eventually managed to fix it so it worked the way I wanted. Then I had included two “if” statements in my program, and I got a suggestion from my friends in the group who recommended replacing one “if” with an “elif” to prevent the program from continuing to run even when the first condition wasn’t met. As for the bisection algorithm, I obtained many more iterations (137) for the square root of 0.25 than my other friends, but with roughly the same square root value; however, for all other values, we had the same number of steps and the same square root values. This experience was very rewarding for me, as it helped me improve how I write programs that use functions.


- Oumar SOW :
I wrote two Python functions to calculate the square root of a number: Newton’s method and the bisection method.I had forgotten to handle the case where (a=0), which caused an error instead of returning 0. I fixed this by adding a specific condition and also handled negative numbers. Newton’s method improves an initial guess, while bisection progressively reduces an interval until the desired precision is reached. Finally, I tested both methods and found that Newton’s method generally converges faster.
 In the extra (optional) part, I forgot to convert the initial value x = a to a float instead of keeping it as an integer. I fixed this by using x = float(a) to ensure that the calculations work correctly with decimal values. 
## Global conclusion

Each member first wrote his or her own version of the code. That helped on ensuring that each one understood the project and favorized the discussions related to the choice of the final program to go on.  Then we compared them and chose to keep Prinicilia DASSI code as the final version. Then some modifications was made into it for having the final version. The final README.md has two parts: the first part was written by Prinicilia DASSI and the second part by Mouhammadou DIA.

## One bug we had and how we resolved it

The program had a bug when we tried negative values or values entered as
text. To fix it, we created a convert function that converts the input
before it is used.
