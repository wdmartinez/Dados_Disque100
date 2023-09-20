# Exploração da Base de Dados do Disque Direitos Humanos (Disque 100) - Grupo 1

Análise de casos de violações aos direitos humanos caracterizadas como trabalho análogo ao de escravo após denúncias realizadas no citado órgão no primeiro semestre de 2022 e 2023.

Trabalho final do Grupo 1 para a disciplina "Fundamentos e Ética do Jornalismo de Dados" do Master em Jornalismo de Dados, Automação e Data Storytelling do Insper.

**Bases de dados**
As bases de dados utilizadas estão disponíveis no [site](https://www.gov.br/mdh/pt-br/acesso-a-informacao/dados-abertos/disque100) do Ministério dos Direitos Humanos e da Cidadania e são relatórios com dados das denúncias recebidas por meio do Disque Direitos Humanos (Disque 100). 
Para fins comparativos, pegamos as bases correspondentes ao primeiro semestre de [2022](https://www.gov.br/mdh/pt-br/acesso-a-informacao/dados-abertos/disque100/primeiro-semestre-de-2022) e [2023](https://www.gov.br/mdh/pt-br/acesso-a-informacao/dados-abertos/disque100/copy2_of_primeiro-semestre-de-2022) em formato.csv.

**Visualização e análise dos dados**
Para melhor visualização dos dados, abrimos ambas as bases no programa [Orange Data Mining](https://orangedatamining.com/) e seguimos os seguintes passos:

1º Usamos a função “Select Rows” para filtrar apenas as denúncias que se encaixavam em critérios relacionados à condições análoga à escravidão:

LIBERDADE>DIREITOS INDIVIDUAIS>CONDIÇÃO ANÁLOGA A DE ESCRAVO>RESTRIGIR A LOCOMOÇÃO DE TRABALHADOR EM RAZÃO DE DÍVIDA
LIBERDADE>DIREITOS INDIVIDUAIS>CONDIÇÃO ANÁLOGA A DE ESCRAVO>SUBMETER TRABALHADOR A JORNADA EXAUSTIVA
LIBERDADE>DIREITOS INDIVIDUAIS>CONDIÇÃO ANÁLOGA A DE ESCRAVO>SUBMETER TRABALHADOR A TRABALHOS FORÇADOS
LIBERDADE>DIREITOS INDIVIDUAIS>CONDIÇÃO ANÁLOGA A DE ESCRAVO>SUJEITAR TRABALHADOR A CONDIÇÕES DEGRADANTES
LIBERDADE>DIREITOS INDIVIDUAIS>CONDIÇÃO ANÁLOGA A DE ESCRAVO>TRANSPORTAR TRABALHADOR PARA FINS DE EXPLORAÇÃO  

2º Com as bases já filtradas, fizemos dois agrupamentos diferentes, uma vez que uma mesma denúncia pode conter mais de uma violação. 

3º Por meio da função “Group By”, filtramos por “violações” e selecionamos como resultado a contagem (“count”) da váriavel “Hash”, que contém o código da denúncia. Com a tabela que foi obtida, pudemos ver quantas denúncias havia para cada violação, sendo a soma de todas as denúncias o número de violações que foram denunciadas nos primeiros semestres de 2022 e 2023. 

4º Com a base original, fizemos outro tipo de agrupamento, dessa vez usando os códigos de denúncias. A contagem única dos códigos resultou no número de denúncias que foram feitas com uma ou mais violações relacionadas à condição análoga a escravo em cada um dos anos.
