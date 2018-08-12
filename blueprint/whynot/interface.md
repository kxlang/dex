# interface

---------------------------

## 0. reference:
- [Russ Cos: interface](https://research.swtch.com/interfaces) 
- [Ian Lance Taylor: go interface](https://www.airs.com/blog/archives/277)

---------------------------

## 1. Some different interface but with the same signature
Here is an  [[example]](https://github.com/vipally/glab/blob/master/lab12/walk_test.go)

The confusion is, there are two different interface filepath.Walker and pet.Walker.

filepath.Walker is designed for **"visit all files of a filepath"**

pet.Walker is designed for **"walk action of animals"**

But unfortunately, both signature is the same:
```
type Walker interface {
		Walk()
}
```
But in go syntax, the follow usage is legal:
```
var petWalker pet.Walker
petWalker = &filepath.FilePath{}
petWalker.Walk()
```
But it's obviously that this usage is out of plan.

---------------------------

## 2. Cannot find all types that has implements an interface
Go tools is hard to find type pet.Dog and pet.Cat through pet.Walker,

Because there is no declarations of the relations between them.

---------------------------

## 3. Maybe this outter-declaration can solve this problem

```
//declare which types has implements this interface
implements pet.Walker{
	*pet.Dog
	*pet.Cat
}
//declare this type has implement any interfaces
implements *filepath.FilePath{
	filepath.Walker
	filepath.Reader
}
```

## 4. Go's non-invasive way to describ the world
There is an interesting example.

How to describ a mermaid,  mankind or fish？

In C++/Java way(invasive interface), try to descrbe a mermaid may cause confusion.

It will cause the "class diagram" change no matter describe mermaid as mankind or fish.

Because mermaid will break the definition of both mankind and fish.

In Go way(non-invasive interface). It is an easy way:

Mermaid is a "Swimmer" and "Speaker", and is not a "Walker".

It has nothing to do with  mankind or fish.
