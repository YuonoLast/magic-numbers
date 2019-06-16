# Magic Numbers

  This library is made for working with numbers. Check for a number, check for the number of numbers of one type or another. If you need to work with numbers and do not want to write for this different scripts, I suggest my own magic-numbers library.

## This library includes the following functions:

**1.** simpleNumberCheck([numberForCheck, {settings}]) 
**1.** moreCheck([[argument1, argument2, argument3, ... argumentN], {settings}])
**1.** ???

## Functional:

### 1. simpleNumberCheck()

`simpleNumberCheck([numberForCheck OR [ArayForCheck], {settings}])` - This function tests an argument or an array of arguments against a number.

### How to setup? 

**Argument passed to the function:** 

[] - pass in the array as the main argument.

**What to transfer to the array:**

[0][argument1, argument2, argument3, ... argumentN] or ARGUMENT - pass an array or one argument to check.

[1]{modeTest: true/false, fullResult: true/false} - settings.  

**Settings object settings:**

modeTest - Its test mode.

fullResult - Full answer.

**It looks like the finished settings:**

[arguments, {modeTest: true/false, fullResult: true/fasle}] - check one argument.

[[argument1, argument2, argument3, ... argumentN], {modeTest: true/false, fullResult: true/fasle}] - checking an array of arguments.


### Example: 

**Check one array:**

`simpleNumberCheck([123, {a: true, b: true}])  => [true, true]`

`simpleNumberCheck([123, {a: true, b: false}])  => true`

`simpleNumberCheck([123, {a: false, b: true}])  => true`

`simpleNumberCheck([123, {a: false, b: false}])  => true`

**Array check:**

`simpleNumberCheck([[123, -12, 1.1, '123', 'asd', NaN], {a: true, b: true}])  => [[true, true], [true, true], [true, true], [false, true], [false, false], [true, false]]`

`simpleNumberCheck([[123, -12, 1.1, '123', 'asd', NaN], {a: true, b: false}])  => [true, true, true, false, false, false]`

`simpleNumberCheck([[123, -12, 1.1, '123', 'asd', NaN], {a: false, b: true}])  => [true, true, true, true, false, false]`

`simpleNumberCheck([[123, -12, 1.1, '123', 'asd', NaN], {a: false, b: false}])  => [true, true, true, true, false, false]`


### 2.moreCheck()

`moreCheck([[arayForCheck], {settings}])` - This function requires one of the keywords and displays true/false depending on whether this type of numbers prevails in the array or not.

### How to setup? 

**Argument passed to the function:** 

[] - pass in the array as the main argument.

**What to transfer to the array:**

[0][argument1, argument2, argument3, ... argumentN] - An array of arguments is passed as the argument to be checked.

[1]{keySearch: 'int'/'neg'/'pos'/'flo'} - settings.  

**Settings object settings:**

keySearch - The type that will be tested for excellence among the rest.

*Decrypt Value keySearch in tabel 1:*

|    'int'    |    'neg'    |    'pos'    |    'flo'    |
|:-----------:|:-----------:|:-----------:|:-----------:|
| Integer     | Negative    | Positive    | Float       |



**It looks like the finished settings:**

[[argument1, argument2, argument3, ... argumentN], {keySearch: 'int'/'neg'/'pos'/'flo'}] - checking an array of arguments.


### Example: 

**Array check:**

`moreCheck([-1000, 300, 3.345354, 3.324, -727, 0], {keySearch: 'int'}])  => true`

`simpleNumberCheck([[-1000, 300, 3.345354, 3.324, -727, 0], {keySearch: 'flo'}])  => false`

`simpleNumberCheck([[-1000, 300, 3.345354, 3.324, -727, 0], {keySearch: 'pos'}])  => true`

`simpleNumberCheck([[-1000, 300, 3.345354, 3.324, -727, 0], {keySearch: 'neg'}])  => false`