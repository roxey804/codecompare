# Code Compare
Comparing syntax between various languages (Python 3, JavaScript(ES6) and Ruby)



 Operation | Python | JS (ES6) | Ruby
|---|---|---|---|
| print | `print("Hello world!")` | `console.log('Hello World!')` | `print "Hello world!"`|
| functions | `def myfunction():`<br>&nbsp;&nbsp;&nbsp;`print("running")` | `function myFunction()`<br>&nbsp;&nbsp; `{ code here }`| `def myfunction()`<br>&nbsp;&nbsp;&nbsp;`print "running"`<br>`end` |
| calling functions | `myfunction()` | `myFunction()`| `myfunction()` |
| conditionals | `if condition:`<br>&nbsp;&nbsp;&nbsp;`do sthing`<br>`else:`<br>&nbsp;&nbsp;&nbsp;`do sthing else`| `if (condition) {`<br>&nbsp;&nbsp;&nbsp; `statement }` <br>`else {` <br>&nbsp;&nbsp;&nbsp;`statement }` | `if condition`<br>&nbsp;&nbsp;&nbsp;`return true`<br>`else`<br>&nbsp;&nbsp;&nbsp;`return false`<br>`end`|
| inline conditional | `val_when_true if condition else val_when_false`| `{ condition? 'true':'false'}`| `condition ? "if true" : "else"`|
| [safe navigation operator](https://mitrev.net/ruby/2015/11/13/the-operator-in-ruby/)| [not yet](https://en.wikipedia.org/wiki/Safe_navigation_operator#Python)| `obj.value?.property`|`account&.username&.address`|| |

# Language specific syntax

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


