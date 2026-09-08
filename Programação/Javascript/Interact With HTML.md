
# Loading Javascript

-     `<script src=<path> defer></script>`
	- `defer`: baixa o javascript desde o início do carregamento mas só executa ele depois de todo o resto estiver carregado

# Select HTML

-  `document.getElementByID(<id>).textContent = variable`: muda texto do elemento HTML com o id selecionado

# Input 

```js
document.getElementById("myButton").onclick = function() {
    username = document.getElementById("myInput").value;
    document.getElementById("myInput").value = null;
    console.log(username);
}
```

`.value`: input
`.textContent`: texto de elemento 
