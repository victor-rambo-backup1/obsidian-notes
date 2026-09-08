
# Log 

- `console.log(<text>)`: escreve no log
- `console.log("my variable is ${var}")`: substitui pelo valor da variável

- `window.alert(<text>)`: mostra uma caixa de alerta

# Loading Javascript

-     `<script src=<path defer></script>`
	- `defer`: baixa o javascript desde o início do carregamento mas só executa ele depois de todo o resto estiver carregado

# Select HTML

-  `document.getElementByID(<id>).textContent = variable`: muda texto do elemento HTML com o id selecionado
# Variables

- `let`
	- Pode ser mudada
	- Não precisa ser atribuido valor na criação 

- `const`
	- Não pode ser mudada
	- Precisa ser atribuida valor na criação

- `typeof <variable>`: retorna o tipo de valor da variável

# Input 

```js
document.getElementById("myButton").onclick = function() {
    username = document.getElementById("myInput").value;
    document.getElementById("myInput").value = null;
    console.log(username);
}
```

`.value`: input
`.textContent`: texto de elemento qualquer
# Type Conversion

> Todos os número em JS são tratados como floats com excessão de big ints

- `Number()`
	- Converter uma string para number retorna um `Nan`
- `String()`
- `Boolean`
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

