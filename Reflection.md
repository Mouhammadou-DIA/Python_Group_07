# Python_Group_07

# Reflection

## Who did what

- Mouhammadou DIA :

In my version of the code, newton_sqrt and bisection_sqrt calculate the
square root and count the steps. When I tested newton_sqrt(-1), the program
crashed: x became 0 after the first step, so a/x gave a division by zero.
I fixed it with try / except, which prints a message
instead of crashing. I also tested newton_cbrt(27) for the cube root.


- Princilia DACI :
- Josué OMOLOHOSO :
- Aby BA :
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
