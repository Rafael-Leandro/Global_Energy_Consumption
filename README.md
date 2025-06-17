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
