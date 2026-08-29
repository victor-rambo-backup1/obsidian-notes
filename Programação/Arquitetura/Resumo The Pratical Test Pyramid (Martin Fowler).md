[[OOSC-Cap1-Quality.pdf]]
# Continuos Integration (CI)

- Teste automatizados
- A cada push no código os testes são executados automaticamente
- Só integra a codebase se tiver passado em todos os testes

# Continuos Delivery (CD)

- Ao passar no CI, automaticamente constroi uma nova versão do projeto
- Pode fazer deploy em um click

# Continuos Deployment

- Continuos delivery com deploy automático

O programa deve sempre priorizar a quantidade de teste de baixo nível

Quanto mais alto nível, como testes end to end, menos testes

# Unit Tests

- Testa uma unidade do código
- Uma unidade pode ser considerada: uma função, método ou classe

# Test Doubles

- `mock`: verifica a interação com o objeto, verifica se os argumentos são válidos
- `stub`: apenas retorna oque foi pré-programado para retornar

# When to Always Mock and Stub

- HTTP requests
- Database requests
- Arquivos

# TDD - Test Driven Development

Uma forma de produção baseada na produção de testes

1. Listar cenários adversos para o novo recurso 
2. Criar um teste para esse item da lista
3. Testar o teste, se ele falhar quer dizer que o teste provavelmente funciona
4. Escrever o código da forma mais simples possível, código não elegante e hardcode é aceitável agora
5. Verificar se o teste passa
6. Refatorar o código do recurso até atingir o nível de qualidade desejado
7. Repetir o passo 2 para implementar novas funcionalidades

# Dicas Unit Test

- Um unit test por classe tende a ser uma regra base ok para se guiar
- Um unit test não deveria ser tão próximo da implementação, ele provavelmente irá quebra durante o refatoramento
- Testar oque é observável os resultados e não a implementação, a lógica
- Métodos privados são fortemente atrelados a implementação e não devem ser testados
- Não testar código trivial, getters, setters, lógica estupidamente simples
- Devem ser testados melhores e piores casos


# Unit Test Types

- `Sociable`: 
	- É permitido que interaja com colaboradores 
	- Não precisa fazer mock/stub de todas dependências

- `Solitary`:
	- Não é permitido que intereja com colaboradores 
	- Precisa fazer mock/stub de todas dependências

# Unit Test General Structure

1. Coletar dados de teste
2. Chamar o método, função, classe passando os dados como argumento
3. Verificar se o resultado era o esperado