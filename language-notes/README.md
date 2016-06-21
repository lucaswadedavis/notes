# Language Notes

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

