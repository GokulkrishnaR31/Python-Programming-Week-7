# Python-Programming-Week-7
1.Abundant Number

An abundant number is a number for which the sum of its proper divisors is greater than the number itself. Proper divisors of the number are those that are strictly lesser than the number.



Input Format:

Take input an integer from stdin

Output Format:

Return Yes if given number is Abundant. Otherwise, print No



CODE:

def abundant(n):

 l=[]

 for j in range(1,n):

  if n%j==0:

   l.append(j)

 if sum(l)>n:

  return "Yes"

 else:

   return "No"
   #2.Automorphic number or not

An automorphic number is a number whose square ends with the number itself. For example, 5 is an automorphic number because 5*5 =25. The last digit is 5 which same as the given number. 



If the number is not valid, it should display “Invalid input”.

If it is an automorphic number display “Automorphic” else display “Not Automorphic”.



CODE:

def automorphic(n):

    a=n*n

    d=a%10



    if(n==d):

        return 'Automorphic' 

    else:

        return 'Not Automorphic' 

#3.Check Product of Digits

Write a code to check whether product of digits at even places is divisible by sum of digits at odd place of a positive integer.





CODE:

def productDigits(n):

    product = 1

    odd_sum = 0

    while n > 0:

        digit = n % 10

        if digit % 2 == 0:

            product *= digit

        else:

            odd_sum += digit

        n //= 10

    return product % odd_sum == 0

#4.Christmas Discount

An e-commerce company plans to give their customers a special discount for Christmas.

They are planning to offer a flat discount. The discount value is calculated as the sum of all the prime digits in the total bill amount.

Write an python code to find the discount value for the given total bill amount.

Constraints

1 <= orderValue< 10e100000

CODE:





def christmasDiscount(n):

 p=str(n)

 l=[]

 for i in range(len(p)):

  count=0

  for j in range(1,int(p[i])):

  

   if int(p[i])%j==0:

    count+=1

  if count==1:

   if p[i] not in l:

    l .append(int(p[i]))

 return sum(l)
 #5.Coin Change

complete function to implement coin change making problem i.e. finding the minimum

number of coins of certain denominations that add up to given amount of money.

The only available coins are of values 1, 2, 3, 4



CODE:

def coinChange(n):

 a=n//4

 b=n%4

 return a+b
 #6.Difference Sum

Given a number with maximum of 100 digits as input, find the difference between the sum of odd and even position digits.





CODE:

def differenceSum(n):

    n=str(n)

    list1=[]

    for i in n:

        list1.append(int(i))

    c=0

    s=0

    for i in range (0,len(list1)):

        if(i%2==0):

            c=c+(list1[i])

        else:

            s=s+(list1[i])

    d=s-c

    return d
    #7.Ugly number



A number is considered to be ugly if its only prime factors are 2, 3 or 5.

[1, 2, 3, 4, 5, 6, 8, 9, 10, 12, 15, …] is the sequence of ugly numbers.

Task:

complete the function which takes a number n as input and checks if it's an ugly number. return ugly if it is ugly, else return not ugly

Hint:

An ugly number U can be expressed as: U = 2^a * 3^b * 5^c, where a, b and c are nonnegative integers.

CODE:





def checkUgly(n):

    if n <= 0:

        return "not ugly"

    

    for p in [2, 3, 5]:

        while n % p == 0:

            n //= p

    

    return "ugly" if n == 1 else "not ugly"
