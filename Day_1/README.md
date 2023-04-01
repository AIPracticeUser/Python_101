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




