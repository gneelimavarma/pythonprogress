
# Everyday progress on python
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
 - 

 

