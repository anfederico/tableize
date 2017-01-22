<p align="center"><img src="https://raw.githubusercontent.com/anfederico/Tableize/master/media/Tableize.png" width=40%></p>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
[![PyPI version](https://badge.fury.io/py/tableize.svg)](https://badge.fury.io/py/tableize)
[![Build Status](https://travis-ci.org/anfederico/Tableize.svg?branch=master)](https://travis-ci.org/anfederico/Tableize)
![Dependencies](https://img.shields.io/badge/dependencies-up%20to%20date-brightgreen.svg)
[![GitHub Issues](https://img.shields.io/github/issues/anfederico/Tableize.svg)](https://github.com/anfederico/tableize/issues)
![Contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)
[![License](https://img.shields.io/badge/license-MIT%20License-brightgreen.svg)](https://opensource.org/licenses/MIT)

## Install
```python
pip install tableize
```

## Code Examples

#### Create a table with 5 columns
```python
from tableize import tableize

letters = ['a','b','c','d','e','f','g','h','i','j','k','l','m','n','o']

t = tableize(letters, cols = 5)
t.show()
```

```
a b c d e 
f g h i j 
k l m n o 
```

#### Flip how the table is filled
```python
t.flip()
t.show()
```

```
a d g j m 
b e h k n 
c f i l o 
```

#### Create a table with 10 rows
```python
from tableize import tableize

t = tableize(letters, rows = 10)
t.show()
```

```
a k 
b l 
c m 
d n 
e o 
f 
g 
h 
i 
j 
```

#### Switch from rows to columns
```python
t.switch()
t.show()
```
```
a b c d e f g h i j 
k l m n o
```

#### More customization
```python
from tableize import tableize

words = ['apple','bus','cart','drum','empty','flint','get','happy','ill','joker','kneel','lard','no','mop']                   

t = tableize(words, cols = 5)
t.text(bullet = '+ ', spaces = 2, spacer = ' ')
```

```
- apple  - bus   - cart   - drum  - empty  
- flint  - get   - happy  - ill   - joker  
- kneel  - lard  - no     - mop  
```

```python
t.text(bullet = '', spaces = 5, spacer = '~')
```

```
apple~~~~~bus~~~~~~cart~~~~~~drum~~~~~empty~~~~~
flint~~~~~get~~~~~~happy~~~~~ill~~~~~~joker~~~~~
kneel~~~~~lard~~~~~no~~~~~~~~mop~~~~~~open~~~~~~
```

```python
t.write(filename = 'mytable', bullet = '+ ', spaces = 3, spacer = ' ')
```

```
mytable.txt

+ apple   + bus    + cart    + drum   + empty   
+ flint   + get    + happy   + ill    + joker   
+ kneel   + lard   + no      + mop  
```