
- A lógica de join deve ficar fora dos elementos musicais 
- Alguma classe para transformar as letras do input em models
- Alguma classe para transformar o model em algo que o Jfugue consegue ler
- Parte da lógica do MusicContext vai ter que ir para uma nova classe representando as Vozes

- Pensar alguma forma em que mudar o dicionário dinamicamente não seja um inferno
- Seria melhor se os nomes relacionados a dict translator fosse agnostico ao tipo dict
- Dividir os dicts em grupos: notas, instrumentos
- Para passar por injeção de dependencia vai ter que ter alguma classe fábrica

- Como fazer as vozes?
- Se virar modelo, como armazenar musicContext
- Lógica das vozes só vai ser lidada nessa primeira parte

- Tradutor de texto para modelo 
- Dentro dele vive as 4 vozes 