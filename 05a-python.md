# Learn Python

Read Allen Downey's [Think Python](http://www.greenteapress.com/thinkpython/) for getting up to speed with Python 2.7 and computer science topics. It's completely available online, or you can buy a physical copy if you would like.

<a href="http://www.greenteapress.com/thinkpython/"><img src="img/think_python.png" style="width: 100px;" target="_blank"></a>

For quick and easy interactive practice with Python, many people enjoy [Codecademy's Python track](http://www.codecademy.com/en/tracks/python). There's also [Learn Python The Hard Way](http://learnpythonthehardway.org/book/) and [The Python Tutorial](https://docs.python.org/2/tutorial/).

---

###Q1. Lists &amp; Tuples

How are Python lists and tuples similar and different? Which will work as keys in dictionaries? Why?

>> lists and tuples are different in following aspects:
1) list values can be changed (e.g., by using append or del functions), but tuples can not
2) tuple values are placed using '(' brackets, but lists in '[' brackets

>>they are same in following aspects:
1) store a list of indexed values
2) recall values using index line list[1:4]

>>now for the keys in dictionaries
dictionary keys must be immutable, hence tuple can be used as a key but not lists. 
---

###Q2. Lists &amp; Sets

How are Python lists and sets similar and different? Give examples of using both. How does performance compare between lists and sets for finding an element. Why?

>> sets and lists are similar in:
1) both are mutable
2) as such they share similar built-in functions like pop()

>>sets and lists are different in:
1) sets can not contain mutable objects 
2) you can not access set objects by indexing 

>>examples of using sets
```
fruits = set(('apple','banana','mango','orange'))

>>examples of using lists
fruits = ['apple','banana','mango','orange']

>>performance issues 
found a good response from this [stackoverflow](http://stackoverflow.com/questions/2831212/python-sets-vs-lists) link. 

for the purpose of systematic iteration, lists are faster. However, for the purpose of checking if an item exists in a list, then sets are faster. 

---

###Q3. Lambda Function

Describe Python's `lambda`. What is it, and what is it used for? Give at least one example, including an example of using a `lambda` in the `key` argument to `sorted`.

>> Lambda is a handy form of integrating a small one line function. There is no need to give a name.

Here are few examples of using this function.
####Example 1:
one popular usage of lambda is to iterate over a list and apply certain function to each element.
>>>list=[1,2,3,4,5]
>>> map(lambda x:x**2, list)


####Example 2:
This [link](https://wiki.python.org/moin/HowTo/Sorting) gave an example of using lambda in the key argument to `sorted` 

>>> student_tuples = [
        ('john', 'A', 15),
        ('jane', 'B', 12),
        ('dave', 'B', 10),
]
>>> sorted(student_tuples, key=lambda student: student[2])

so, the above example applies sorted on the student tuple but the key to sort dictates doing the sort on the third element of the tuple which is student grade.

---

###Q4. List Comprehension, Map &amp; Filter

Explain list comprehensions. Give examples and show equivalents with `map` and `filter`. How do their capabilities compare? Also demonstrate set comprehensions and dictionary comprehensions.

>> list comprehensions allows creation of lists in an intuitive way
following [link](http://www.secnetix.de/olli/Python/list_comprehensions.hawk) 
describes list comprehension with examples. Following are few from the above link.

the code below produces a list containing squares of numbers from 0 to 9
`[x**2 for x in range(10)]`

following code allows applying three difference function of each word of a sentence
```
words = 'The quick brown fox jumps over the lazy dog'.split()
list_comprehension = [len(w) for w in words]
```
the above example can be done using lambda and map as follows
```
map(lambda x:len(x),words)
```
however, it should be noted that the list comprehension is for readable and efficient than map and lambda, this has been highlighted in the following stackoverflow [link](http://stackoverflow.com/questions/1247486/python-list-comprehension-vs-map)

---

###Complete the following problems by editing the files below:

###Q5. Datetime
Use Python to compute days between start and stop date.   
a.  

```
date_start = '01-02-2013'    
date_stop = '07-28-2015'
```

>> 937

b.  
```
date_start = '12312013'  
date_stop = '05282015'  
```

>> 513

c.  
```
date_start = '15-Jan-1994'      
date_stop = '14-Jul-2015'  
```

>> 7850 

Place code in this file: [q5_datetime.py](python/q5_datetime.py)

---

###Q6. Strings
Edit the 7 functions in [q6_strings.py](python/q6_strings.py)

---

###Q7. Lists
Edit the 5 functions in [q7_lists.py](python/q7_lists.py)

---

###Q8. Parsing
Edit the 3 functions in [q8_parsing.py](python/q8_parsing.py)





