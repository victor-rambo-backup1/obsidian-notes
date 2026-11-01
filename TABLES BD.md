___

## Netflix

# 1.0

Filmes
Series
Episodios
Atores
Diretores
Produtora
Generos

# 1.1

Usuario
codu, 

Produções
codp, data_lancamento, visualizações, curtidas, 

Atores 
coda, nome, idade

Diretores
codd, nome, idade

Produtora
codpr, nome, ano_criação

Generos
nome_genero,

ProducaoGenero
codp, nome_genero

ConteudoProdução
codp, nome_producao, duracao_producao,

AlocacaoProducaoAtor
codp, coda

AlocacaoProducaoDiretor
codp, codd

AlocacaoProducaoProdutora
codpr, codp



Consultas
1. GetTop10ProducoesMaisAssistidas

2. GetProducoesPorNome
	GetProducoesPorGenero
	GetProducoesPorProdutora
	GetProducoesPorAtor
	GetProducoesPorDiretor

3. GetProducaoMaisAssistidaDeUmGenero

4. GetGeneroFavoritoUsuario
	GetUsuarioTipoProducaoPreferido

5. GetProducoesUsuarioAteData


