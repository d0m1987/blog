---
author: Dominic Buehler
title: Unwrangling list comprehensions 🤓☝️
date: 2022-04-09
series: ["60 second gists"]
tags: 
    - "python"
---

If you're having problems understanding (nested) python list comprehensions like I had at the beginning, don't worry anymore!
The following explanation really helped me to understand how comprehensions and for-loops are linked.  

Just make yourself aware that the following for-loop ...

```python
items_level_1 = [1,2,3]
for item_level_1 in items_level_1:
    print(item_level_1)
```
... is equivalent to this list comprehension

```python
[print(item_level_1) for item_level_1 in items_level_1]
```

So the main thing that changes is that `print(item_level_1)` is standing in the beginning instead of being at the end of the for-loop.

If you are having a nested for-loop like the following...

```python
items_level_2 = [[1,2,3],[4,5,6]]
for items_level_1 in items_level_2:
    for item_level_1 in items_level_1:
        print(item_level_1)
```

... you can still transform it into a (hard to read) list comprehension

```python
[print(item_level_1) for items_level_1 in items_level_2 for item_level_1 in items_level_1]
```

{{% notice tip "Tip" %}}
When you read the list comprehension from left to right, it's like reading the nested for-loop from top to bottom.
{{% /notice %}}

{{% notice warning "Warning" %}}
Please keep the Zen of Python in mind:

> Flat is better than nested.  
> Readability counts.  

It's rare that a nested list comprehension is better than two easy to read for loops 😉
{{% /notice %}}

I hope that this helps you understand list comprehensions a bit more in the future. Read you soon 👋

