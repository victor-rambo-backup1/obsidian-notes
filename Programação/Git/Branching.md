
`main`: A branch principal do projeto
 - Antigamente era chamada de `master`

`origin`: O nome padrão do repositório remoto

`HEAD`: 
- Aponta para o commit atual, logo aponta para a branch atual 

`Merge`: combina os conteúdos de duas branches em uma só

`git branch`
- Cria nova branch

`git switch`
- Muda de branch
- Pode gerar conflitos ao trocar entre branches se não tiver commitado a branch


`git merge`
- Executado da branch que vai receber as atualizações


### Como Passar um branch remota para local?

```bash
git fetch origin
git switch -c nome-da-branch --track origin/nome-da-branch
```

O `Working Directory` só mostra os arquivos da branch atual, escondendo os arquivos das outras branches