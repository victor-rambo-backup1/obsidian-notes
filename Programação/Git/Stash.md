`git stach`
- Salva a branch numa pilha temporaria
- Permite trocar de branch sem commitar 

`git stash pop`
- Importante trocar para a branch certa 
- Pega a ultima alteração salva na stash e tenta fazer merge na branch atual
- Da pop na pilha 

`git stash apply`
- Tenta fazer o merge na branch atual mas não da o pop, deixa guardado

`git stash list`
- Mostra todos os estados armazenados na pilha