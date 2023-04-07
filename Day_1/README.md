## Augmented Assignment Operator
```
some_value = 5
some_value = some_value + 2
```

With Augmented Assigment Operator, we can simply use
```
some_value  += 2
```
Points to note: Need to define variable first before using augmented assigment

## Strings

3 ways to assign string

1. "hello"
2. 'hello'
3. Long String
'''
hello
my
friend
'''

### String Concatenation
```
print("Hello" + "Steven")
```

However, only works with string
```
print("Hello" + 5) will generate error
```

### Booleans
is_cool = True
print(bool(0))      #False
print(bool(1))      #True
print(bool('True')) #True



### Type Conversion
To know the type of the variable, use type function
```
print(type(str(100)))  # <class 'str'>
print(type(100))       # <class 'int'>
```

### Escape Sequence
```
weather = 'It's sunny'  # This will generate an error 
```
2 ways to to solve this

1. Use different quotations
```
weather = "It's sunny" 
```

2. Use slash, to recognize that whatever after the slash is a string
```
weather = 'It\'s sunny'
```
We can also add a tab to the string
```
weather = '\t It\'s sunny'   #      It's sunny
```
Also a newline to the the string
```
weather = 'It\'s sunny. \n Hope you have a good day!'
 
# It's sunny
# Hope you have a good day
```

### Formatted String
```
name = 'Johnny'
age = 55
print('hi ' + name + '. You are ' + str(age) + ' years old'

#Result: hi Johnny. You are 55 years old
```

With formatted string, you do not need to convert variables to string
And it is easier to construct the sentence
```
print(f'hi {name}. You are {age} years old)
```
Previously in Python 2, format string used to work as shown below
```
print('hi {name}. You are {age} years old'.format(name='Johnny', age=100)
```
### String Indexes
```
#[start:stop:stepover]
selfish = 'me me me'
print(selfish[0])  -> m
print(selfish[1])  -> e
print(selfish[-1]) -> e

number = '01234567'
print(number[0:7]) 
print(number[0:8:2])
print(number[1:])
print(number[:5])  
print(number[::-1]) 

#Results:
#0123456
#0246
#1234567
#01234
#76543210
```
### Built-In functions + Methods
functions ->  https://docs.python.org/3/library/functions.html
string    ->  https://www.w3schools.com/python/python_ref_string.asp

Example of function
```
print(len('hellloooo'))  -> 9
```
Example of methods
```
quote = 'to be or not to be'
print(quote.upper())              -> TO BE OR NOT TO BE
print(quote.capitalize())         -> To be or not to be
print(quote.find('be'))           -> 3
print(quote.replace('be', 'me'))  -> to me or not to me
```

Question: After executing the above program, when executing print(quote), what is the exepcted result?

Answer: to be or not to be
Reason: Because string is immutable, they cannot be change. They can only be destroyed or created.
```
quote2 = quote.replace('be', 'me')) 
print(quote2) -> to me or not me
```

### List
```
#You can add anything in the list
l1 = [1,2,3,4,5]
l2 = [1,2,'a',True]

print(l2[0])  # 1
```

### List Slicing
```
# List is mutable
amazon_cart = [
 'notebooks',
 'sunglasses',
 'toys',
 'grapes'
]
amazon_cart[0] = 'laptop'
print(amazon_cart)
#Result: ['laptop','sunglasses','toys','grapes']

print(amazon_cart[1:3])
#Result: ['sunglasses','toys']

# Mistake
amazon_cart[0] = 'laptop'
new_cart = amazon_cart
new_cart[0] = 'gum'

print(new_cart) 
print(amazon_cart)

#Result
#['gum', 'sunglasses', 'toys', 'grapes']
#['gum', 'sunglasses', 'toys', 'grapes']

#In order to get the correct answer, you need to copy the list by slicing
amazon_cart[0] = 'laptop'
new_cart = amazon_cart[:]
new_cart[0] = 'gum'
print(new_cart)
print(amazon_cart)

['gum','sunglasses','toys','grapes']
['laptop','sunglasses','toys',grapes']
```

### Matrix
```
#Example of 2 dimensional array
matrix = [
 [1,2,3],
 [2,4,6],
 [7,8,9]
]

print(matrix[0][1])
#result: 2
```

### List Methods
List methods: https://www.w3schools.com/python/python_ref_list.asp
```
# adding
basket = [1,2,3,4,5]
print(basket.append(100))
print(basket)
# Result: [1,2,3,4,5,100]

#insert
basket = [1,2,3,4,5]
basket.insert(4, 100)
print(basket)
#Result: [1,2,3,4,100,5]

#extend
basket = [1,2,3,4,5]
basket.extend([100,101])
print(basket)
#Result: [1,2,3,4,5,100,101]

#pop
basket = [1,2,3,4,5]
basket.pop()
print(basket)
#Result: [1,2,3,4]
basket.pop()
print(basket)
#Result: [1,2,3]
basket.pop(0) #index 0
print(basket)
#Result: [2,3]

#remove
basket = [1,2,3,4,5]
basket.remove(4) #value 4
print(basket)
#Result: [1,2,3,5]

#clear
basket = [1,2,3,4,5]
basket.clear()
print(basket)
#Result: []
```

