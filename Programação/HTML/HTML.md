
## Elemento

- Composto por:
    - Opening Tag: onde inicia o elemento, diz qual o tipo de elemento
    - Content: conteudo do elemento, em texto geralmente
    - Closing Tag: onde termina o elemento
- Exemplo:
    - `<p>I love my cat</p>`

## Void Elements

- Não possuem closing tag, nem conteudo
- Não podem ter outros elementos dentro de sí

## Tipos de Elementos

- `<em>`: itálico
- `<strong>`: negrito
- `<p>`: parágrafo
- `<br>`: quebra de linha
- `<hr>`: linha horizontal com quebra de linha
- `<a>`: transforma texto em links
    - `href`: link direcionado ao clicar
- `<label>`:
- `<link>`: especifica a relação entre a página e um recurso externo
- `<span>`:

## Character Reference

- Uma forma de representar caractéres especiais no HMTL
- `&lt;`: <
- `&gt;`: >
- `&quot;`: “
- `&apos;`: ‘
- `&amp;`: &

## Atributos

- Contem informações extras do elemento que não fazem parte do conteúdo
- `<Elemento Atributo1=valor1>`

## Estrutura HTML

- `<!DOCKTYPE html>`
    - Antigamente apontava para um arquivo para fazer verificação de definições gramaticais consideradas boas na época para o HTML
    - Hoje em dia virou artefato, esse é o formato mínimo para não gerar erro
- `<html>`
    - Engloba todo conteudo da página
    - `lang=`: Língua do conteudo da página, útil para SEO e para screen readers
- `<head>`
    - Contem metadados da página, informações que são importante para o navegador mas que não são conteúdo
    - `<meta charset="utf-8" />`: Configura o padrão do encoding dos caractéres para utf-8
    - `<title>`: O título da página HTML
- `<body>`
    - Contem o conteúdo da página

## Comentários

- `<!-- *comentário* -->`

## Meta

- Contem os metadados de uma página
- Uma mesma página pode conter vários elementos meta
- `meta charset=`: define o enconding da página
- `name=`: da um título ao metadado
- `content=`: descreve o conteudo do metadado
- Muito importante para SEO
    - No exemplo definimos o autor da página e descrição do conteudo da página, ajudando a search engine do browser
    
    ```html
    <meta name="author" content="Chris Mills" />
    <meta
      name="description"
      content="The MDN Web Docs Learning Area aims to provide
    complete beginners to the Web with all they need to know to get
    started with developing websites and applications." />
    ```
    
- Pode se adicionar também o icone do site usando
    - `<link rel="icon" href="<caminho do icone>" />`

## Adicionando CSS

- Usaremos o elemento link
- `<link rel="stylesheet" href="<caminho do icone>" />`
- Se o caminho possui `/` isso indicia que ele é em relação ao diretório raiz

## Heading

- Existem seis níveis de heading do h1 ao h6
- É fortemente recomendando que a ordem hierárquica sejá seguida, seria errado colocar h2 antes de h2
- É recomendado usar no máximo 3 heards de tipo diferente por página
- É geralmente recomendado usar um h1 por página
- Importante para SEO e screen readers

## Semantic Elements

- `<header>`: header
- `<nav>`: nagevation bar, permite navegar pelo site, leva para outras páginas
- `<main>`: conteúdo principal da página, possui subníveis:
    - `<article>`
    - `<section>`
- `<aside>`: sidebar, dentro da `main` geralmente
- `<footer>`: footer

## Non-Semantion Elements

- Priorizar o uso de elementos semánticos a não semánticos
- `<span>`: engloba uma linha
- `<div>`: engloba um bloco

## Lists

- `<ol>`: lista ordenada, números
    - `<li>`: marca cada elemento
- `<ul>`: lista desordenada, pontos
    - `<li>`: marca cada elemento
- `<dl>`: lista de descrição, recebe o texto e sua descrição
    - `<dt>`: description term, o texto a ser descrito
    - `<dd>`: description definition, a descrição do texto

## Bold, Italic, Underline

- `<em>`: itálico, passa ideia de enfase ao navegador
- `<i>`: itálico, não apresenta ideia de enfase
    - Nomes estrangeiros
    - Nomes ciêntificos
- `<strong>`: deixa em negrito, e passa ideia de importância ao navegador
- `<b>`: negrito, apenas destacado visualmente sem importância extra
    - Palavras-chave
    - Nome de produto
- `<u>`: underline
    - palavras escritas errado
- Dar prioridade ao uso de `<strong>` e `<em>`, impacta SEO

## Quotation

- Serve para citar outras fontes
- `<blockquote>`: cria um bloco de citação, sem aspas, com identação
- `<q>`: cria uma citação inline, com aspas
    - Ambos usam o atributo `cite=` que armazena o link da citação
    - Ele infelizmente não serve para muita coisa, nem SEO ou visualização

## Abreviation

