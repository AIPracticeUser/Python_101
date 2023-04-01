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
print(number[0:7])  -> 123456
print(number[0:8:2] -> 0246
print(number[1:]    -> 1234567
print(number[:5]    -> 01234
print(numner[::-1]  -> 76543210
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

