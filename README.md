# PUC-MBA
Trabalho de conclusão do MBA PUC-Rio

## TEMA CENTRAL
Este trabalho tem por ideia central a utilização de metodologias já difundidas para calcular uma pontuação (score) com relação à igualdade de gênero para todos os municípios brasileiros. Baseada nos critérios apresentados pelo índice GGI - Global Gender Gap Index, a ideia central é partir desta nova variável – somada às demais variáveis escolhidas - encontrar agrupamentos e características que permitam distinguir perfis de cidades que possuem maior igualdade de gênero.

## OBJETIVO:
* Analisar quais perfis de municípios brasileiros são possíveis distinguir com relação à igualdade de gênero.

## BASE DE DADOS:
A base de dados foi construida pela autora, é resultado de uma composição de três fontes distintas: 

**Dados para construção do score de gênero:** Censo 2010- IBGE, Tribunal Superior Eleitoral (TSE) – Eleições 2010 (governadores e senadores), Tribunal Superior Eleitoral (TSE) – Eleições 2008 (prefeitos e vereadores).

**Dados básicos municipais:** publicados do Altas de Desenvolvimento Humano (IPEA, 2013), que consolida os principais dados do censo 2010 realizado pelo IBGE, a nível municipal.

**Dados gerais municipais:** obtidos através de raspagem de dados no site IBGE cidades (https://cidades.ibge.gov.br/brasil). 

## METODOLOGIA
Após avaliação e tratamento dos dados faltantes na base de dados, a base foi padronizada para posterior utilização nos algoritmos selecionados: K-Means e Agglomerative Clustering. Foi utilizada uma abordagem de otimização de hiperparâmetros para verificação do número de clusters ideais para cada algoritmo e avaliados através do método Silhouette e Elbow, identificou-se que o numero mais adequado para este dataset seria 3 clusters.

![](Imagens/Clusters_kmeans_silhouette.png) ![](Imagens/Clusters_ward_silhouette.png)

## APLICAÇÃO DOS ALGORITMOS
### 1. K-Means
Ao aplicar o K-Means, usando os dados padronizados e como parâmetro n_clusters=3, observou-se uma grande concentração de cidades nos clusters 0 e 1 e apenas duas cidades no cluster 2 (Rio de Janeiro-RJ e São Paulo-SP). Para melhor visualização dos dados, foi aplicado o PCA para redução de dimensionalidade.

![](Imagens/scatter_kmeans.png) 


A divisão de quantidade de cidades por região e cluster segue detalhada na tabela abaixo:

| Região       | Cluster | Qtd Municípios |
|--------------|---------|----------------|
| Centro-Oeste |       0 |             52 |
| Centro-Oeste |       1 |            336 |
|     Nordeste |       0 |           1709 |
|     Nordeste |       1 |             85 |
|        Norte |       0 |            384 |
|        Norte |       1 |             65 |
|      Sudeste |       0 |            230 |
|      Sudeste |       1 |           1436 |
|      Sudeste |       2 |              2 |
|          Sul |       0 |             47 |
|          Sul |       1 |           1219 |

Podemos observar também que regiões Norte e Nordeste possuem a maioria dos seus municípios classificados como Cluster 0, enquanto que nas demais regiões, a maioria dos municipios foi classificada como Cluster 1. O gráfico abaixo mostra a quantidade de cidades por cluster em cada Região e Estado.

![](Imagens/Clusters_kmeans_regiao.png)

##### 1.1. Principais atributos encontrados na análise PCA


### 2. Agglomerative Clustering

## RESULTADOS
