
# Log 

- `console.log(<text>)`: escreve no log
- `console.log("my variable is ${var}")`: substitui pelo valor da variável

- `window.alert(<text>)`: mostra uma caixa de alerta


# Variables

- `let`
	- Pode ser mudada
	- Não precisa ser atribuido valor na criação 

- `const`
	- Não pode ser mudada
	- Precisa ser atribuida valor na criação

- `typeof <variable>`: retorna o tipo de valor da variável

# Type Conversion

> Todos os número em JS são tratados como floats com excessão de big ints

- `Number()`
	- Converter uma string para number retorna um `Nan`
- `String()`
- `Boolean()`
	- Converter uma string não vazia para Boolean retorna `True`


# Random 

> Usar Math.random()


# Ternary Operator

`age <=18 ? "You are a adult" : "You are a minor"`
- `?`: resultado se for verdadeiro
- `:`: resultado se for falso


# Switch

> Switch statements podem ser usados para verificar se condições são verdadeiras

```js
switch(True) {
	case age <= 60:
		text = "you are old"
		break;
	case age <= 18:
		text = "you are an adult";
		break;

}
```


# String

- `.padStart(20, "0")`: prenche o início da string com 0 até chegar a 20 caracteres
- `.padEnd(20, "0"`: prenche o fim da string com 0 até chegar a 20 caracteres

- `.slice(<start>, <end>)` 
	- pega a subtring começando no start até o end (não inclusivo)
	- Se não botar end vai até o final da string

# Strict Equality 

`===`: compara se o valor é igual e o tipo do dado é igual


# Functions 

`function MyFunc() {}`


# For Loop

`for (let animal of animals) {}`


# Spread Operator

`...`: Separa objetos iteráveis, como strings e listas, em elementos separados

```js
let nums = [1, 2, 3];
let maxNum = Math.max(...nums);
```

> Pode ser usado para concatenar listas

```js
let nums1 = [1, 2, 3];
let nums2 = [4, 5, 6];

let nums = [...nums1, ...nums2];
```


# Rest Parameters

`...`: Permite passar quantos argumentos quiser, o JS vai empacota-los em uma lista

> Tipo \*args do python

```js
function printNames(...names) {
    console.log(names)
}

printNames("Victor", "Raissa", "Isadora");
```

# Callbacks

> Passar uma função como argumento para uma função


```js
function addTwoNumbers(callback, num1, num2) {
    let sum = num1 + num2;
    callback(sum);
}

function printNum(num) {
    console.log(num);
}

addTwoNumbers(printNum, 1, 2);
```
