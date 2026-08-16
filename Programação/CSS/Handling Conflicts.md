
# Cascade

Se usarmos seletores exatamente iguais e mudarmos exatamente a mesma propriedade, a regra que será aplicada é a que vem por último.

# Specificity

> Seletores mais específicos tem mais prioridade a serem aplicados

Elemento < Classe < ID

# Inheritance 

> Algumas propriedades são herdadas pelos filhos

Exemplos
- `color`
- `font-family`

Não são herdados: `margin`, `pading`, `border`, `width`


# Inheritance Value Properties 

- `initial`
	- Define para o valor dafault do CSS
	- Pode ser diferente do padrão default do navegador
	- CSS toma prioridade em relação a estilo default do navegador
	
	- `color`:`initial` deixa cor do texto como default do CSS, preto

- `inherit`
	- Obrigado a herdar valor de propriedade do elemento pai
	- Util para propriedades que não herdam valores por default

- `unset`
	- Reseta a propriedade para seu valor natural
	- Se a propriedade for herdada age como `inherit`
	- Se a propriedade não for herdade age com `initial`
	- Pode ser feito para cancelar propriedades

- `revert`
	- Reverte a propriedade para o valor padrão do navegador do usuário

- `revert-layer`
	- Rever a propriedade para um valor aplicado na layer anterior


`all`: `<inheritance value>` 
 - pode ser usado para fazer com que todos os filhos tenha determinando inheritance value