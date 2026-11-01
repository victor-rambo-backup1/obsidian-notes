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

Premio

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

Tipos de Produção: Série, Filme, Especial

Consultas
1. GetTop10ProducoesMaisAssistidas

2. GetProducoesPorNome
	GetProducoesPorGenero
	GetProducoesPorProdutora
	GetProducoesPorAtor
	GetProducoesPorDiretor

3. GetProducoesExcetoPorNome
	GetProducoesExcetoPorGenero
	GetProducoesExcetoPorProdutora
	GetProducoesExcetoPorAtor
	GetProducoesExcetoPorDiretor

4. GetProducaoMaisAssistidaDeUmGenero

5. GetGeneroFavoritoUsuario
	GetUsuarioTipoProducaoPreferido

6. GetProducoesUsuarioAteData

7. ProduçõesMaisReassitidas

8. GetProduçoesQueUsuarioNãoViu

9. GetProduçõesMaisVistasQueUsuarioNãoVIU

10. GetProduçõesUsuárioNãoViuSãoSérie

11. GetSeriesComEpisodesComMenosQueDuraçãoX

12. GetSeríesPremiadas



