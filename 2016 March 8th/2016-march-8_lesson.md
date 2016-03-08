##NYIT Manhattan IEEE
###2016 March 8,
---



### Builtin Functions
Today we're going to start off with learning about some of python's builtin functions

+ __print__  -- sends the contents of a variable to stdout. When I say stdout, just read it as 'it prints it to the screen'. We'll worry about the details about it later
+ __type()__ -- when working with data, you need to know what type of data it is so you know how you can manipulate it
+ __str()__ -- this will try to convert whatever you give it to a string. Be aware that this function is very handy, but it is not a cure-all, so to speak. If you pass it an object, the resulting output may not be the data you're looking for.
+ __range()__ -- creates a list of numbers, with some choice in iteration
+ __map()__ -- Applies a function to each _iterable_ item and returns a list.





####print

To set a variable in python we use the __=__ operator, but to see the data we need a tool of some sort.


```python
>>>s = 'hello world'
>>>print s
>>>hello world
```

I used the __print__ _function_ to show the results of the variable. [python docs on the print function](https://docs.python.org/2/reference/simple_stmts.html#print)


####type()

```python
>>>number = 42
>>>type(number)
<type 'int'>

>>>word = 'spam'
>>>type(word)
<type 'str'>
```
Returns the type of the given object. 


####str()
```python
>>>foo = 42
>>>type(foo)
<type 'int'>

>>>foo = str(foo)
>>>type(foo)
<type 'int'>

# being careful
>>>import math
>>>type(math)
<type 'module'>

>>>str(math)
"<module 'math' from '/usr/local/Cellar/python/2.7.11/Frameworks/Python.framework/Versions/2.7/lib/python2.7/lib-dynload/math.so'>"

```


####range()

```python
>>>range(10)
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

>>>foo = range(5)
>>>foo
[0, 1, 2, 3, 4]

# what if I wanted every fifth number?
>>>range(0, 50, 5)
[0, 5, 10, 15, 20, 25, 30, 35, 40, 45]
```
range() allows for a quick creation of a list of numbers, following any iteration pattern of your choosing. Be it every second negative number between -4 and -60, or what have you. Other languages you would use a _for loop_ to obtain the same results; python provides a simple one-line statement for you.



####map()
```python
>>>nums = range(10)
>>>nums
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

>>>map(hex, nuts)
['0x0', '0x1', '0x2', '0x3', '0x4', '0x5', '0x6', '0x7', '0x8', '0x9']
```
Here we create a list of numbers using the range function. What if we wanted to convert each entry in the list to a hexadecimal number [wiki](https://en.wikipedia.org/wiki/Hexadecimal). We simple can't convert a list object by passing it into the hex() function. Think about it for a moment and you'll see why. The job of the list object is to hold __stuff__ in a certain fashion in memory. It doesn't matter what's in the list object, the only thing that matters is how it's organized. Say, compared to a dictionary. In this instance, we don't care how the data is organized, all we care about is converting the data to a different type. We need to change each instance in the list object, not the list itself. We can do that, with the map() function.






---
---

###User Functions

There's a limit to how useful python's own functions can be; what would be better is if we could create our own

We do so using the __def()__ function

```python
>>>def hello(name):
>>>    print 'hello ' + name

>>>hello('George')
>>>hello George
```

Congratulations, you've just witness one of the most simple python functions ever constructed. Nevertheless, let's take a look at it.

We start off with the __def__ function and end with a __:__
This is the standard syntax for creating a function in python, if you don't have such, you'll get an error. The parenthesis are used to specify input to the function, this depends on what your goal of said function is. Currently, the example produces and output to stdout by using the print function. What if we didn't want to print out the result, and save it for later?

```python
>>>def area(len, width):
>>>    area = len * width
>>>    return area

>>>shape = area(4, 2)
>>>shape
8

```
Here we use the term _return_ to specify what we want the function to give as a result. If we didn't mention what we want to return, the function would do the calculation with the given input, and then nothing. If you don't save the results anywhere, the computer isn't gonna do it for you.


---

### Lists and Dicts

I'd like to cover two types of data structures today that are extremely paramount in your understanding of python. They are, the __list__ and the __dict__ (heh). 

A __list__ is a _mutable_ object that holds data in a list. Mutable means that we can change the length of the list at any time. 

```python
# this is a valid list
>>>things = ['word', '8gt8H(*&', 12, 1.671345]
>>>type(things)
<type 'list'>

>>>words = list()
>>>words.append('cliche')
>>>words.append('eccentric')
>>>words.append('senpai')
>>>words.append('student debt')
>>>words
['cliche', 'eccentric', 'senpai', 'student debt']



A __dict__ (or dictionary) is an object for storing data in a dictionary-like fashion. With dicts, we have a _key_ and a _value_. A dictionary, is a real world example of a python dict









