
## Selectors

- Selecione um elemento HTML usando `<elemento> {}`
- Selecione múltiplos elementos HTML usando `<elemento>, <elemento> {}`
- Selecione uma classe usandoa `.<clase> {}`
- A alteração que fica é sempre a última útil para retrocompatibilidade

## Specific Selectors

- Selecione somente um elemento contido em outro
    - `<elemento> <elemento> {}`
- Selecione somente o elemento que vem após o outro
    - `<elemento> + <elemento> {}`

## Styling Based on State

- Podemos mudar o estado específico de determinado elemento
- `a:link {}`: muda o estilo de um link que ainda não foi clicado
- `a:visited {}`: muda o estilo de um link que já foi clicado
- `a:hover {}`: muda o estilo do link ao passar o mouse por cima

## Funções

- `calc()`: executa aritimética básica
    - `width: calc(100px - 80px);`
- `rotate`: permite rotacionar elementos
    - `transform: rotate(0.8turn)`

## @Rules

- Lógica condicional básica para executar CSS
- `@media (width <= 300px) {}`: executa o CSS só se o viewport do navegador tiver larguar menor que 300 pixels

## Comentários

- `/* */`

## Targeting Classes

- Imagine uma classe chamada `big`
- `.big {}`: seleciona qualquer elemento que tenha como sua classe `big`
- `h1.big {}`: seleciona qualquer `h1` que tenha como sua classe `big`
- `h1 .big {}`: seleciona qualquer sub-elemento de `h1` que tenha como classe `big`
- Imagine agora outra classe `long`
- `.big.long {}`: seleciona apenas os elementos que tenham como suas classes `big` e `long`

## ID

- Pode ser usado apenas uma vez por página
- `id="nome id"`
- Para selecionar um id usamos:
    - `#<nome-do-id> {}`

## Selector Lists

- Se quero aplicar todas as propriedades as classes `big` e `long` é possível:
    - `.big, .long {}`

## Universal Selector

- `* {}`: seleciona todos os elementos de uma página
- `h1 * {}`: seleciona todos os elementos dentro de `h1`
- `h1 *:first-child {}`: aplica o estilo somente ao primeiro elemento dentro de `h1`

## Atribute Selector

- Podemos usar para selecionar apenas elementos que possuem determinado atributo
- `a[href] {}`: seleciona apenas ancoras que possuem um atributo href dentro de sí
- `a[href="https://www.youtube.com/"]`: seleciona apenas as ancoras com atributo href que leva ao site do youtube
- `a[href^="https"] {}`: seleciona apenas ancoras com href que começem com https
- `a[href$=".com"] {}`: seleciona apenas ancoras com href que termine com .com
- `a[href*="you"] {}`: seleciona apenas ancoras com href contendo a substring `"you"`
- `a[href~="you"] {}`: seleciona apenas  ancoras com href contendo a palavra `"you"` na string, não seleciona substrings

## Combinator Selector

- Seleciona apenas elementos que tenham relações específicas com outros elementos
- `div p {}`:  seleciona qualquer elemento `p` que seja filho de `div`, não precisa ser filha direta
- `div > p {}`: seleciona qualquer elemento `p` que seja filho direto de uma `div`
- `div ~ p {}`: seleciona qualquer elemento `p` que esteja em um mesmo grau de identação que uma `div`
- `div + p {}`: seleciona qualquer elemento `p` que esteja diretamente abaixo de uma `div`

## Pseudo Class Selector

#### Links

- `a:link {}`: aplica o estilo a links que não foram clicados ainda
- `a:visited {}`: aplica o estilo a links que já foram visitados
- `a:hover {}`: aplica o estilo ao link ao passar o cursor por cima
- `a:focus {}`: aplica o estilo ao link que está no foco ao apertar o tab
- `a:active {}`: aplica o estilo ao link entre o intervalo de apertar o link e carregar a nova página

#### Inputs

- `input:focus {}`: aplica o estilo ao input ao passar o cursor por cima
- `input:required {}`: aplica o estilo aos inputs obrigatórios
- `input:checked {}`: aplica o estilo a `checkbox` e `radios` que estão selecionadas
- `input:disabled {}`: aplica o estilo aos inputs desativados

#### Position

- `a:first-child {}`: aplica o estilo ao primeiro link filho dentro de um container pai
- `a:last-child {}`: aplica o estilo ao último link filho dentro de um container pai
- `a:nth-child(n) {}`: aplica o estilo ao `n` link filho dentro de um container pai
- `a:nth-child(even) {}`: aplica o estilo aos links filhos pares dentro de um container pai
- `a:first-of-type {}`: aplica o estilo ao primeiro link presente dentro de um container pai
- `a:last-of-type {}`: aplica o estilo ao último link presente dentro de um container pai

Pseudo Element Selector

- `a::before {}`: insere a string especificada no início e aplica o estilo
    - `content: "->"`: vai escrever o → com estilo aplicado antes do restante do texto
- `a::after {}`: insere a string especificada no fim e aplica o estilo
- `a::first-letter {}`: aplica o estilo apenas para a primeira letra do texto
- `a::first-line {}`: aplica o estilo apenas para a primeira linha do texto