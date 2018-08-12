# DEX: Ideal modern programming language design plan

## Principles of design
- Practical
- Easy(read/write/etc)
- Full features
- Fast(coding/compiling/running/testing/etc)
- Inherit(C-family)
- Treat everything equally(build-in/types/syntax/etc)
- Reading beautify 

## Design reference
- [C](#)
- [C++](#)
- [D](https://dlang.org/spec/spec.html)
- [Go](https://golang.org/ref/spec)

## Features
- enough build-in types
- tuple,map,array,slice
- interface
- compile-time calculating
- properties
- clean grammar
- templates
- function overloading
- operator overloading
- buildin-testing
- reflect
- package
- with-object C?
- no class, no inherit?

## package
- root
- project root
- refer go package

A package is in a single directory.

A package can have any number of files.

Test files and template files is sperate from nomal code files. *.dex *.test

## grammar

## declarations

## basic types
| type | size | range | desc
| --- | --- | --- | ---
| int8 | 1 | [-128, 127] | 
| int16 | 2 |  | 
| int32 | 4 |  | 
| int64 | 8 |  | 
| int128 | 16 |  | 
| int | 4 or 8 |  | 
| byte | 1 | [0, 255] | 
| uint8 | 1 | [0, 255] | 
| uint16 | 2 |  | 
| uint32 | 4 |  | 
| uint64 | 8 |  | 
| uint128 | 16 |  | 
| uint | 4 or 8 |  | 
| float32 | |  | 
| float64 | |  | 
| double | |  | 
| complex64 | |  | 
| complex128 | |  | 
| complex | |  | 
| bool | |  | 
| string |  |  | 
| rune |  |  | 
| slice |  |  | 
| array |  |  | 
| map |  |  | 
| struct |  |  | 
| class |  |  | 
| union |  |  | 
| enum |  |  | 
| tuple |  |  | 

## declarations
- var a int
- const b = 5
- var f = func(a int)float32{}
- g := func(a int)float32{}
- func MyFunc(x, y int)int{ return x+y }
- type Mystruct struct{}
- type MyUnion union{}
- type MyEnum enum {}
- template(T) func Add(x,y T) T{ return x+y }

## keywords
- if
- else
- switch
- multiswitch
- while
- do while
- foreach
- for
- break
- continue
- fallthrough
- range
- type
- func
- struct
- union
- enum
- tuple
- map
- decltype
- auto
- lazy
- alias
- interface
- template
- mixin
- nil
- iota

## operator
- +
- -
- *
- /

## enums
```
type enumName enum dataType_opt{}
```

## unions
```
type unionName union {}
```

## structs
```
type structName struct {}
```

## consts
- prefix
- suffix
- strings

## [function](http://blog.golang.org/gos-declaration-syntax)
 ```
func Name(para) retType
```

## interface
```
type someInterface interface{
	someFun1(para int)int
	someFun2(para string)string
}
implements someInterface{
	someTypeA
	someTypeB
}
```


## generic
- template function
- template struct
- template union
- template enum
- which package will the gp and generated code in? 

## compile time
- #if
- #elseif
- #else
- #switch
- #mulswitch
- #foreach
- #assert
- #format
- #message
- #align
- #templateName()
- ##templateFunc()
- #type
- #rettype
- #date
- #time
- #timestamp

## override

## operator override
- operator =()
- operator ==()
- operator >()
- operator >=()
- operator <()
- operator <=()
- operator +()
- operator -()
- operator *()
- operator /()
- operator &()
- operator |()
- operator ~()
- operator >>()
- operator <<()
- operator >>>()

## properties

## attributes

## expressions

## statement

## oop - do not need?

## build-in functions

## tests
- *.test files

## examples

## tools
- dox

## reflect
- #typeof(v)
- #@$
