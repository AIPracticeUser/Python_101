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
