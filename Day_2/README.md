# Python Basic 2

## Tenary Operator

- Condition_if_true if condition else condition_if_else
Example
```
is_friend = True
can_message = "message allowed" if is_friend else "not allowed to message"

#Result: message allowed
```
## For Loop
```
for item in (1,2,3,4,5)
  for x in ('a', 'b', 'c')
    print(item, x)
    
Result:
1a
1b
1c
2a
.
.
5c
```
## Iterables
```
user = {
  'name': 'Golem',
  'age' : 5006,
  'can_swim': False
  
for item in user.items():
  print(item)
  
#result: 
#('name', 'Golem')
#('age', 5006)
#('can_swim', False)

for item in user.values():
  print(item)

#result:
# Golem
# 5006
# False

for item in user.keys():
  print(item)
  
#result:
# name
# age
# can_swim

for key, value in user.items():
  print(key, value)

# result:
# name Golem
# age 5006
# can_swim False

```

### Range
```

#Ascending +2 steps
for _ in range(0, 10, 2):
  print(_)

#Result
#0
#2
#4
#6
#8

#Descending
for _ in range(10, 0, -1):
  print(_)
  
#Result
#10
#9
#8
#7
#6
#5
#4
#3
#2
#1

for _ in range(0, 10, 2):
  print(list(range(10)))

#Result:
#[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
#[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
#[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
#[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
#[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

```

### enumerate()
```
for char in enumerate("Hello"):
  print(char)
  
#Result
#(0, 'H')
#(1, 'e')
#(2, 'l')
#(3, 'l')
#(4, 'o')


for i,char in enumerate("Hello"):
  print(i,char)
  
#Result
#0 H
#1 e
#2 l
#3 l
#4 o

for i,char in enumerate([1,2,3]):
  print(i,char)
  
#Result
#0 1
#1 2
#2 3


for i,char in enumerate((1,2,3)):
  print(i,char)
#0 1
#1 2
#2 3

for i,char in enumerate(list(range(100))):
  if char == 50:
    print(f"the index is {i}")

# the index is 50
```

