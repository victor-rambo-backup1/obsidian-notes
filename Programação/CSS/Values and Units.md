
# Lenghts 

### Unidades Absolutas

> Sempre representam o mesmo valor 

- `px`: representam um pixel
- `cm`: representam um centímetro
- Importante notar que um pixel ou centímetro em CSS não é necessariamente equivalemente a sua medida na vida real
- Unidades absolutas no geral são iguais independente de dispostiivo

### Unidades Relativas

> Mudam com base em algum aspecto definido

- `em`: relativo ao tamanho de fonte do elemento ou, do pai do elemento quando usado em `font-size`
- `rem`: relativo ao tamanho de fonte do elemento raiz 
- `vh`: relativo ao tamanho vertical do viewport
- `vw`: relativo ao tamanho horizontal do viewport

`rem` evita efeito cascata de aumento de fonte, diferente do `em` 


# Porcentages

- São tratados com `lenghts` no geral 
- Valor relativo a algo, geralmente o objeto pai
- `width: 20%` -> 20% da largura do objeto pai

# Colors 

> É sugerido usar o mesmo formato de cores atravez de todo o projeto

### Hexadecimal RGB

- Um `#` + `6 caracteres`, cada par de caracteres representa um canal rgb
- Usar valor hexadecimal diretamente na propriedade

### RGB

- 3 valores que vão de 0 a 255, representando os canais, `red`, `green`, `blue`
- Precisa usar a função `rgb()`
- Pode usar `rgba()`, com o ultimo valor indo de 0 a 1, definindo a opacidade


# Image

- `url(<caminho-da-imagem>)`: acessa imagem via CSS



