# Code Compare

## Side-by-side syntax "comparisons" between 3 languages: Python (3), JavaScript(ES6) and Ruby

> Note: not every data type or function has a direct comparison in the other language, sometimes these are approximate. 

 Operation | Python | JS (ES6) | Ruby
|--|---|---|---|
| print | `print("Hello world!")` | `console.log('Hello World!')` | `print "Hello world!" / puts "Hello world!"`|
| functions | `def myfunction():`<br>&nbsp;&nbsp;&nbsp;`print("running")` | `function myFunction()`<br>&nbsp;&nbsp; `{ code here }`| `def myfunction()`<br>&nbsp;&nbsp;&nbsp;`print "running"`<br>`end` |
| calling functions | `my_function()` | `myFunction()`| `myfunction()` |
| conditionals | `if condition:`<br>&nbsp;&nbsp;&nbsp;`do sthing`<br>`else:`<br>&nbsp;&nbsp;&nbsp;`do sthing else`| `if (condition) {`<br>&nbsp;&nbsp;&nbsp; `statement }` <br>`else {` <br>&nbsp;&nbsp;&nbsp;`statement }` | `if condition`<br>&nbsp;&nbsp;&nbsp;`return true`<br>`else`<br>&nbsp;&nbsp;&nbsp;`return false`<br>`end`|
| inline conditional | `val_when_true if condition else val_when_false`| `{ condition? 'true':'false'}`| `condition ? "if true" : "else"`|
| [safe navigation operator](https://mitrev.net/ruby/2015/11/13/the-operator-in-ruby/)| [not yet](https://en.wikipedia.org/wiki/Safe_navigation_operator#Python)| `obj.value?.property`|`account&.username&.address`|| |

## In-depth comparison

### Conditionals

 Function | Python | JS (ES6) | Ruby | Notes
|--|--|--|--|---|
| Conditionals | `if, elif, else` | `if, elseif, else` | `if, elsif, else / unless, else` | - |
| Ternary operators | `val_when_true if condition else val_when_false`| `{ condition? 'true':'false'}`| `condition ? if_true : else`||
| Switch/case | - | - | `case expression`<br>`when condn`<br>&nbsp;&nbsp;&nbsp;`statement` |input is always a str by default for all 3
| Advanced printing | f strings: `f"Hello, {var}"` | `Hello, {name}` | `puts / print` |`puts` automatically adds a new line, otherwise use `print`|



### Comparison (equal/not equal) and Boolean (and/or/not) operators
 Operator | Python | JS (ES6) | Ruby | Notes
|---|---|---|---|---|
| Boolean | `bool(var)` | `var.length` | | bla | 
| Falsey | `0, 0.0, ''` |  |`false, nil` | bla | 
| Equal to | `==` | `==/===` | `==`| Note `int` and `str` are **not** equal to each other e.g. `22!='22'`|
| Not equal to | `!=` | `!=/!==` | `!=`| |
| And | `and` | `&&` | `&&`| |
| Or | `or` | &#124;&#124;  |&#124;&#124;| |
| Not | `not` | `!` |`! / unless?` |unless executees code if conditional is false.  |

### Loops

 Operator | Python | JS (ES6) | Ruby | Notes
|---|---|---|---|---|
| For | `for i in range(x)` | `-` |  bla | **For** loops iterate a **specific** no. of times
| While | `while i < 3``while True` | `-` | bla | **While** loops iterate **while** a certain condn is true

### Built-in functions e.g. length

 Function | Python | JS (ES6) | Ruby | Notes
|---|---|---|---|---|
| length | `len(var)` | `var.length` | | bla | 
| user input | `input(str)` | `` | ``| |input is always a str by default for all 3
| advanced printing | f strings: `f"Hello, {var}"` | `` | ``| |input is always a str by default for all 3

### TEMPLATE
 Operator | Python | JS (ES6) | Ruby | Notes
|---|---|---|---|---|
| Boolean | `bool(var)` | `var.length` | | bla | 



## Web development framework comparison

 X | Python | JS (ES6) | Ruby
|---|---|---|---|
|Web development frameworks|Flask, Django|React, Vue, Angular |Sinatra, Ruby on Rails|
|Unit testing|Pytest, Unitttest|React testing library, Jest |RSpec, minitest|
|Syntax linting|pylint|ESLint|Rubocop|
|Frontend tests|Selenium|Cypress|Capybara, Cucumber|

 X | Python - Django | React JS | Ruby on Rails
|---|---|---|---|
|Package manager|pip|node, yarn|RubyGems => bundler|
|Package config stored in:|`requirements.txt`|`package.json/yarn.lock`|`Gemfile.lock`|
|Library installation|`pip install <lib>`|`npm/yarn install <package>`|`gem install <gem>`|
|Library/package import|`import library`|`import library`|`require "package"`|


# Language specific syntax

## Python

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

**Q** how many times will this sentence be printed? 
```python
for i in range(3):
    print('hi')
```

<details>
<summary>
 <b>Answer</b>
</summary>
<b>3</b> times, the first time the variable i is set to 0, then 1 and 2 NOT including 3. Total of 3 times - as range(<b>3</b>)
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

### Functions from built-in modules e.g. random

Remember all python functions have a **return value**, if no ```return``` statement, the return value defaults to a ```None``` type. 

 Module | usage | example | notes
|---|---|---|---|
| random | `random.randint(var)` | `random.randint(1,10)` |generate random number between 1 and 10|
| sys | `sys.exit()` | `sys.exit()` | This allows a script to terminate, anything below this code will **not** be ecxecuted
| pyperclip | `pyperclip.paste()` | `pyperclip.copy(` | copy text from clipboard|


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


