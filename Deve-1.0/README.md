# CS321

<http://aktemur.github.io/cs321>

## Deve

This is a simple programming language
where we have arithmetic expressions (add, multiply, subtract, divide),
names, bindings, conditionals, and boolean literals.

Grammar:

```
main ::= exp EOF
exp  ::= INT | BOOL | NAME
       | exp PLUS exp
       | exp STAR exp
       | exp MINUS exp
       | exp SLASH exp
       | IF exp THEN exp ELSE exp
       | LET NAME EQUALS exp IN exp
```

### Interpreter

To run:

```ocaml
# #use "main.ml";;
...
# run "30 + 6 * 2";;
- : int = 42
# run "let a = 3
       in let b = 3
          in let c = 5
             in 7 * a - 9 / b + c";;
- : int = 23
# run "if true then 42 else 8";;
- : int = 42
```
