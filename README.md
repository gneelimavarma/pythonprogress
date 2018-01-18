
# Python basics 
**Python installation**

 1. Download python for 64 bit machine and set path variable (right click on my computer-->go to properties, add 'C:/Python36' to PATH variable)
 2. Bring up cmd prompt , enter python -v to check python version
 3. To exit python interpreter , use ctrl Z or exit().
 4. Install geany (texteditor) to run python programs

# **Python primer**

 5. To run a python script 'python hello.py' , to run it in interactive mode 'python -i hello.py,
 6. Python is a **dynamically typed language**, which means need not specify the type of identifier while declaring unlike other languages.
			 eg: temperature = 98.6
 Here temperature is an identifier pointing to mem address where object is stored. 'temperature' here is an object of float class.
-Interestingly int,float and string are classes in python unlike objective C,java where they are primitive data types

 7. if we do temperature = room_temp then room temp has become '**alias**' of 'temperature', which means they point to the same object. However '*assigning*' a new value to any one will break the alias.eg: room_temp = room_temp+5 , here room_temp = 103.6 and temperature remains 98.6.
## Creating using objects

 8. Process of creating new instance of a class is called **instantiation**  which is generally done using a constructor of the class. eg: w = Widget()
 9. Most built in classes support **literal** form of instantiation. eg: room_temp = 98.6 will create an object of float class, 98.6 is the literal form.
 10. Some methods return information about state of object without changing the state , they are called **accessors**. Methods which change the state are called **mutators**.
## Built in classes in Python
 ** *list,set and dict are mutable classes***

1.**Bool**
 - bool() is default constructor which returns false
 - We can create bool value from nonbool value using bool(foo). It returns false if number is zero or if string is empty or if a list is empty.
 

2.**int & float**

 - Default constructors are int() and float()
 - when passed a parameter in constructor they return equivalent int or float value. eg: int(3.4) or int(-3.9) return 3 and -3
 

3.**Sequence Types: list,tuple and str class**

 - Sequence types list,tuple and str are collection of objects in which order is significant.
 - List instance stores sequence of objects similar to array,create lists using [] . eg colors = ['red','yellow','black']
 - list() constructor produces empty list,by passing iterable objects like *string,tuple,list or dict* we can produce new list. eg: list('hello') gives ['h','e','l','l','o']

----------

 - Tuple is immutable version of sequence.(I think all immutable versions are more streamlined then mutable versions,so whenever possible use immutable version)
 - Tuple is created using (),  when creating a tuple with single instance make sure you use comma. eg: (17,) is correct (17) is not a tuple


----------

 - Python string is indexed sequence of characters, it is immutable. Can be enclosed in single or double quotes.

----------

 - Python set is a collection of elements , without duplicates and without any order.
 - Hence sets are most efficient to find whether an element is present or not
 - sets are based on concept of hashtables, drawbacks of sets are that elements are not ordered and only immutable objects can be added. For example we can create set of tuples but cannot create set of sets or set of lists.
 - set is created using {} eg: {'1','2'}. exception is {} doesnt create empty lists. Instead constructor set() creates empty set. similar to lists when iterable parameter is passed to constructor it creates set of **distinct** elements. eg set('hello') produces {'h','e','l','o'}.


----------

 - Python dict is a mapping of distinct keys to associated values.{} represents an empty dictionary. eg : {'andhra':'telugu','kerala':'malyalam'}
  ## Functions
 
 - Functions are stateless, they are invoked without any context of a class or instance of a class. eg: sort(data). Methods are used to describe a member function,hence invoked on specific object. eg: data.sort().
 -  Following is an example of python function, note *def* is used start the definition of a function. Note that there is no need to mention the type of arguments passed or type of return values.

 ```python
 def findCountOfTarget(data,target):
    for val in data:
        if val == target:
            print('found target')
            return
        
    print('Did not find target')
```
- When a function is called python creates a ***activation record*** that stores all the relevant data,this record includes *namespace * to manage all identifiers that have local scope.Namespace include function parameters and all the identifiers that are defined locally.
## Information Passing

 - Formal parameters - Arguments used in function signature
 - Actual Parameters - Once passed in the function call
 - Parameters passed are assigned to formal parameters using *assignment statement*, this assignment makes actual and formal parameters aliases.
 - This makes information passing very efficient because parameters are not copied.
```Python
list1 = [1,2,3]
def infoPassing(data):
    data.append(8)
    print('fourth elemnt in formal params',data[3])
    print('fourth elemnt in actual params',list1[3])
infoPassing(list1);
```
- The above snippet is an example of information passing and also how aliases work. Here when append is applied it affects the actual parameter too because list1 and data are aliases.
## Conditional expression

 - Expressed as exp1 if condition else expr2 .
 ```Python
 if n>0:
     param = n
 else:
     param = -n
```
The above if else condition can be represented as 
```Python
n = int(input('enter a number ,positive or negative '))
param='positive' if n>0 else 'negative'
print('you entered %s number'% param )
```
## Comprehension syntax

 - A common programming task is to produce a series of output after manipulation existing series.we generally use **list comprehension**, For example
 ```Python
  result = []
      for value in iterable: 
          if condition:
              result.append(expression)
```
- The above can be represented in **comprehension syntax** as
```Python
[expression for value in iterable if condition]
```
- So to create a list of squares we can simply write
```python
numbers = [1,2,3,4,5]
result = [n*n for n in numbers]
print(result)

Above code prints [1,4,9,16,25]

```
- To create a list of squares of odd numbers
```Python
numbers = [1,2,3,4,5]
result = [k*k for k in numbers if k%2 != 0]
print(result)

Above code prints [1,9,25]
```
## Packing & Unpacking Sequences

 - If a function has a return function like this
```python
return x,y
```
It will be returning a tuple in the form (x,y) hence making it a single object.This behaviour is called *automatic packing* 
- Eg. of *Unpacking*
```python
x,y,z = range(7,10)

This assigns x=7,y=8,z=9
```
- Unpacking can be used to assign tuples returned by a function like this
```python
quotient,remainder = divmod(4,3)

divmod generally returns tuple in form (a//b,a%b)
```
## Modules & import

 - There are two ways of using a function that is defined in a module.
```python
from math import pi,sqrt

##The above statement includes the definition of pi and sqrt in the current namespace, hence they can be used directly

import math
 
##This creates an identifier 'math' in the current namespace hence methods can be accessed using dot notation
math.sqrt(6)
```











 
 

 