- `<abbr>`: usado para indicar abreviação
- Pode ser usado sozinho ou com atributo `title=`, permite ao passar o mouse por cima falar oque a abreviação significa

## Address

- É mais um recurso semántico para o próprio programador
- É basicamente uma div
- Sinta-se livre para botar qualquer informação de contato dentro ou localidade
- Não impacta aparência ou SEO
- `<address>`

## **Superscript e Subscript**

- `<sup>`: Deixa caracteres pequenos e deslocados para cima
- `<sub>`: Deixa caracteres pequenos e deslocados para baixo
- Bom para fórmulas matemáticas, químicas, datas.

## Representando Código

- `<code>`: código genérico
    - Bom usar `<pre>` para manter identação
- `<pre>`: mantem espaços em brancos

## Data/Hora

- `<time>`: serve para o computador poder facilmente identificar as datas
    - `datetime=`: sintaxe específica para o computador ler facilmente

## Links

- `<a>` - Criar hyperlink
    - `href=`: url do recurso a ser carregado
    - `title=`: ao passar mouse por cima mostra um menssagem
    - `target= _blank`: abre recurso em uma nova página
- Pode ser usado para o embedding de images, textos, headers.
- Se botar `href` o id de um elemento, ao cliclar rola a página até ele
- Não botar a palavra link no link, pessoas conseguem ver que é um link e o screen reader vai dizer
- Para links não html, é interessante falar quando é dowload e caso vai abrir em uma nova guia
- Links internos na mesma página
- Links externos em nova página
- `href="mailto:*email*`: vai abrir para mandar um email

## Imagem

- `<img>`
    - `<src>:` link ou caminho para a imagem
    - `<alt>:` texto descrevendo para screen readers e SEO
- Sempre rostear as próprias imagens e recursos
- Jamais fazer imagens apontando para URLs de outros sites
    - Isso é antiético
    - Vai consumir recursos de outro servidor
    - O recurso pode ser removido
- Nunca botar texto dentro de imanges:
    - Não é copiável
    - Screen readers não vão conseguir ler
- `width`, `height` são usados para definir o tamanho de uma imagem
    - Indica para o browser qual tamanho da imagem antes do request, evita que os elementos da página sejam alterados de lugar
    - Nunca usar para aumentar tamanho da imagem, use editores ou CSS no lugar
- HTML é a melhor escolha se uma imagem tiver significado
- CSS é a melhor escolha para imagens puramente decorativas

## Alt Text

- Importante para
    - screen readers
    - SEO
    - browsers com imagens desabilitadas para economizar banda
- Se a imagem é decorativa não precisa ter alt, pode usar `alt=""`
- Não repetir texto no alt text, o screen reader vai ler duas vezes e vai ficar estranho
- `<title>` não é como o alt text, muitos screen readers não oferecem suporte

## Captions

- Já que legendas não deve ser postas em imagens devemos bota-las em texto
- O `<figure>` é superior a um `<p>` visto que relaciona cada imagem a uma legenda diretamente, ótimo para screen readers
- `<figure>`: um container que contem a `<img>` e o `<figurecaption>`
- Caption é diferente de alt
    - Caption seria uma legenda da imagem, diz oque é
    - Alt é pra ser uma descrição detalhada da imagem de forma física, para alguem que não possa ver

## Vídeo

- `<video>`: permite fazer o enbedding do vídeo na página
    - `src=`
    - `controls`: manda o navegador adicionar sua interface própria de controle de vídeo
- Alguns navegadores antigos podem não suportar a tag vídeo do HTML, por isso é importante fazer um fallback com um link direto para a mídia
    
    ```html
    <video src="rabbit320.webm" controls>
      <p>
        Your browser doesn't support HTML video. Here is a
        <a href="rabbit320.webm">link to the video</a> instead.
      </p>
    </video>
    ```
    
- Muitos formatos também não são suportados, por isso é importante fazer um fallback com diversos formatos, usando `<source>`
    
    ```html
            <video controls>
                <source src="mídia/rabbit320.webm" type="video/webm" />
                <source src="mídia/rabbit320.mp4" type="video/mp4" />
                <p>
                    Seu navegador não suporta videos HTML.
                </p>
                <a href="mídia/rabbit320.mp4">Vídeo</a>
            </video>
    ```
    
    - `type=`: o tipo da mídia, assim o navegor pode antecipadamente ver se ele oferece suporte ao formato, se não oferecer o request nem é feito
- `autoplay` apenas funciona se `muted` estiver ativado
- `poster=`: define imagem inicial para o vídeo, caso não ativado mostrará tela preta ou primeiro frame do vídeo
- `preload=`: define se deve ser pré-baixado apenas, o vídeo, os metadados do vídeo ou nada.

## Audio

- Opera da mesma forma que o elemento `<video>`

## Subtitles

