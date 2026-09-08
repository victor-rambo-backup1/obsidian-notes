
`...`: Permite passar quantos argumentos quiser, o JS vai empacota-los em uma lista

> Tipo \*args do python

```js
function printNames(...names) {
    console.log(names)
}

printNames("Victor", "Raissa", "Isadora");
```