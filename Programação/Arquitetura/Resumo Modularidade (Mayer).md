
# Five Criteria

### Decomposability
- Poder dividir um problema em subproblemas
- Top-view: Ir de uma abstração muito grande e ir diminuindo o nível até que a implementação seja possível

### Composability 
- Poder juntar módulos para poder resolver novos problemas
- Modulos muito decompostos podem estar muito próximos da implementação, podendo dificultar composição 

### Understandability
- A lógica dos modulos e de como o sistema é organizado deve seguir a lógica do domínio, para gerar familiaridade e facilitar a compreensão 

### Continuity
- Modificar os módulos não deve ser algo muito difícil e não deve causar um efeito cascata entre diversos módulos, afetando no máximo os vizinhos

### Protection 
- Situações anormais dentro de módulos devem ser identificados e tratadas dentro dele e não arrastadas pela cadeia lógica inteira



# Five Rules

### Direct Mapping
- A lógica do software deve seguir uma correspondência com a lógica do domínio

### Few Interfaces
- Os módulos devem se comunicar o mínimo possível entre sí 
- Evitar comunicações estranhas, bidirecionais

### Small Interfaces
- Se dois módulos se comunicam é interessante eles trocarem o mínimo de informação possível, apenas o necessário

### Explicit Interfaces
- Quando módulos compartilham informação, é relevante que seja explicito essa relação
- Ruim seria silenciosamente só alterar parâmetro do outro

### Information Hiding
- Tudo relacionado a implementação deveria ser privado
- Se um módulo for fortemente dependente da implementação do outro, mudanças serão um inferno


# Five Principles

### Linguistic Modular Units
- É interessante que um módulo corresponda a uma unidade lógica de uma língua

### Self-Documentation
- A documentação interna deve estar junto ao código
- Criar uma documentação separada aumenta a chance dela não ser mantida de forma adequada

### Uniform Access
- Quando preciso pegar um valor, a forma de chamar o valor deveria ser independente de o valor for um atributo de uma classe ou um método
- Isso facilita migrar entre soluções que priorizam computação ou armazenamento.

### Open-Closed
- Uma classe deve estar sempre aberta adições 
- Um modulo só deve ser considerado fechado quando estiver bem definido, isso é possui interface e implementação
- Uso de herança para criar copias especificas para caso sem tornar código redundante


### Single Choice
- Quando tiver diferentes possibilidades de escolha, apenas uma classe deve ter acesso a essa lista, assim se precisarmos mudar algo é apenas em um lugar.