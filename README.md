Credit Card Validator
    1.  Summary - Validate a credit card number using standard Luhn Algorithm
    Description – Credit card numbers can be validated using an industry-standard algorithm
    called the Luhn Checksum:
    From the rightmost digit (the check digit), double the value of every second digit. The check digit is not doubled; the first digit doubled is immediately to the left of the check digit.
    If the result of this doubling operation is greater than 9 (e.g., 8 × 2 = 16), then subtract 9 from the product (e.g., 16: 16 − 9 = 7, 18: 18 − 9 = 9).
    Take the sum of all the digits from step 1, both doubled and natural.
    If the total modulo 10 is equal to 0 (if the total ends in zero) then the number is valid according to the Luhn formula; otherwise it is not valid.
    See the attachment tab for an example of account number "7992739871x". The sum of all the digits in the third row is 67+x. If x = 3, then the modulo of 10 = 0, which means the credit card number is valid.
    Write a program that will validate credit card numbers using this algorithm and indicate the result.
Example:
1. Input: A single line of input containing a potential credit card number.
2. Output: True if the credit card number is valid False if the credit card number is not valid.

Reverse and Add
    2. Summary - Continually add a number to its reverse to arrive at a palindrome
    Description - Credits: Programming Challenges by Steven S. Skiena and Miguel A. Revilla
    The problem is as follows: choose a number, reverse its digits and add it to the original. If the sum is not a palindrome (which means, it is not the same number from left to right and right to left), repeat this procedure. eg.
    195 (initial number) + 591 (reverse of initial number) = 786 786 + 687 = 1473
    1473 + 3741 = 5214
    5214 + 4125 = 9339 (palindrome)
    In this particular case the palindrome 9339 appeared after the 4th addition.
    This method leads to palindromes in a few step for almost all of the integers. But there are interesting exceptions. 196 is the first number for which no palindrome has been found.
    t is not proven though, that there is no such a palindrome.
Example:
1. Input - Your program should read lines of text from standard input. Each line will contain an integer n < 4,294,967,295.
Assume each line of input will always have an answer and that it is computable with less than 1000 iterations (additions).
2. Output - For each line of input, generate a line of output which is the number of iterations 