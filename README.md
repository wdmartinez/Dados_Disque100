# Exploração da Base de Dados do Disque Direitos Humanos (Disque 100) - Grupo 1

Análise de casos de violações aos direitos humanos caracterizadas como trabalho análogo ao de escravo após denúncias realizadas no citado órgão no primeiro semestre de 2022 e 2023.

Trabalho final do Grupo 1 para a disciplina "Fundamentos e Ética do Jornalismo de Dados" do Master em Jornalismo de Dados, Automação e Data Storytelling do Insper.

As bases de dados que usamos estão disponíveis no site [inserir link na palavra “site”: https://www.gov.br/mdh/pt-br/acesso-a-informacao/dados-abertos/disque100 ] do Ministério dos Direitos Humanos e da Cidadania e são relatórios com dados das denúncias recebidas através do Disque Direitos Humanos (Disque 100). Para fins comparativos, pegamos as bases correspondentes ao primeiro semestre de 2022 [inserir link em “2022”: https://www.gov.br/mdh/pt-br/acesso-a-informacao/dados-abertos/disque100/primeiro-semestre-de-2022 ] e 2023 [inserir link em “2022”: https://www.gov.br/mdh/pt-br/acesso-a-informacao/dados-abertos/disque100/copy2_of_primeiro-semestre-de-2022 ] (formato .csv).

Para melhor visualização dos dados, abrimos ambas as bases no programa Orange Data Mining [inserir link em “Orange Data Mining”: https://orangedatamining.com/ ]. Começamos filtrando (através da função “Select Rows”) apenas as denúncias que se encaixavam em critérios relacionados à condições análoga à escravidão:

LIBERDADE>DIREITOS INDIVIDUAIS>CONDIÇÃO ANÁLOGA À DE ESCRAVO>RESTRIGIR A LOCOMOÇÃO DE TRABALHADOR EM RAZÃO DE DÍVIDA
LIBERDADE>DIREITOS INDIVIDUAIS>CONDIÇÃO ANÁLOGA À DE ESCRAVO>SUBMETER TRABALHADOR A JORNADA EXAUSTIVA
LIBERDADE>DIREITOS INDIVIDUAIS>CONDIÇÃO ANÁLOGA À DE ESCRAVO>SUBMETER TRABALHADOR A TRABALHOS FORÇADOS
LIBERDADE>DIREITOS INDIVIDUAIS>CONDIÇÃO ANÁLOGA À DE ESCRAVO>SUJEITAR TRABALHADOR A CONDIÇÕES DEGRADANTES
LIBERDADE>DIREITOS INDIVIDUAIS>CONDIÇÃO ANÁLOGA À DE ESCRAVO>TRANSPORTAR TRABALHADOR PARA FINS DE EXPLORAÇÃO  

Com as bases já filtradas, fizemos dois agrupamentos diferentes, uma vez que uma mesma denúncia pode conter mais de uma violação. 

Primeiro agrupamos (através da função “Group By”) por “violações” e selecionamos como resultado a contagem (“count”) da váriavel “Hash”, que contém o código da denúncia). Através da tabela obtida, pudemos ver quantas denúncias tiveram para cada violação, sendo a soma de todas as denúncias, o número de violações que foram denunciadas em cada um dos anos. 

Com a base original, fizemos outro tipo de agrupamento, dessa vez agrupando pelos códigos de denúncias. A contagem única dos códigos resulta no número de denúncias que foram feitas com uma ou mais violação relacionada à condição análoga à de escravo em cada um dos anos.
