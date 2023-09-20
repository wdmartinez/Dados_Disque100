# Exploração da Base de Dados do Disque Direitos Humanos (Disque 100) - Grupo 1

Análise de casos de violações aos direitos humanos caracterizadas como trabalho análogo ao de escravo após denúncias realizadas no Disque Direitos Humanos (Disque 100), no primeiro semestre de 2022 e 2023.

Trabalho final do Grupo 1 para a disciplina "Fundamentos e Ética do Jornalismo de Dados" do Master em Jornalismo de Dados, Automação e Data Storytelling do Insper.

<hr>

## **Bases de dados**

As bases de dados utilizadas estão disponíveis no [site](https://www.gov.br/mdh/pt-br/acesso-a-informacao/dados-abertos/disque100) do **Ministério dos Direitos Humanos e da Cidadania**. Esses documentos são relatórios com dados das denúncias recebidas por meio do Disque Direitos Humanos **(Disque 100)**. Para fins comparativos, pegamos as bases correspondentes ao primeiro semestre de [2022](https://www.gov.br/mdh/pt-br/acesso-a-informacao/dados-abertos/disque100/primeiro-semestre-de-2022) e [2023](https://www.gov.br/mdh/pt-br/acesso-a-informacao/dados-abertos/disque100/copy2_of_primeiro-semestre-de-2022) em formato _.csv_.

<hr>

## **Visualização dos dados**

Para melhor visualização dos dados, abrimos as duas bases no programa [Orange Data Mining](https://orangedatamining.com/) e seguimos os seguintes passos:

+ 1º - Usamos a função “`Select Rows`” para filtrar apenas as denúncias que se encaixavam em critérios relacionados à condições análogas à escravidão:

```
LIBERDADE>DIREITOS INDIVIDUAIS>CONDIÇÃO ANÁLOGA A DE ESCRAVO>RESTRIGIR A LOCOMOÇÃO DE TRABALHADOR EM RAZÃO DE DÍVIDA
LIBERDADE>DIREITOS INDIVIDUAIS>CONDIÇÃO ANÁLOGA A DE ESCRAVO>SUBMETER TRABALHADOR A JORNADA EXAUSTIVA
LIBERDADE>DIREITOS INDIVIDUAIS>CONDIÇÃO ANÁLOGA A DE ESCRAVO>SUBMETER TRABALHADOR A TRABALHOS FORÇADOS
LIBERDADE>DIREITOS INDIVIDUAIS>CONDIÇÃO ANÁLOGA A DE ESCRAVO>SUJEITAR TRABALHADOR A CONDIÇÕES DEGRADANTES
LIBERDADE>DIREITOS INDIVIDUAIS>CONDIÇÃO ANÁLOGA A DE ESCRAVO>TRANSPORTAR TRABALHADOR PARA FINS DE EXPLORAÇÃO  
```

+ 2º - Com as bases já filtradas, fizemos dois agrupamentos diferentes, uma vez que uma mesma denúncia pode conter mais de uma violação. 

+ 3º - Por meio da função “`Group By`”, filtramos por “`violações`” e selecionamos como resultado a contagem (“`count`") da váriavel “`hash`”, que contém o código da denúncia. Com a tabela gerada, pudemos ver quantas denúncias havia para cada violação, sendo a soma de todas as denúncias o número de violações que foram denunciadas nos primeiros semestres de 2022 e 2023. 

4º Com a base original, fizemos outro tipo de agrupamento, dessa vez usando os códigos de denúncias. A contagem única dos códigos resultou no número de denúncias que foram feitas com uma ou mais violações relacionadas à condição de trabalho análogo ao de escravo em cada um dos anos.

<hr>

## **Análise dos dados**

A análise dos dados revelou que no primeiro semestre de 2023, o Disque 100 recebeu **3.024** casos de violações aos direitos humanos caracterizadas como trabalho análogo ao de escravo. O número representa um aumento de **76,53%** em relação ao total de violações dessa natureza registradas no mesmo período de 2022, que somou **1.713** registros. 

No Disque 100, há **cinco tipos** de violações em que denúncias relacionadas ao trabalho escravo se enquadram. Durante a análise dos dados, foi encontrada uma semelhança entre os casos de violações mais registrados no primeiro semestre de 2022 e no mesmo período em 2023. Denúncias de **jornadas de trabalho exaustivas** foram os casos mais registrados nos dois períodos pelos canais do Disque Direitos Humanos.

Além disso, o número de denúncias também cresceu. Enquanto o primeiro semestre de 2022 registrou **1.096 ** denúncias de violações, no mesmo período de 2023 foram realizadas **1.603** denúncias, o que representa um aumento de **46,26%**. É importante destacar que uma denúncia registrada no Disque 100 pode conter uma ou mais violações relacionadas à condição de trabalho análogo ao de escravo.

<hr>

## **Integrantes do Grupo 1:**
Ana Carolina Andrade, Giovanna Serafim, Jeová Pereira, Maria Eduarda Nascimento e Wanise Martinez

Email para contato: wanise@gmail.com
