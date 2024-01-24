# DSA Tips

Whenever we come across questions with multiple strings, it is best to think if Trie can help us.

## Logic Statement

```python
return left if left is not None else right
```

This line checks if left is not None.
If left is not None, it returns left.
If left is None, it returns right.
This is the correct way to check if left is None and decide which value to return.

```python
return left if not None else right
```

This line does not actually check the value of left.
not None is always True because None is considered falsey in Python, and not None thus becomes True.
So, this line is effectively just return left because the condition not None is always True, regardless of the value of left.
This means right will never be returned, even if left is None.