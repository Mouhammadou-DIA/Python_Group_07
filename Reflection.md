# Python_Group_07

# Reflection

## Who did what



- Aby BA :

In my code, I used two methods to calculate the square root of a number: Newton’s method and the bisection method. I added a counter to track the number of steps taken by each method. Both methods provide an approximation of the square root.


- Princilia DASSI :

I first wrote my own complete version of the code. In it, I added the function convert, because we don't know what the user will type: it first turns the input into a number, keeps the minus sign aside, and cuts at the point to rebuild decimal numbers, so "0.25" or "-4" are accepted. I also added an if condition just after convert in newton_sqrt and bisection_sqrt, so the function stops and gives back a message when the input is not a number, instead of crashing. While testing, I fixed the minus sign that was lost for decimal numbers. Then I put my version together with the ideas of the others to finalize the code we submit.


- Mouhammadou DIA :

I’m thinking more along these lines: I wrote my own version of the code, adhering to the conditions specified in the context. In particular, I had to test negative values, such as -1, which triggered a `ZeroDivisionError`; this led me to implement `try` and `except` blocks to handle such cases. Furthermore, it should be noted that for `newton_cbrt`, I had to incorporate an additional condition specific to calculating a cube root, which differed from the logic used in the initial version. Finally, I completed the "think and explain" section in the `README.md` file and included the results for $a=2$ and $a=3$ for each method.


- Josué OMOLOHOSO :

While working on my programs for the Newton method and the bisection method, I encountered a few issues. Initially, I had forgotten to include a condition to exclude negative real numbers, which triggered an error message; after discussing this with a friend who reviewed my code, I added a condition to filter out negative values, which resolved the problem. Additionally, I had used two separate "if" statements in my program, but friends in my group suggested replacing one of them with an "elif" to ensure the program wouldn't continue executing unnecessarily if the first condition wasn't met. Furthermore, for the bisection method, my program required significantly more iterations (137) to calculate the square root of 0.25 compared to my peers' results, even though the final square root value was roughly the same.


- Oumar SOW :



## Global conclusion

Each member first wrote his or her own version of the code. Then we compared
them and chose to keep Prinicilia DASSI code as the final version.
Then some modifications was made into it for having the final version.

The final README.md has two parts: the first part was written by
Prinicilia DASSI and the second part by Mouhammadou DIA.

## One bug we had and how we resolved it

The program had a bug when we tried negative values or values entered as
text. To fix it, we created a convert function that converts the input
before it is used.
