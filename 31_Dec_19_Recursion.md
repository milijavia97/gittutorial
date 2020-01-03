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
durationInYears = 10
compoundedPerYear = 12array = [{
    'times compounded': 0,
    'duration remaining': 10,
    'interest rate': .06,
    'current payment': 2000,
    'compounded per year': 12,
    'principal amount': 4000,
    'total compounded': compoundedPerYear*durationInYears
}]*
(compoundedPerYear*durationInYears)def recursiveData(inputArr, outputArr):
    if len(inputArr) == 0 or inputArr[-1]['principal amount'] <= 0:
        return outputArr
    else:
        current = inputArr[:1][0]
        inputArrayLength = len(inputArr[1:])
        outputArray = outputArr
        if len(outputArray) == 0:
            outputArray.append(current)
            return recursiveData(inputArr[1:], outputArray)
        else:
            newTimesCompounded = outputArray[-1]['times compounded'] + 1
            newDurationRemaining = current['duration remaining']
            if ((outputArray[-1]['times compounded'] + 1) % 12) == 0:
                newDurationRemaining = outputArray[-1]['duration remaining'] - 1
            principal = (outputArray[-1]['principal amount'])*(1+(outputArray[-1]
                                                                  ['interest rate']/outputArray[-1]['compounded per year']))
            currentPayment = current['current payment']
            if currentPayment > principal:
                currentPayment = principal
            newPrincipalAmount = (principal - currentPayment)
            newTotalCompounded = outputArray[-1]['total compounded'] - 1
            newCurrent = {
                'times compounded': newTimesCompounded,
                'duration remaining': newDurationRemaining,
                'interest rate': current['interest rate'],
                'current payment': currentPayment,
                'compounded per year': current['compounded per year'],
                'principal amount': newPrincipalAmount,
                'total compounded': newTotalCompounded
            }
            outputArray.append(newCurrent)
            inputArr = [newCurrent]*inputArrayLength
            return recursiveData(inputArr, outputArray)returnData = recursiveData(array, [])
for i in returnData:
    print (i)
```


![](https://hackernoon.com/hn-images/1*9DxIgwaja_ikvLSxCI4U6g.png)

##### Inner Function
Whenever we print any variable inside an inner function, the Python interpreter searches for that variable declaration/initialization until four scopes. First, the local scope of the inner function, then the local scope of the enclosing function, then the global scope and at last the built-in module scope. So, the inner function can access the variables declared/initialized in all these four scopes as shown in the below image.

![](https://i1.faceprep.in/Companies-1/closures-in-python-first.png)

###### You use inner functions to protect them from everything happening outside of the function, meaning that they are hidden from the global scope

##### Calling Techniques

![](http://pycallgraph.slowchop.com/en/master/_images/filter_none.png)

class Parent: 
  
    # constructor of Parent class 
    def __init__(self): 
        # Initialization of the Strings 
        self.String1 ="Hocus"
        self.String2 ="Pocus"
  
    def Function2(self): 
        print("Function2 : ", self.String1) 
        return

child class is inheriting from Parent class 
class Child(Parent): 
![](https://hackernoon.com/hn-images/1*9DxIgwaja_ikvLSxCI4U6g.png)

##### Inner Function
Whenever we print any variable inside an inner function, the Python interpreter searches for that variable declaration/initialization until four scopes. First, the local scope of the inner function, then the local scope of the enclosing function, then the global scope and at last the built-in module scope. So, the inner function can access the variables declared/initialized in all these four scopes as shown in the below image.

![](https://i1.faceprep.in/Companies-1/closures-in-python-first.png)

###### You use inner functions to protect them from everything happening outside of the function, meaning that they are hidden from the global scope

##### Calling Techniques
![](http://pycallgraph.slowchop.com/en/master/_images/filter_none.png)

```
class Parent: 
  
    # constructor of Parent class 
    def __init__(self): 
        # Initialization of the Strings 
        self.String1 ="Hocus"
        self.String2 ="Pocus"
  
    def Function2(self): 
        print("Function2 : ", self.String1) 
        return
  
# Child class is inheriting from Parent class 
class Child(Parent): 
  
    def Function1(self): 
        # calling Function2 Method in parent class  
        self.Function2() 
        print("Function1 : ", self.String2) 
        return   
  
### Instance of Parent class 
Object1 = Parent() 
  
### Instance of Child class 
Object2 = Child() 
  
# Calling Function1 using Child class instance 
Object2.Function1()
    def Function1(self): 
        # calling Function2 Method in parent class  
        self.Function2() 
        print("Function1 : ", self.String2) 
        return   
  
 Instance of Parent class 
Object1 = Parent() 
  
 Instance of Child class 
Object2 = Child() 
  
 Calling Function1 using Child class instance 
Object2.Function1()
```
![](https://codeforwin.org/wp-content/uploads/2017/12/return-value-from-function-in-c.png)
