## Dictionaries

Dictionaries are collections of associated pairs of items where each pair consists of a key and a value. This key-value pair is typically written as key:value. Dictionaries are written as comma-delimited key:value pairs enclosed in curly braces. For example:

## Dictionary operators

| **Operator** | **Use**          | **Explanation**                                               |  
| ------------ | ---------------- | ------------------------------------------------------------- |  
| `[]`         | `my_dict[k]`     | Returns the value associated with `k`, otherwise its an error |  
| `in`         | `key in adict`   | Returns `True` if key is in the dictionary, `False` otherwise |  
| `del`        | del `adict[key]` | Removes the entry from the dictionary                         |

```python
>>> capitals = {'Iowa':'DesMoines', 'Wisconsin':'Madison'}
>>> capitals
{'Wisconsin': 'Madison', 'Iowa': 'DesMoines'}
>>> print(capitals['Iowa'])
DesMoines
>>> capitals['Utah'] = 'SaltLakeCity'
>>> print(capitals)
{'Utah': 'SaltLakeCity', 'Iowa': 'DesMoines', 'Wisconsin': 'Madison'}
>>> capitals['California'] = 'Sacramento'
>>> print(len(capitals))
4
```

```python
>>> for i in capitals:
...     print(capitals[i], 'is the capitol of', i)
... 
Sacramento is the capitol of California
SaltLakeCity is the capitol of Utah
DesMoines is the capitol of Iowa
Madison is the capitol of Wisconsin
```

```python
>>> capitals['Wisconsin']
'Madison'
>>> 'Florida' in capitals
False
>>> 'Wisconsin' in capitals
True
>>> del capitals['Iowa']
>>> capitals
{'California': 'Sacramento', 'Utah': 'SaltLakeCity', 'Wisconsin': 'Madison'}
```

## Dictionary methods

| **Method name** | **Use**            | **Explanation**                                              |  
| --------------- | ------------------ | ------------------------------------------------------------ |  
| `keys`          | `adict.keys()`     | Returns the keys of the dictionary in a dict_keys object     |  
| `values`        | `adict.values()`   | Returns the values of the dictionary in a dict_values object |  
| `items`         | `adict.items()`    | Returns the key-value pairs in a dict_items object           |  
| `get`           | `adict.get(k)`     | Returns the value associated with `k`, `None` otherwise      |  
| `get`           | `adict.get(k,alt)` | Returns the value associated with `k`, `alt` otherwise       |

```python
>>> extensions = {'brian':1410, 'jake':1137}
>>> extensions
{'jake': 1137, 'brian': 1410}
```

Use the `list()` function to extract keys, values and items into lists:

```python
>>> extensions.keys()
dict_keys(['jake', 'brian'])
>>> list(extensions.keys())
['jake', 'brian']
```

```python
>>> extensions.values()
dict_values([1137, 1410])
>>> list(extensions.values())
[1137, 1410]
```

```python
>>> extensions.items()
dict_items([('jake', 1137), ('brian', 1410)])
>>> list(extensions.items())
[('jake', 1137), ('brian', 1410)]
```

The `get()` method returns a the value of the specified key. If no matching key, it returns `None`. A second alt argurment can be provided that returns if no matching key found:

```python
>>> extensions.get('brian')
1410
>>> extensions.get('steve')
>>> extensions.get('steve', 'NO ENTRY')
'NO ENTRY'
```
