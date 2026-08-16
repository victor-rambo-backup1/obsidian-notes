

`git checkout <commit-id>`
- Permite voltar o projeto para o estado de commits anteriores

`git diff <commit-id> <commit-id>`
- Mostra as linhas alteradas e oque foi alterado entre as duas versões 

`git restore`
- Retorna para versão do último commit

	`git restore <file>`
	- Retorna arquivo para estado do último commit

	`git restore .
	- Retorna repositório local para estado do último commit

	`git restore --staged .
	- Retorna repositório local para estado do último commit



`git revert <git-commit>`
- Retorna o estado do repositório local para commit desejado, criando um novo commit

> `revert` é bem mais recomendado que `reset`
- `revert`: cria novo commit mudando para commit antigo
- `reset`: apaga commits até chegar no commit desejado


`git rebase`
- Aplica todos os commits de uma branch na branch atual

`rebase`: 
- Pega todos os commits e aplica sucessivamente, um por um, na branch atual
- Não gera um commit separado
- Não usar quando múltiplas pessoas estão trabalhando na mesma branch ao mesmo tempo

`merge`: 
- Cria um novo commit que reune os dois históricos de commit
- Gera um commit separado