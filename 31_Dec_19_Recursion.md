#### Recursion in python

![](https://hackernoon.com/hn-images/1*fRTXgLKPanRlrZTd8V02yw.png)

Recursion occurs when any function calls itself. One of the big differences between recursion and looping is the way that a recursive function terminates. In the above example, a for loop ends at the end of the sequence it is looping over. However, a recursive function could continue indefinitely since it doesn’t necessarily have a sequence of data. Instead, recursive functions have what is called a base condition. A base condition is one that will terminate the loop if the condition is met.

##### Calculating Compound Interest with Recursion and Looping

As a slightly more difficult exercise, let’s determine the value of a loan or an investment with compounded interest. In order to determine what this value would be, we need 4 things:

- Duration in Years
- Interest Rate
- Number of Times Compounded Per Year
- Principal Amount
- The formula for calculating compound interest is as follows:

![](https://hackernoon.com/hn-images/1*UqPzTlpM_Ny1VoBjeim39g.png)



``` 
durationInYears = 10;
interestRate = .06;
compoundedPerYear = 12 ;
principalAmount = 4000;
 
  def compoundInterest(principal, compounded, duration, rate):
  totalCompounded = duration * compounded
  for i in range(1, (totalCompounded+1)):
  principal = principal*(1+(rate/compounded))
  return principalprint (compoundInterest(principalAmount, compoundedPerYear, durationInYears, interestRate))
	```
