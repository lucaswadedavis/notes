# Language Notes

What do I want?
- Simplicity (Favor Simple Logic and Complex Data over Simple Data and Complex Logic)
- Modularity (Components should be unitary - I shouldn't need to go to 3 files to figure out what is going on)
- No Templates, No HTML, No CSS
- Enthalpy (Least Surprise)
- Composeability
- Interoperability (can I use lots of other tools with this)
- (Optional) Lifecycle hooks (I worry that this reduces Simplicity and interoperability)
- Clarity
- Parsimony
- Transparency (JSON not Strings)
- Flexibility
- Extensibility
- Every program is a filter (Correlary: keep data data as long as possible, only create DOM at the last moment)
- I want to work in the lab not the factory

Symbols I like:
```
    <> [] {} () . ... - --- | ||| :
```

Symbols I don't like:
```
    ! ? ~ ` ' " ; , & ^ % $ # @ / \
```

So I like things that look like this
```
    x : ( y:int(12) ) { y + 12 }
    x(12)
```
Returns 24

```
    a : ( b:bool(false) ) { not b }
    a()
```
Returns true

```
    create_adder : ( d:int(0) ) { f : ( e:int(0) ) { d + e} }
    g : create_adder(10)
    g(2)
```
Returns 12

```
    a : [1, 2, 3]
    a(0)
```
Returns 1

```
    a : {
        b : 12,
        c : ( x : int ( 100 ) ) { x / 2 }
    }
    a(b)
```
Returns 12

```
    a : {
        b : 12,
        c : ( x : int ( 100 ) ) { x / 2 }
    }
    a(c)(12)
```
Returns 6

I'm just daydreaming now
```
    x
    x()
    x[]
    {x}
    [x]
    x.y
    (x)
    x:[1,2,3]
    y:[accumulator, item]
    reduce :: [c:list, a, f:func] {...}
    [c, a, f]::reduce
    
