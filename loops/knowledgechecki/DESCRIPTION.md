# Knowledge Check I

This challenge is going to test your python knowledge up to this point!

# Challenge 

In this challenge you will write a program to calculate the *hailstone number* of a user supplied integer. This challenge will apply the [collatz conjecture](https://www.geeksforgeeks.org/dsa/hailstone-numbers/). This sounds scary, but it is rather simple. 

The *collatz conjecture* states that any given number (N) will eventually become 1 given the following calculations:
- If N is even, we divide it by two, and that becomes our new N.
- If N is odd, we do the formula 3N + 1, and that becomes our new N.

We repeat this as many times as we need for N to equal 1. The hailstone number is how many calculations it takes to get from our starting N, to 1. 

## Example

If you were to start with N = 8. Then the following sequence would happen:

8 / 2 = 4
4 / 2 = 2
2 / 2 = 1

So, including our starting number of 8, the hailstone number would be 4. Since N was 8 -> 4 -> 2 -> 1 (4 numbers in total). 

This challenge will require you to use conditionals, loops, and if statements to finish!

Your code must do 2 things:
1. Take in one number from the user.
2. Calculate the hailstone number and print out ONLY the number.

To test your code, run `verify <your_python_file.py>`, and get the flag!
