# ANÁLISE DE MOVIMENTAÇÃO DE COMÉRCIO INTERNACIONAL DO CEARÁ

Desenvolvido por Marcus Vinicius Cavalcante

## Introdução

Bem-vindo(a). Esse projeto busca realizar análise da movimentação de carga nos portos do estado do Ceará visando exportações. A intenção dessa análise é estabelecer um panorama das movimentações de carga e, a partir dessa visualização, formular observações e conclusões que guiem tomadas de decisão. Para alcançar esses objetivos, foram traçadas as seguintes perguntas:

* Existe algum país (ou grupo de países) que domina as exportações do estado?
* Quais as principais diferenças entre produtos embarcados nos diferentes portos?
* Existem novos parceiros que vêm crescendo nas exportações cearenses?

## Importante

Esse projeto foi criado com intuito exclusivo de constituição de portifólio de análise de dados, sendo idealizado e construído de forma individual e independente. Portanto, essas análises não estão vinculadas a nenhum governo ou organização. Também não é intenção do autor promover qualquer tipo de viés político.

## Sobre os dados

A fonte base dos dados reúne diversos dados públicos brasileiros.  Os dados são tratados e disponibilizados gratuitamente.

No próprio site da fonte, em cada base de dados pode-se encontrar os componentes de cada tabela. Ao selecionar quais componentes serão visualizados, o próprio site já fornece a query (SQL, python ou R) para correta visualização e tradução das colunas selecionadas.

A base de dados escolhida contém registros a partir de janeiro de 1997. Porém, para evitar o enviesamento das análises com dados antigos, todas as análises foram feitas apenas com dados dos últimos 10 anos (até ago/2025), a menos que outro período seja explicitado.

Todos os valores financeiros analisados estão em dólares americanos (USD) e se referem apenas ao valor da mercadoria. Não estão inclusos outros valores como frete ou seguro.

## Tecnologias utilizadas

Esse projeto foi construído usando principalmente SQL para consultas ao banco de dados e Python para tratamento e análise desses dados. A principal biblioteca python utilizada foi Matplotlib, além da biblioteca "basededados" para conexão com a fonte. As consultas SQL foram feitas diretamente dentro do código, com seu retorno sendo armazenado em dataframes para posterior análise usando python.

Também foi utilizado Google Cloud via BigQuery para acessar os dados da Base dos Dados. Isso permitiu realizar as consultas SQL em grandes volumes de dados diretamente da nuvem, sem a necessidade de baixar arquivos pesados para um banco de dados local.

## Principais conclusões

Foi possível identificar que o estado do Ceará possui grande dependência comercial das exportações para os Estados Unidos, notoriamente envolvendo produtos siderurgicos. Tal dependência pode representar uma vulnerabilidade, pois qualquer alteração nessa parceria pode ter grande impacto na economia estadual.

Outro foco de análise permitiu identificar que os dois portos do estado (Pecém e Fortaleza) trabalham predominantemente com tipos de carga semelhantes. Com forte dominância de derivados de aço, essa distribuição é importante para evitar sobrecargas e subutilizações, mantendo o correto fluxo logístico.

Por fim, existem importantes parceiros comerciais que vêm crescendo em valor de negócios com o Ceará. Essas movimentações crescentes são importantes para que o estado fortaleça sua economia tanto em valor quanto em estabilidade. Portanto é interessante que se mantenham políticas voltadas a manter essas relações crescendo e promover ainda mais essa diversificação.

## Como replicar

Para a replicação desse projeto, incialmente deve-se instalar as bibliotecas necessárias em ambiente virtual. Para isso, use no terminal o comando `pip install -r requirements.txt`. Dessa forma o arquivo com os requisitos será lido e todas as bibliotecas mencionadas serão instaladas automaticamente.

Além disso, é necessário um id de projeto do google cloud. Esse passo é necessário porque a base de dados utiliza consultas diretamente no Google BigQuery e o Google Cloud exige um id para gerenciar cotas de processamento. A fonte de dados oferece mensalmente 1Tb gratuito de cotas, o que é mais que suficiente para execução desse projeto. No arquivo `analise-comex-ceara.ipynb` está indicado o local onde se deve inserir esse id.
