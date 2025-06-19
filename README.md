# Consumo de Energia Global
### Análise do Consumo de Energia Global

Sejam bem-vindos ao projeto Global_Energy_Consumption. Nesse projeto estarei mostrando a vocês os insights obtidos através da análise de dados do [arquivo CSV](https://github.com/Rafael-Leandro/Global_Energy_Consumption/blob/main/global_energy_consumption.csv).
Logo abaixo estarei mostrando mais informações das etapas do projeto.

## Apresentando a Problemática
O consumo de energia global tem crescido exponencialmente nas últimas décadas, impulsionado pelo aumento populacional, pela urbanização e pela expansão da atividade industrial. Esse crescimento descontrolado apresenta sérios desafios, como o esgotamento de recursos naturais, o aumento da emissão de gases de efeito estufa e a pressão sobre as redes de fornecimento de energia. Além disso, há uma grande desigualdade no acesso à energia entre países desenvolvidos e em desenvolvimento. Nesse contexto, a análise de dados torna-se uma ferramenta essencial para a gestão eficiente da demanda energética, permitindo a formulação de políticas sustentáveis e o uso racional dos recursos. [Ver mais](https://github.com/Rafael-Leandro/Global_Energy_Consumption/blob/main/Problem%C3%A1tica%20-%20Consumo%20Global%20de%20Energia.pdf)

## Sobre a base de dados
O Conjunto de Dados de Consumo Global de Energia fornece insights abrangentes sobre o uso de energia em diferentes países e setores nas últimas duas décadas. O conjunto de dados visa auxiliar pesquisadores, analistas de dados e formuladores de políticas a compreender os padrões de consumo, identificar regiões de alto consumo e analisar o impacto da adoção de energias renováveis e das emissões de carbono.

## Coleta de dados
Este conjunto de dados é do tipo estruturado e se encontra em formato CSV. A coleta dos dados foi feita através do download direto do dataset existente na plataforma Kaggle. [Ver fonte de dados](https://www.kaggle.com/datasets/atharvasoundankar/global-energy-consumption-2000-2024/data)

## Modelagem de dados
Após o download do conjuto de dados foi utilizada a plataforma do Google Colab para fazer a modelagem e o tratamento dos dados. 
Foi feita a verificação inicial utilizando os comandos:
```
print(df.shape)
print(df.isnull().sum())
print(df.duplicated().sum())
print(df.dtypes)
```
Através dessa verificação inicial foi constatado que o conjunto de dados apresentava a quantidade de 10.000 linhas e 10 colunas, não apresentou nenhum valor nulo, não apresentou nenhum valor duplicado e foi identificado o tipo de dado para cada uma das colunas, respectivamente. Caso fosse encontrado algum valor nulo ou algum valor duplicado seria necessário utilizar os comandos "df.dropna()" e "df.drop_duplicates()" para fazer a remoção desses dados e assim deixar a análise mais precisa. Também é importante destacar que caso alguma coluna do conjunto de dados estivesse com a tipagem diferente do esperado, por exemplo, uma coluna com números decimais sendo tratada como "string" ao invés de "float", seria necessário utilizar o comando "df = df.astype({"NOME_COLUNA": TIPO_DADO})" para alterar a sua tipagem e assim evitar erros durante a análise.

## Análise dos dados
Através da [análise exploratória](https://github.com/Rafael-Leandro/Global_Energy_Consumption/blob/main/An%C3%A1lise%20Explorat%C3%B3ria%20-%20EDA.ipynb) realizada no arquivo foi possível identificarmos insights relevantes como, os países que têm o maior consumo de energia, aqueles que possuem a maior taxa de emissão de gás carbônico e também aqueles que possuem uma dependência de combustível fóssil maior que a média encontrada. Além disso, também foi possível realizar uma análise individual de cada país como, por exemplo, os EUA que apresentou a maior média de consumo de energia para o ano de 2016 e teve a sua menor média de consumo para o ano de 2005. Após a análise exploratória foi realizada a [correlação](https://github.com/Rafael-Leandro/Global_Energy_Consumption/blob/main/Correla%C3%A7%C3%B5es.ipynb) entre as colunas e apresentado gráficos utilizando as bibliotecas "matplotlib.pyplot" e "seaborn". Depois dessas etapas realizadas foi elaborado o [relatório da análise dos dados](https://github.com/Rafael-Leandro/Global_Energy_Consumption/blob/main/Relat%C3%B3rio%20da%20An%C3%A1lise%20de%20Dados.pdf), informando os principais achados da análise, a relevância dos achados e também apresentando sugestões de ações.

## Dashboard e visualização
Para a visualização dos dados de maneira mais adequada foi elaborado um dashboard no Google Looker Studio onde podemos ter uma visão geral do consumo de energia global além de outros aspectos como o ranking de países que mais emitiram gás carbônico ao longo dos anos, com um filtro para analisar cada ano separadamente ou um período desejado, e os países que tiveram o maior consumo de energia. [Vizualizar Dashboard](https://lookerstudio.google.com/reporting/c6fa6cfa-358f-4040-87d0-704429487f98)

## Conclusões
A análise de dados desempenha um papel fundamental na transição para um modelo energético mais sustentável e eficiente. Ao permitir uma gestão mais precisa e inteligente do consumo de energia, essa abordagem contribui para a redução das emissões de gases poluentes, para a otimização de custos e para a promoção da justiça energética. Investir em tecnologias de análise de dados no setor energético é, portanto, essencial para enfrentar os desafios do século XXI e garantir um futuro mais equilibrado para as próximas gerações.
