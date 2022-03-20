# Code Compare

## Side-by-side syntax "comparisons" between 3 languages: Python (3), JavaScript(ES6) and Ruby

> Note: not every data type or function has a direct comparison in the other language, sometimes these are approximate. 

 Operation | Python | JS (ES6) | 
|--|---|---|
| print | `print("Hello world!")` | `console.log('Hello World!')` |
| functions | `def myfunction():`<br>&nbsp;&nbsp;&nbsp;`print("running")` | `function myFunction()`<br>&nbsp;&nbsp; `{ code here }`| x
| calling functions | `my_function()` | 
| conditionals | `if condition:`<br>&nbsp;&nbsp;&nbsp;`do sthing`<br>`else:`<br>&nbsp;&nbsp;&nbsp;`do sthing else`| `if (condition) {`<br>&nbsp;&nbsp;&nbsp; `statement }` <br>`else {` <br>&nbsp;&nbsp;&nbsp;`statement }` | 
| inline conditional | `val_when_true if condition else val_when_false`| `{ condition? 'true':'false'}`|
| [safe navigation operator](https://mitrev.net/ruby/2015/11/13/the-operator-in-ruby/)| [not yet](https://en.wikipedia.org/wiki/Safe_navigation_operator#Python)| `obj.value?.property`| |

## In-depth comparison

### Conditionals

 Function | Python | JS (ES6)  | Notes
|--|--|---|------|
| Conditionals | `if, elif, else` | `if, else if, else` | - |
| Ternary operators | `val_when_true if condition else val_when_false`| `{ condition? 'true':'false'}`| |
| Switch/case | - | `switch case expression`<br>`when condn`<br>&nbsp;&nbsp;&nbsp;`statement`| |


### Comparison (equal/not equal) and Boolean (and/or/not) operators
 Operator | Python | JS (ES6) | Notes
|---|---|---|----|
| Boolean | `bool(var)` | `var.length` | | bla | 
| Falsey | `0, 0.0, ''` |  |`false, nil` | bla | 
| Equal to | `==` | `==/===` | `==`| Note `int` and `str` are **not** equal to each other e.g. `22!='22'`|
| Not equal to | `!=` | `!=/!==` | `!=`| |
| And | `and` | `&&` | `&&`| |
| Or | `or` | &#124;&#124;  |&#124;&#124;| |
| Not | `not` | `!` |`! / unless?` |`unless` executes code if conditional is false.  |


### Functions

 Python | JS (ES6)  |  Notes
|---|---|---|
| `def myfunction(args)` | `function myFunction() { //code here }` | JS functions and vars are defined using **camelCase** | 
| **JS Arrow func. syntax** => | `const myFunction = () => { // code here }` | `const myFunction = (args) => { // code here }` | 
| **JS Arrow func syntax** allows for single-line function definition| If returning a **JS object** wrap it in **( )**| `=> ({JS object})`|

### Loops

 Operator | Python | JS (ES6)  | Notes
|---|---|---|-----|
| For | `for i in range(x):` | `-`  | **For** loops iterate a **specific** no. of times
| While | `while i < 3:``while True:` | `-`  | **While** loops iterate **while** a certain condn is true


### Built-in functions e.g. length

 Function | Python | JS (ES6)  | Notes
|---|---|---|----|
| string | `str(var)` |  | - | 
| int | `int(var)` |  | - | 
| length | `len(var)` | | - | 
| type | `type(var)` | `typeof(var)` | - | 
| user input | `input("")` | `window.prompt("")`  |input is always a str by default 
| F and template strings | f strings: `f"Hello, {var}"` | ``Hello, ${name}`` |whitespace is honoured in both|
| Sleep (delay) | sleep(5) | setTimeout(myFunc, 2000) |where 2000 is in ms|


### Data structures
 Data type | Python | JS (ES6) | Notes
|---|---|---|----|
| String |`"string"` or `'string'` |  | - | 
| Integer | 1|  | - | 
| Boolean | True |  | - | 
| Mutable List | `[1,2,3]` |  | - | 
| Unmutable list | tuple `(1,2,3)`|  | - | 
| Key:value | Dictionary `{"key":"value"}`| JS Object | - | 

## Web development framework comparison

 X | Python | JS (ES6) | Ruby
|---|---|---|---|
|Web development frameworks|Flask, Django|React, Vue, Angular, NextJS |Sinatra, Ruby on Rails|
|Unit testing|Pytest, Unitttest|React testing library, Jest |RSpec, minitest|
|Syntax linting|pylint|ESLint|Rubocop|
|Frontend tests|Selenium|Cypress|Capybara, Cucumber|

 X | Python - Django | React JS | Ruby on Rails
|---|---|---|---|
|Package manager|pip, pipenv, poetry|node, yarn|RubyGems => bundler|
|Package config stored in:|`requirements.txt`|`package.json/yarn.lock`|`Gemfile.lock`|
|Library installation|`pip install <lib>`|`npm/yarn install <package>`|`gem install <gem>`|
|Library/package import|`import library`|`import library / { Component } from`|`require "package"`|


# Language specific syntax

## React Javascript

JSX is **not** HTML but a combination of JS + XML

### React component syntax

`<Component prop={} />`

	```
<ParentComponent>
 <ChildComponent>
</ParentComponent>
```

 Python | JS (ES6)  |  Notes
|---|---|---|
| `def myfunction(args)` | `function myFunction() { //code here }` | JS functions and vars are defined using **camelCase** | 
| **JS Arrow func. syntax** => | `const myFunction = () => { // code here }` | `const myFunction = (args) => { // code here }` | 

## Python

### [Scope](https://www.codequizzes.com/python/beginner-II/variable-scope)
Think of scope as a **container**

_Local_ scope is _temporary_, created when a _function_ is called and _destroyed_ when the function _returns_. 
A _local_ variable _cannot_ be used in a **global** scope. 

**Global** scopes are created **outside** a function 

This allows functions to work as individual black boxes and helps isolate code.

```python
variable = 'GLOBAL'

def my_function():
    variable = 'local'
```
**Q** In the below, what value of name will be printed out?
```python
def func_1():
    name = 'Maria'
    func_2()
    print(name)
    
def func_2():
    name = 'Bob'

func_1()
```
<details>
<summary>
 <b>Answer</b>
</summary>

Maria - as the scope of ```func_2``` will be destroyed once it returns
 </p>
</details>

The ```global``` keyword can be used to create [global](https://www.programiz.com/python-programming/global-keyword) variables in a local context (within a function)

**Q** What will be the output if you run the below?
```python
result = 0 # initial global variable

def add():
    global result
    result = result + 2 # increment by 2
    print("Inside add():", result)

add()
print("In main:", result)
```
<details>
<summary>
 <b>Answer</b>
</summary>
When we run the above script, the output will be:
<code>
Inside add(): 2
In main: 2
 </code>
 </p>
</details>

**Q** In a python function without a return statement, what type does the return value default to?

<details>
<summary>
 <b>Answer</b>
</summary>

```python
NoneType
```
 </p>
</details>  

Standard if/else blocks **keep** the existing scope and don't destroy them like a function.

**Q** In the below, what value of number will be printed out?
```python
number = 9

if True:
 number = 15

print(number)
```
<details>
<summary>
 <b>Answer</b>
</summary>
 if True means that the indented code underneath will <b>always</b> be executed,
 <b>15</b>  - if/else statements do not convert code to local scope, they <b>mantain</b> the existing scope. 
 </p>
</details>

### [Args and Kwargs](https://google.com)

**Q** What are the kwargs (optional args) for the print() function?

<details>
<summary>
 <b>Answer</b>
</summary>

```python
sep='sthing to separate each str by', end="" <--no /n after each print() call```

print("a string", sep=, end=)
```
</p>
</details>

```python
def myfunction(arg1, arg2=defaultvalue):
    print("hi")
myfunction(2,3)
```
**Q** What wil be the output of the below code snippet? #TODO

```python
def myfunction(arg1, arg2=99):
    print(arg1,arg2)
myfunction(2,3)
```
<details>
<summary>
 <b>Answer</b>
</summary>
 
```
2, 3  as those values will have overridden the default
```
</p>
</details>

### For Loops

**Q** how many times will this sentence be printed? 
```python
for i in range(3):
    print('hi')
```

<details>
<summary>
 <b>Answer</b>
</summary>
<b>3</b> times, the first time the variable i is set to 0, then 1 and 2 <b>not</b> including 3. Total of 3 times - as range(<b>3</b>)
</p>
</details>

**Q** Write a for loop to count the sum of all no.s from 1 to 100

<details>
<summary>
 <b>Answer</b>
</summary>

```python
total = 0
for i in range(101):
    total = total + i
print(total)
```
</p>
</details>

**Q** Sum of all no.s from 4 to 99

<details>
<summary>
 <b>Answer</b>
</summary>

```python
total = 0
for i in range(4, 100):
    total = total + i
print(total)
```
</p>
</details>

#### To append items to a list in a for loop, remember to instantiate your list _outside_ the for loop

### Functions from built-in modules e.g. random, sys

Remember all python functions have a **return value**, if no ```return``` statement, the return value defaults to a ```None``` type. 

#### Getting arguments from the command line ```import sys```

**Q** What is ```sys.argv[0]``` in the following line? ```python myscript.py jenna 2```

<details>
<summary>
 <b>Answer</b>
 
</summary>
<code>myscript.py</code>
<br>
sys.argv[0] is the name of the script being run, with the following arguments being sys.argv[1] and [2] and so on
</p>
</details>

**Q** What is the type of any arguments passed in to a python script by default? thourgh ```sys``` or ```input()```?

<details>
<summary>
 <b>Answer</b>
 
</summary>
<code>string</code>
<br>
that's why for integers you <b>must specify</b> <code>input = int(....</code> or <code>int(sys.argv[1])</code>
</p>
</details>

### [Python dunder methods](https://note.nkmk.me/en/python-script-file-path/)

 Method | Description | Use| ?
|---|---|---|---|
|`__main__`|A module’s __name__ is set equal to '__main__' when read from standard input|`if __name__ == __main__:`|..|
|`__file__`|returns the path specified (usually the filepath) |`filepath = __file__`|..|
|`__init__`|object inittialisation|`def __init__(self, `|..|

### [Python string methods](https://www.w3schools.com/python/python_ref_string.asp)

 Method | Description | Use| ?
|---|---|---|---|
|`strip()`|remove whitespace at **start** and **end** of a string|`myvar.strip()`|..|
|`replace()`|specified value is replaced by another|`myvar.replace(" ","")`|..|
|`join()`|useful for converting **iterables to strings**|`separator.join(iterable)`|..|

### [Python number/integer methods](https://medium.com/@bonfirealgorithm/beyond-the-for-loop-higher-order-functions-and-list-comprehensions-in-python-695b58ab71d3)

 Method | Description | Example| Use
|---|---|---|---|
|`filter()`|takes a function and an iterable as arguments and constructs a new iterable by applying the function to every element in the list|filter even no.s|`even = filter(lambda x: x % 2 == 0, integers)`|
|`map()`|applies a function to every element in a list. Unlike filter, it leaves the number of elements in the list unchanged|`myvar.replace(" ","")`|..|
|`reduce()`|Reduce works by applying a function that takes two arguments to the elements in the list, from left to right|..|..|

### [Python list comprehensions](https://google.com)

Module | usage | example | notes
|---|---|---|---|
| random | `random.randint(var)` | `random.randint(1,10)` |generate random number between 1 and 10|
| sys | `sys.exit()` | `sys.exit()` | This allows a script to terminate, anything below this code will **not** be ecxecuted
| get even no.s | `even = [x for x in integers if x % 2 == 0]`| bla | 

# JavaScript [(ES6)](https://www.w3schools.com/react/react_es6.asp)

### Defining variables
New ```let, const``` keywords were introduced. Unlike ```let``` variables, ```const``` variables **cannot** be changed.

```javascript
let x = 2;
const company = 'BT'
```
### Object destructuring


## [Ruby](https://repl.it/join/sspejxsy-roxey804)

### [Symbols](https://www.youtube.com/watch?v=VytEw_DDcYI) ( : )

* An *immutable* data type
* Symbols are denoted by a colon (**:**) and are identifiers (fixed values) unlike strings which are meant to be mutable, 
* Tend to be used for method names or attribute names
```ruby
my_symbol = :name
my_symbol2 = :name
```
`my_symbol.object_id` and `my_symbol2.object_id` will be **the same**

### Hashes
* Hashes are as objects in JS

### Unit tests - [RSpec](https://rspec.info/documentation/)

```ruby
describe "scenario name" do
  it "test name" do
    <test code here>
    <expectation here>
  end
  
  decribe "can create a new country" do
   it "create country" do
   
```


