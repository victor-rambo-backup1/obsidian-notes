
Um software possui fatores internos e externos

- `Externo`: Velocidade, facilidade de adaptação e uso.
    - Ligado ao usuário final no geral
- `Interno`:   Legibilidade, modularidade
    - Ligado ao programador

O usuário final não liga para as qualidades internas de um software, visto que apenas as externas o impactam. Todavia, as qualidades internas de um programa são meios para melhorar as qualidades externas.

## Review dos Fatores Externos

---

#### **Correctness**

- A capacidade de um software executar a tarefa específica para qual ele foi criado

Ideia de layers, para o programa estar correto é suposto que o compilador está correto. É suposto que as bibliotecas estão corretas. Não é a mesma coisa que confiar cegamente, mas é separado as responsabilidades entre corretude de diferentes camadas do programa.

#### Robustness

- O quão bem o programa consegue lidar com casos especiais, casos não previstos numa execução ideal do programa

Robustez não é sobre estar preparado para todas as exceções do universo, mas sim lidar bem com situações consideradas anormais. 

Entre as qualidades de um programa robusto estão: não crashar em situações inesperadas, mensagens de log significativas e termina execução de forma limpa.

#### Extendibility

- O quão fácil é adicionar ou modificar um software

Extensibilidade se apoia na ideia de que apesar de um software ser desenvolvido pensando em determinada finalidade, é provável que essa finalidade tenha que ser eventualmente adaptada para as necessidades do presente.

Os principais fatores que influenciam a extensibilidade de um software é sua a simplicidade e modularidade.

#### Reusability

- O quão fácil é reusar parte de um software.

Reusabilidade é essencial na indústria de software visto que grande parte das aplicações desempenham funções similares. Assim, podemos gastar menos tempo escrevendo código novo e mais tempo melhorando as outras qualidades citadas.

#### Compatibilidade

- O quão fácil é um programa se comunica com outro

Compatibilidade é baseada em uma padronização do modo de comunicação como:

- Formato de arquivo padronizado
- Estruturas de dados padronizadas
- Interfaces padronizadas

#### Efficiency

- Habilidade de um software de rodar gastando poucos recursos de hardware como memória RAM, memória de disco, tempo de processador e banda larga de internet.

Os programadores geralmente ou são loucos por eficiência ou tendem a ignorar ela. É importante ter uma visão realista 

Eficiência é importante pois:

- Entidades que compraram máquinas mais potentes querem poder resolver problemas novos ou mais problemas e não somente os mesmos problemas devido a má otimização
- Algoritmos com péssima complexidade vão muito provavelmente rodar mal independente da máquina
- Eficiência pode muitas vezes afetar a corretude do problema, com velocidade sendo uma necessidade

#### Portability

- A habilidade mede o quão preso a um determinado sistema ou hardware um determinado software está.

#### Ease of Use

- O quão fácil é de se utilizar um determinado software

No geral um sistema bem construído, bem estruturado, naturalmente será mais fácil de usar

Um software precisa conhecer seu público alvo, todavia um software bom provavelmente vai superar esse público, o ideal é fazer o menor número possível de predições em relação ao usuário

#### Functionality

- O quão rico o software é em diferentes possibilidades de uso

É muito comum programadores se perdem na adição de novas funcionalidades, implementando utilidades que agregam pouco valor ao programa ou negligenciando as outras qualidades no código.

Um fluxo muito comum que deve ser desincentivado é a adição excessiva de funcionalidades para a posterior correção do código, isso provavelmente causará um grande estresse no final do projeto e em caso de encurtamento de prazos pode levar a entrega de um produto com nível de qualidade muito a baixo.

O ideal seria tentar ao máximo possível manter as qualidades do código e só passar para a próxima funcionalidade quando a anterior estiver num nível agradável.

#### Timeliness

- É o timing do tempo de lançamento do software em relação ao interesse do público.

De nada adianta lançar um projeto incrível mas que a demanda era de seis meses atrás.

## Documentation

---

Uma boa documentação ajuda a manter as qualidades mencionadas acima, podemos dividi-las em três grupos:

- `Documentação Externa`: Para o usuário, como usar o software
- `Documentação Interna`: Para o programador, explica a estrutura e implementação do código
- `Documentação de Interface`: Para o programador, explica oque o módulo faz sem entrar em grandes detalhes sobre implementação

Vale notar que um programa com as qualidades acima diminui a necessidade de documentação, mas não a elemina, visto que uma boa UI diminui a necessidade de um manual de usuário e um bom código é lógico e significativo.

## Maintenance

---

A maior parte do custo de produção de um software é gasto em sua manutenção, sendo os principais a adição de novas funcionalidades e alteração de tipos de dados. As qualidades acima permitem que a manutenção ocorra de forma muito mais rápida e barata, por meio de:

- Documentação automática via ferramentas externas
- Maior extensibilidade permite adição de funções de forma mais rápida
- Maior reusabilidade implica em código menos ligado, facilitando alterar tipos de dados