### List Method 2
Python Keywords = https://www.w3schools.com/python/python_ref_keywords.asp
```
#Index
basket = ['a','b','c','d','e']
print(basket,index('d'))
Result: 3

#Index with parameters
basket = ['a','b','c','d','e']
print(basket,index('d', 0, 2)) #start at index 0, stop at index 2
Result: Error
print(basket,index('d', 0, 4)) #start at index 0, stop at index 4
Result: 3

#Another way of searching for element in list
basket = ['a','b','c','d','e']
print('d' in basket)
Result: True
print('f' in basket)
Result: False
print('i' in 'hi my name is steven')
Result: True

#Counting number of occurrences of value
basket = ['d','b','c','d','d']
print(basket.count('d'))
Result: 3
```
### List Method 3
```
# Sort
basket = ['d','b','c','d','d']
basket.sort()
print(basket)
Result: ['b','c','d','d','d']

# Sorted
basket = ['a','x','b','c','d','e','d']
# Produce a new array of result without affecting the previous list
print(sorted(basket)) 
print(basket)
#Result:
# ['a','b','c','d','d','e','x']
# ['a','x','b','c','d','e','d']

# Copy
basket = ['a','x','b','c','d','e','d']
new_basket = basket.copy()
print(new_basket)
Result: ['a','x','b','c','d','e','d']

# Reverse
basket = ['a','x','b','c','d','e','d']
basket.reverse()
print(basket)
Result: ['d','e','d','c','b','x','a']
```

### Common List patterns
```
#Another method of list reversing
basket = ['a','x','b','c','d','e','d']
print(basket[::-1])
Result: ['d','e','d','c','b','x','a']

# Creating a range
print(list(range(100)))
#Result: [0,1,2.......100]

# Join a sentence
sentence = '!'
new_sentence = sentence.join(['hi','my','name','is','JOJO'])
print(new_sentence)
#Result: hi!my!name!is!JOJO

#Another method of writing join

new_sentence2 = ' '.join(['hi','my','name','is','JOJO'])
print(new_sentence2)
#Result: hi my name is JOJO
```

### List Unpacking
```
#Unpacking
a,b,c = [1,2,3]
print(a)
print(b)
print(c)
#Result: 1, 2 ,3

#Unpacking with rest of list
a,b,c, *other = [1,2,3,4,5,6,7,8,9]
print(other)
#Result: [4,5,6,7,8,9]

#Unpacking with rest of list and last item
a,b,c, *other, d = [1,2,3,4,5,6,7,8,9]
print(other)
#Result: [4,5,6,7,8]
print(d)
#Result: 9

```

### Dictionary
```
#Dictionary is an unordered key value pair
dict = {
 'a': [1,2,3],
 'b': "hello",
 'c': True
}

print(dictionary['b'])
Result: Hello

print(dictionary['a'][1])
Result: 2

#Dictionary in List
my_list = [
 {
  'a': [1,2,3],
  'b': "hello",
  'c': True
  },
  {
  'a': [1,2,3],
  'b': "hello",
  'c': True
  }
]

print(my_list[0]['a'][2])
Result: 3

### Dictionary Methods
user = {
  'basket': [1,2,3],
  'greet' : 'hello'
}

print(user['age'])
#Result : Error (This will cause an error if there is no such key)

print(user.get('age'))
#Result: None (This will not cause an error)

#if dict does not contain such key, use alternative value
user = {
  'basket': [1,2,3],
  'greet' : 'hello'
}
print(user.get('age', 55))
#Result: 55

#if the dict has the key, it will use they key pair value
user = {
  'basket': [1,2,3],
  'greet' : 'hello'
  'age'   : 40
}

print(user.get('age',55))
#Result: 40

#Another way to create a dictionary
user2 = dict(name = 'John')
#Result: {'name' : 'John'}
```

