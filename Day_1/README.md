## Augmented Assignment Operator

some_value = 5
some_value = some_value + 2

With Augmented Assigment Operator, we can simply use

some_value  += 2

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
print("Hello" + "Steven")

However, only works with string
print("Hello" + 5) will generate error


### Type Conversion
To know the type of the variable, use type function
print(type(str(100)))  -> <class 'str'>
print(type(100))       -> <class 'int'>

### Escape Sequence
weather = 'It's sunny'  -> This will generate an error 

2 ways to to solve this

1. Use different quotations
weather = "It's sunny" 

2. Use slash, to recognize that whatever after the slash is a string
weather = 'It\'s sunny'

We can also add a tab to the string
weather = '\t It\'s sunny'   ->      It's sunny

Also a newline to the the string
weather = 'It\'s sunny. \n Hope you have a good day!'
-> 
It's sunny
Hope you have a good day


### Formatted String
name = 'Johnny'
age = 55
print('hi ' + name + '. You are ' + str(age) + ' years old'
Result: hi Johnny. You are 55 years old

With formatted string, you do not need to convert variables to string
And it is easier to construct the sentence
print(f'hi {name}. You are {age} years old)

Previously in Python 2, format string used to work as shown below
print('hi {name}. You are {age} years old'.format(name='Johnny', age=100)

### String Indexes
[start:stop:stepover]
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

### Built-In functions + Methods
functions ->  https://docs.python.org/3/library/functions.html
string    ->  https://www.w3schools.com/python/python_ref_string.asp

Example of function
print(len('hellloooo'))  -> 9

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





