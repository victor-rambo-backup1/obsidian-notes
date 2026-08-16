
## Ideais novas que aprendi:

- Quando o código tiver argumentos de mesmo tipo, pode ser benéfico botar eles numa struct ou classe, fica mais legível e diminui duplicação de código com funções e métodos;
- Ao invés de passar parametros de uma classe, pode ser mais benéfico passar a classe inteira;
- Ao invés de chegar null, podemos criar um NullObject, que tem como função fazer nada basicamente. Isso deve ser usado apenas quando null é um resultado esperado, quando null for um erro deve fazer o if do null;
- Se todos as condições retornam a mesma coisa, é melhor passar todas as condições para um método separado e só fazer if dele;
- Classes são trabalhosas de serem mantidas, se não fizer sentido melhor desfazela;
- Uma classe que só serve para guardar dados com getter e setters provavelmente é ruim, visto que a lógica de programação dela vai estar fora dela.
- Se for do mesmo tipo usar herança, se ele apenas precisa/usar tipo usar delegação

## Ideias que reforcei:

- Se um método é usado mais em um outra classe do que na própria classe de origem, faz sentido passar para a outra classe;
- Não faz sentido eu criar variáveis dentro de classes, apenas para elas serem usadas em um caso muito específico, é melhor passar como argumento;
- Pode ser benéfico transformar um método em uma classe própria, com o init dela sendo as variáveis necessárias, poluindo menos os métodos;
- Ao invés de usar herança podemos usar delegação, destruindo a herança e criando uma classe dentro do filho;
- No geral é melhor funções parametrizadas do que fixas.
- A lógica de uma classe deve estar dentro dela
- Nó geral o fluxo de classes deveria seguir uma linha, um vai e vem será um inferno de entender e manter.
- Não fazer fluxos bidirecionais