### Dictionary Method 2
```
user = {
  'basket': [1,2,3],
  'greet' : 'hello'
  'age'   : 20
}

print('basket' in user)
#Result: True

#Checking for dictonary keys
user = {
  'basket': [1,2,3],
  'greet' : 'hello',
  'age'   : 40
}

print('age' in user.keys())
#Result: True

#Checking for dictonary values
user = {
  'basket': [1,2,3],
  'greet' : 'hello',
  'age'   : 40
}

print('age' in user.values())
#Result: False

#Checking the whole dictionary structure (items)
user = {
  'basket': [1,2,3],
  'greet' : 'hello',
  'age'   : 40
}
print(user.items())
#Result: dict_items([('basket', [1, 2, 3]), ('greet', 'hello'), ('age', 40)]) #This is a tuple

#Clearing the dict
user = {
  'basket': [1,2,3],
  'greet' : 'hello',
  'age'   : 40
}
user.clear()
print(user)
#Result: {}

#Copy the dict
user2 = user.copy()
print(user2)
#Result: {'basket': [1, 2, 3], 'greet': 'hello', 'age': 40}

#Pop the dict records
user = {
  'basket': [1,2,3],
  'greet' : 'hello',
  'age'   : 40
}

print(user.pop('age'))
print(user)
#Result: 
# 40
# {'basket': [1, 2, 3], 'greet': 'hello'}

#Pop the last item in the dictionary
user = {
  'basket': [1,2,3],
  'greet' : 'hello',
  'age'   : 40
}
print(user.popitem())
print(user)
#Result:
#('age', 40)
#{'basket': [1, 2, 3], 'greet': 'hello'}

#Update on the value
user = {
  'basket': [1,2,3],
  'greet' : 'hello',
  'age'   : 40
}

print(user.update({'age':55}))
print(user)
#Result: {'basket': [1, 2, 3], 'greet': 'hello', 'age': 55}

#Insert a new value if update key is not found
user = {
  'basket': [1,2,3],
  'greet' : 'hello',
  'age'   : 40
}

print(user.update({'ages':55}))
print(user)
#Result: {'basket': [1, 2, 3], 'greet': 'hello', 'age': 40, 'ages': 55}
```

### Tuple
```
#Tuple is an immutable list
my_tuple = (1,2,3,4,5)
print(my_tuple[0]) #Result: 1
my_tuple[1] = 'z' #Result in Error
print(5 in my_tuple) #Result: True

#Since tuple is immutable, it can be included in a dictionary as a key
user = {
  (1,2): [1,2,3],
  'greet':'hello',
  'age': 20
  
}
print(user[(1,2)])
#Result: [1,2,3]

#Tuple slicing
my_tuple = (1,2,3,4,5)
new_tuple = my_tuple[1:2]
print(new_tuple)
#Result: (2,)

#Tuple Assigning
x,y,z, *other = (1,2,3,4,5)

print(other)
#Result: (4,5)

#Tuple count
my_tuple = (1,2,3,4,5,5)
print(my_tuple.count(5))
#Result: 2

#Tuple Index
my_tuple = (1,2,3,4,5,5)
print(my_tuple.index(4))
#Result: 3
```
### Set
```
Set is unordered collections of unique objects
my_set = {1,2,3,4,5}
my_set.add(100)
my_set.add(2)
print(my_set)
#Result: {1, 2, 3, 4, 5, 100}

#Changing list to set
my_list = [1,2,3,4,5,5]
print(set(my_list))
#Result: {1,2,3,4,5}

#Checking for value
my_set = {1,2,3,4,5}
print(my_set[0]) #Result will return an error
print(1 in my_set) #Result: True

#Same methods as previous
my_set = {1,2,3,4,5}
new_set = my_set.copy()
my_set.clear()
print(new_set)
#Result: {1,2,3,4,5}
```

### Sets 2
```
#Difference
my_set = {1,2,3,4,5}
your_set = {4,5,6,7,8,9,10}

print(my_set.difference(your_set))
#Result: {1, 2, 3} #This tells the difference without changing the set

#Discard
my_set.discard(5)
print(my_set)
#Result: {1, 2, 3, 4}

#Difference_update
my_set.difference_update(yourset))
print(my_set)
#Result: {1,2,3} #It adds the differences and changes the set

#Intersection
my_set = {1,2,3,4,5}
your_set = {4,5,6,7,8,9,10}
print(my_set.intersection(your_set))  #Can use print(my_set & your_set) as well
#Result: {4,5}

#isdisjoint
my_set = {1,2,3,4,5}
your_set = {4,5,6,7,8,9,10}
print(my_set.isdisjoint(your_set))
#Result: False (Because the 2 sets has same element in common)

#union()
print(my_set.union(your_set))
#Result: {1, 2, 3, 4, 5, 6, 7, 8, 9, 10}

#Another way of representing union
print(my_set | your_set)
#Result: {1, 2, 3, 4, 5, 6, 7, 8, 9, 10}

#is subset
my_set = {4,5}
your_set = {4,5,6,7,8,9,10}
print(my_set.issubset(your_set))
#Result: True 

my_set = {3,4,5}
your_set = {4,5,6,7,8,9,10}
print(my_set.issubset(your_set))
#Result: False

#issuperset
my_set = {4,5}
your_set = {4,5,6,7,8,9,10}
print(your_set.issuperset(my_set))
#Result: False

my_set = {4,5}
your_set = {4,5,6,7,8,9,10}
print(my_set.issuperset(your_set))
#Result: True
```

