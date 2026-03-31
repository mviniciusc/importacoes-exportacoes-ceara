# ANÁLISE DE MOVIMENTAÇÃO DE COMÉRCIO INTERNACIONAL DO CEARÁ

## Introdução

Bem-vindo(a). Esse projeto busca realizar análise da movimentação de carga nos portos do estado do Ceará visando comércio exterior. A intenção dessa análise é estabelecer um panorama das movimentações de carga e, a partir dessa visualização, formular observações e conclusões que guiem tomadas de decisão. Para alcançar esses objetivos, foram traçadas as seguintes perguntas:

* Existe algum país (ou grupo de países) que domina as exportações do estado?
* Quais as principais diferenças entre produtos embarcados nos diferentes portos?
* Qual o impacto da sazonalidade na exportação de frutas e produtos derivados?
* Existem novos parceiros que vêm crescendo nas exportações cearenses?


## Sobre os dados

A fonte base dos dados reúne diversos dados públicos brasileiros.  Os dados são tratados e disponibilizados gratuitamente.

No próprio site da fonte, em cada base de dados pode-se encontrar os componentes de cada tabela. Ao selecionar quais componentes serão visualizados, o prórpio site já fornece query a (SQL, python ou R) para correta visualização das colunas selecionadas.

A base de dados escolhida contém registros a partir de janeiro de 1997. Porém, para evitar o enviesamento das análises com dados antigos, todas as análises foram feitas apenas com dados dos últimos 10 anos (ago/2015 a ago/2025).

Todos os valores financeiros analisados se referem apenas ao valor da mercadoria. Não estão inclusos outros valores como frete e seguro.

## Tecnologias utilizadas

Esse projeto foi construído usando principalmente SQL para consultas ao banco de dados e Python para tratamento e análise desses dados. As principais bibliotecas python utilizadas foram Pandas, Matplotlib e Seaborn, além da biblioteca basededados para conexão com a fonte. As consultas SQL foram feitas diretamente dentro do código, com seu retorno sendo armazenado em dataframes para posterior análise usando python.

Também foi utilizado Google Cloud via BigQuery para acessar os dados da Base dos Dados. Isso permitiu realizar as consultas SQL em grandes volumes de dados diretamente da nuvem, sem a necessidade de baixar arquivos pesados para um banco de dados local.

## Principais conclusões

## Como replicar

Para a replicação desse projeto, incialmente deve-se instalar as bibliotecas necessárias em ambiente virtual. Para isso, deve ser digitado no terminal o comando `pip install -r requirements.txt`. Dessa forma o arquivo com os requisitos será lido e todas as bibliotecas mencionadas serão instaladas automaticamente.

Além disso, é necessário um id de projeto do google cloud. Esse passo é necessário porque a base de dados utiliza consultas diretamente no Google BigQuery e o Google Cloud exige um id para gerenciar cotas de processamento. A fonte de dados oferece mensalmente 1Tb gratuito de cotas, o que é mais que suficiente para execução desse projeto. No arquivo `analise-comex-ceara.ipynb` está indicado o local onde se deve inserir esse id.
