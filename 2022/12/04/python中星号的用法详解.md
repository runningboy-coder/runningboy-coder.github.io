# *tuple 和 ** dict
 *tuple: 作用是申明将此可迭代对象的元素视为此函数调用的位置参数
 **dict:作用是申明将字典中的键值对视为此函数调用的附加命名参数。
# positional-only parameter and keyword-only parameter
\*之后的参数都是keyword-only
`
def f(a, *, b): ...

f(1, b=2)  # fine
f(1, 2)    # error: b is keyword-only

`

\ 之后的参数都是positional-only

`
def f(a, /, p, *, k): ...

f(  1,   2, k=3)  # fine
f(  1, p=2, k=3)  # fine
f(a=1, p=2, k=3)  # error: a is positional-only
`



