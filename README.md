# Project 7: Square Roots with Newton and Bisection

## What our program does

Our program finds the square root of a number with two methods, Newton and bisection. Both start with a guess and make it better again and again, until the guess is close enough. Each function gives back the answer and the number of steps it needed, so we can see which method is faster.

Not knowing what the user will want to enter in the calculator, we used a function `convert` to first convert what the user enters. So the user can give a number, but also a number written as text, like `"3"` or `"-0.25"`. And if what is entered is not a number at all, the user gets a message instead of an error.

### How the code works

#### convert

\- If it is already a number (`int` or `float`), we give it back as it is.

\- If it is not a number and not a text either, we return `"This is not a number!"`.

\- If it is a text, we remove the spaces with `strip()`. If there is a `"-"` at the start, we keep it aside in `sign` and remove it.

\- If what is left is only digits, it is a whole number, so we return `sign*int(a)`.

\- If there is one point, we cut the text in two with `split(".")`, then we put the two parts back together: the decimal part is divided by 10 to the power of its number of digits. For example `"3.25"` gives 3 + 25/100 = 3.25.

\- If none of this works, we return `"This is not a number!"`.

#### newton_sqrt and bisection_sqrt

Both start the same way: we call `convert`, and if the result is not a number, we stop and give back the message. Then there are three cases:

\- if a is negative, we stop, the square root does not exist;

\- if a is 0, we give back (0, 0), no need to compute anything;

\- if a is positive, we go in the loop and count each turn.

The difference is in the loop:

\- **Newton:** we start with x = a and repeat x = (x + a/x) / 2 until x\*x is very close to a.

\- **Bisection:** we keep the root between `low` and `high`. At each step we take the middle `mid`. If mid\*mid is smaller than a, then `low = mid`, if not, `high = mid`. We stop when low and high are almost the same. When a is smaller than 1, we start with `high = 1`, because the root is bigger than a (the root of 0.25 is 0.5).

### Extra: cube root

For the cube root we want x such that x\*x\*x = a. The function `newton_cbrt` works like `newton_sqrt`, with x = x - (x\*x\*x - a) / (3\*x\*x) in the loop. There is no case for negative numbers, because the cube root of a negative number exists.

For the error, we did not keep 0.000001 like for the square root. When we tested with 27, we got 3.000000001793672 in 9 steps, and not 3. So we added zeros one by one. With one more zero (0.0000001), nothing changed. With two more zeros (0.00000001), the code does one more step and we get exactly 3.0 in 10 steps. So we kept 0.00000001.

## Answer to question related to 

1. ### There is fewer steps for Newton method. It has 4 steps for a=3.
2. ### We have this :

#### First Step : 1 correct digit

#### Second Step : 3 correct digits

#### Third Step : 6 correct digits

#### Fourth Step : 9 correct digits

#### We see that more steps are convergent to the right value of square root of 2.


## Example results

### Example 1: a negative number,a=-4

\- `-4` is already a number, so `convert` keeps it.

\- It is negative, so the function stops here. The loop never starts.

```python
print(newton_sqrt(-4))
# The square root of -4 doesn't exist
```

### Example 2: zero,a=0

\- `0` is already a number, so `convert` keeps it.

\- It is not negative, but it is equal to 0, so the function gives back (0, 0) without going in the loop.

```python
print(newton_sqrt(0))
# (0, 0)
```

### Example 3: a number given as text, a="0.25"

\- `"0.25"` is a text. There is no space and no minus sign.

\- It is not only digits because of the point, so `convert` cuts it into `"0"` and `"25"` and puts them back together: 0 + 25/100 = 0.25.

\- 0.25 is not negative and not 0, so we go in the loop with x = 0.25.

\- x becomes 0.625, then 0.5125, then 0.5001524, then 0.5000000232. Now x\*x is close enough to 0.25, so it stops after 4 turns.

```python
print(newton_sqrt("0.25"))
# (0.50000002, 4)
```
