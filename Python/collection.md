# Collection
## Menu
- set
- sequence
- mappings
- streams
## Common operations
```python
x in coll
x not in coll
any(coll) #true if any item in coll is true
all(coll) #true if every item in coll is true
len(coll) #streams not support
max(coll)
min(coll)
sorted(coll)
```
## Set
> unordered, no duplicates

### operations
```python
                #set1.isdisjoint(coll)
set1<=set2      #set1.issubset(coll)
set1<set2          
set1>=set2      #set1.issuperset(coll)
set1>set2       
#---------------------------------
set1|set2       #set1.union(coll,..) 并集
set1&set2       #set1.intersection(coll ,...) 交集
set1-set2       #set1.difference(coll,...) 差集
set1^set2       #set1.symmetric_difference(coll,..)对称差


```
### frozenset
> immutable set

## Sequences
> ordered collection, duplicated

sequence types:
```python
- str           # 'abc'
- bytes         # b'abc'
- bytearray     
- range         #range(100)
- tuple         #(a,b)
- list          #['a',b,3]
```
### operations
```python
<,<=,>,>=
==,!=
in,not in
Repetition(*)
Concatenation(+)
Indexing
Slicing
```
### Str Testing
```python
str1.isalpha()
str1.isalnum()
str1.isdigit()
str1.numeric()
str1.isdecimal()
str1.islower()
str1.isupper()
str1.istitle()
```

## Mappings
> mutable, unordered, key/value pairs

mapping types:
- Dictionaries(dict in python)



## Streams
> temporally ordered sequence, indefinite length, one type

> from source to sink

types:
- file
- generator
- raw_input

### Files
```python
t   # text mod
b   # byte mod
r
w
a
r+
w+
a+
```


### Generators
```python
yield replace return to produce a generator 
next(generator[,default value])

```
# Collection-Related Expression Features
## Comprehensions
### list comprehensions
```python
[expression for item in collection]
```
### set and dictionary comprehensions
``` python
{expression for item in collection}

{key-expression:value-expression for key, value in collection}
```
### generator expression
```python
(expression for item in collection)
```
### conditional comprehensions
```python
[expression for element in collection if test]
```
### nested comprehensions
```python
[exp1+exp2 for i in col1 for j in col2]
```
## Functional Parameters
- key parameter
```python
max(x,y,key=fun)
```
- Function object
```python
fn = max  # 相当于同名函数？
fn(1,2,3)

```
- Anonymous functions
```python
lambda args:expression-using-args

fn = lambda x,y:x*x+y*y
fn(1,2)

```
