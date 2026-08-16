
`git status`
 - Quais arquivos foram alterados, excluidos, modificados

`git add`
- Passa arquivo do `working directory` para o `stage`

	`git add -A`
	- Passa todos os arquivos do projeto para `stage` 
	
	`git add .`
	- Passa todos os arquivos da pasta para `stage`

`git rm <file>`
- Exclui o arquivo e faz a exclusão entrar no `stage`

`git reset`
- Tira somente as mudanças do `stage`

	`git reset --hard`
	- Faz o `working directory` voltar para o estado do commit anterior

`git commit`
- Passa arquivo do `stage` para o `commit`

`git log`
 - Mostra todo o histórico de commits

	`git log --oneline`
	 - Mostra todo o histórico de commits de forma resumida
	 - Bom para descobrir os ids dos commits