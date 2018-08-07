# DEX: Ideal modern programming language design plan

## Principles of design
- Practical
- Easy(read/write/etc)
- Full features
- Fast(coding/compiling/running/testing/etc)
- Inherit(C-family)
- Treat everything equally(types/syntax/etc)
- Reading beautify 

## Design reference
- [C](#)
- [C++](#)
- [D](https://dlang.org/spec/spec.html)
- [Go](https://golang.org/ref/spec)

## Features
- enough build-in types
- tuple
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
- no oop?

## package
- root
- project root
- refer go package

## grammar

## declarations

## basic types
| type | size | range | 说明
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
| tuple |  |  | 
| slice |  |  | 
| array |  |  | 
| map |  |  | 
| struct |  |  | 
| class |  |  | 
| union |  |  | 
| enum |  |  | 
| tuple |  |  | 


## packages

## declarations
- var a int
- const b = 5
- var f = func(a int)float32{}
- g := func(a int)float32{}
- func MyFunc(x, y int)int{ return x+y }
- struct Mystruct{}
- class Myclass{}
- union MyUnion{}
- enum MuEnum{}
- template(T) func Add(x,y T) T{ return x+y }

## keywords
- if
- switch
- while
- do while
- foreach
- for
- type
- rettype
- mulswitch
- auto
- fallthrough
- range
- tuple

## [function](http://blog.golang.org/gos-declaration-syntax)
 `func Name(para) ret`


## generic
- template function
- template struct
- template union
- template enum

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

## overwrite

## operator overloadings
- operator +()
- operator -()
- operator *()
- operator /()

## properties

## attributes

## expressions

## statement

## oop - do not need?

## inner function

## tests

## examples

## tools

## reflect
- #typeof(v)
- #@$
