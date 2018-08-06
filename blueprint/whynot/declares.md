# why do not use C/C++ function declare syntax

Official go blog has explains why changes C function declare syntax:
- [gos-declaration-syntax](https://blog.golang.org/gos-declaration-syntax)

The main idea is

## The C function declaration syntax 
`retType funcName(paras){}`

While parameters or return type has function pointers, it may be:
```
int (*fp)(int a, int b);
int (*fp)(int (*ff)(int x, int y), int b)
int (*fp)(int (*)(int, int), int)
int (*(*fp)(int (*)(int, int), int))(int, int)
```
Finally, this last one is unrecognizable for any human beens.

## The Go function declaration syntax 
`func funcName(paras) retType`

If the parameters or return type has function type, it may be:

```
f func(func(int,int) int, int) int
f func(func(int,int) int, int) func(int, int) int
sum := func(a, b int) int { return a+b } (3, 4)
```

It is easy to recognize the syntax then.

Otherwise, the syntax of template function in C++ also seems some strange:

```
template<typaname T> int MyFunc(T a){ ... }
template<typaname T> class MyClass{ ... }
```

It is easy to recognize the template class declaration by keyword "class", but the template function syntax is absent.

If we use Go-function sytax, it may becomes:

```
template<typaname T> func MyFunc(T a) int{ ... }
template<typaname T> class MyClass{ ... }
```

The surprise is that both syntax becomes the same style:

`template<T> templateType(keyword) templateName ...`

In final words, the C-function-declaration syntax makes lots of syntax hard to comprehending.
So we use go-style syntax:
`func funcName(paras) retType`