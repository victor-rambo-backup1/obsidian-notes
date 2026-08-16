
# Block

- Quebra em nova linha
- Respeita `widht` e `height`
- Padding, margin, border vão empurrar outro elementos
- Sem `width`especificada a caixa vai prencher todo espaço horizontal do container
- Prenche todo o espaço disponível em uma linha por padrão

>  `h1`, `p` usam block por default 
# Inline

- Não quebra linha
- `width` e `height` não tem efeito
- Padding e border de cima e baixo não afetaram outros elementos verticais, causando overlap
- Padding, border, margin afeta elementos horizontais adjacentes
- Prenche apenas o espaço horizontal do texto

> `a`, `span`, `em`, `strong` usam inline por default
# Outer Display

> Determina como o elemento irá interagir aos elementos ao redor

- `Block`, `Inline`

# Inner Display

> Determina como os elementos dentro do container iram interagir entre sí

- `Flex`

# Box Parts

- `Content`: Espaço para o conteúdos
	- `Width`
	- `Height`
- `Padding`: define a distância do conteúdo para a borda
- `Border`: define o tamanho da borda
- `Margin`: define a distância da borda para outros elementos

# Margin Collapsin

- Duas margens positivas vão se unir e pegar o valor da maior
- Duas margens negativas vão se unir e pegar o valor da menor
- Uma margem positiva e negativa vão se subtrair

# Border

- Em box model padrão a border não faz parte do conteúdo
- Em box model alternativa, `border-box`,  a borda pega espaço do conteudo, definida por `witdh` e `height` 

# Padding

- Qualquer imagem de background do elemento aparecerá no padding
- Não pode ter padding negativo
# Inline-Block

> Uma mistura entre display block e inline

- Não quebra linha
- Respeita `padding`, `border` e `margin`

# Outros

- width: `min-content` 
	- 
- width: `max-content`


