- Legendas utilizam o formato `.vtt` de arquivo
- `<track>`: deve ser posto dentro do `<video>` ou `<audio>`
    - `kind=`: o tipo de track que vai ser, usaremos `subtitles`
    - `src=`
    - `srclang=`: a língua da legenda, exemplo: `br`
    - `label=`: o texto que aparece para o usuário na hora de selecionar, exemplo: `Português`

## Form

- `<form>`: é um wrapper para um forms
    - `action=`: caminho para onde deve ser mandado as informações
    - `method=`: o método do protocólo http que será usado

## Input

- `<input>`: colocado dentro do forms, um campo para prencher informações
    - `type=`: tipo de informação, faz verificação automática de tipo
        - `name`
        - `email`
        - `date`
        - `radio`
        - `time`
        - `color`
    - `placeholder=`: Texto dentro da caixa, geralmente dando instruções
    - `value=`: O valor default, ao abrir a página já aparece escrito
    - `name=`: O nome do atributo para onde a informação for mandada
    - `id=`: Especifica o ID do elemento, usado em `label`
    - `required`: Torna o campo obrigatório

## Label

- `<label>`: Relaciona um texto a um input
    - `for=`: o nome do `id` do input associado
    - Possível botar texto dentro do elemento
- Bom para screen readers
- Bom para usuários mobile, clicar no label seleciona o campo
- Pode ser feito de duas formas, implicito e explicito
- Implicito:
    
    ```html
    <label>
      Name (required):
      <input type="text" name="name" required />
    </label>
    ```
    
- Explicito:
    
    ```html
    <label for="name">Name (required):</label>
    <input type="text" name="name" id="name" required />
    ```
    
- É recomendada a forma explicita
    - Alguns screen readers se confundem com a forma implicita
    - Escala melhor em projetos

## Button

- `<button>`: um botão clicável em seu navegador
- Para adicionar funções a ele é necessário usar javascript
- Dentro de um form o botão automaticamente vira um botão com a função `submit` enviando o request
- Nunca usar botão de reset para forms, muitas pessoas clicam por engano

## Radio Input

- Bolinha de seleção onde só é possível escolher um elemento
- Combina com `<fieldset>`, um container que gera um caixa com uma legenda
    - `<legend>`: sobreo oque é a seleção no geral
    - `<div>`
- `type=radio`
- `name=` precisa ser igual para os radios inputs associados, se marcar em um desmarca no outro
- `value=` vai ser o valor que vai ser enviado ao selecionar uma das caixas, obrigatório
- `disabled` para desativar completamente um input
- `checked` para deixar opção ativada por padrão
    
    ```html
    <fieldset>
        <legend>Opções de Carro</legend>
        <div>
            <input 
                type="radio"
                name="carros"
                id="carroOpção1"
                value="fox fudido" />
            <label for="carroOpção1">Fox Fudido 0 R$</label>
    
            <input
                type="radio"
                name="carros"
                id="carroOpção2"
                value="Argo foda" />
            <label for="carroOpção2">ArgoFoda 1 R$</label>
        </div>
    </fieldset>
    ```
    

## Checkbox Input

- Seleção em caixas, permite escolher mais de uma opção
- `type=checkbox`
- Similar ao radio na implementação
- Não precisa de `value=`, retorna booleans usando o atributo `name`
    
    ```html
    <fieldset>
        <legend>Opções de Carro</legend>
        <div>
            <input 
                type="checkbox"
                name="fox"
                id="fox"
            <label for="fox">Fox Fudido 0 R$</label>
    
            <input
                type="checkbox"
                name="argo"
                id="argo"
            <label for="argo">Argo Foda 1 R$</label>
        </div>
    </fieldset>
    ```
    

## Select Input

- Abre uma caixa de seleção ao clicar, permite apenas escolher uma opção
    
    ```html
            <label for="carros">Tipo de carro: </label>
            <select name="carros" id="carros">
                <option value="">Selecione um valor</option>
                <option value="fox">Fox</option>
                <option value="argo">Argo</option>
            </select>
    ```
    

## Comments Input

- Um caixa de comentários onde pode ser escrito texto
- `<textarea>`
    - `rows=`: número de linhas
    - `cols=`: número de colunas

```html
<label for="comentario">Envie sua sugestão!!!</label>
<textarea name="comentario" id="comentario" cols="20" rows="5"></textarea>
```

## Tables

- Tables jamais devem ser usada para estruturar dados na página, CSS existe para isso
- `<table>`: marca o início e fim da tabela
- `<tr>`: marca cada linha da tabela
- `<td>`: marca cada célula da tabela
- `<colgrop>`: permite aplicar a css a cada coluna
    - `<col>`: cada elemento desses representa uma coluna
        - Uma tabela de seis colunas sem `span` deve ter seis `<col>`
        - `class=` para mudar o coluna via CSS
        - `span=` para que um `<col>` valha para mais colunas
        - exemplo: `<col span="2" />`, pula duas colunas