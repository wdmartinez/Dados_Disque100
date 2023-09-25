# Exploração da Base de Dados do Disque Direitos Humanos (Disque 100) - Grupo 1

Análise de casos de violações aos direitos humanos caracterizadas como trabalho análogo ao de escravo após denúncias realizadas no Disque Direitos Humanos (Disque 100), no primeiro semestre de 2022 e 2023.

Trabalho final do Grupo 1 para a disciplina "Fundamentos e Ética do Jornalismo de Dados" do Master em Jornalismo de Dados, Automação e Data Storytelling do Insper.

<hr>

## **Bases de dados**

As bases de dados utilizadas estão disponíveis no [site](https://www.gov.br/mdh/pt-br/acesso-a-informacao/dados-abertos/disque100) do **Ministério dos Direitos Humanos e da Cidadania**. Esses documentos são relatórios com dados das denúncias recebidas por meio do Disque Direitos Humanos **(Disque 100)**. Para fins comparativos, pegamos as bases correspondentes ao primeiro semestre de [2022](https://www.gov.br/mdh/pt-br/acesso-a-informacao/dados-abertos/disque100/primeiro-semestre-de-2022) e [2023](https://www.gov.br/mdh/pt-br/acesso-a-informacao/dados-abertos/disque100/copy2_of_primeiro-semestre-de-2022) em formato _.csv_.

<hr>

## **Por que escolhemos essa base?**

Escolhemos essa base pela ampla possibilidade de exploração de dados. Apesar de ser bastante densa, o que nos deu trabalho para filtrar os dados e chegar em pontos de importância para o que queríamos buscar como pauta, essa base tem um potencial enorme como provedora de informação de qualidade. Ainda assim, levamos em consideração que, como essa é uma base com dados novos, sua utilização pede mais cuidado na hora da checagem e tratamento dos dados para, assim, garantir que as informações utilizadas na futura matéria estejam corretas e ofereçam confiabilidade aos leitores.

Vale destacar que o Disque 100 analisa e encaminha denúncias de violações de direitos humanos relacionadas aos seguintes grupos e/ou temas: crianças e adolescentes; pessoas idosas; pessoas com deficiência; pessoas em restrição de liberdade; população LGBTQIA+; população em situação de rua; discriminação ética ou racial; tráfico de pessoas; trabalho análogo à escravidão; terra e conflitos agrários; moradia e conflitos urbanos; violência contra ciganos, quilombolas, indígenas e outras comunidades tradicionais; violência policial (inclusive das forças de segurança pública no âmbito da intervenção federal no estado do Rio de Janeiro); violência contra comunicadores e jornalistas; violência contra migrantes e refugiados e pessoas com doenças raras.

## **O que perguntamos aos dados?** 

+ Quantos casos de violações aos direitos humanos caracterizados como trabalho análogo ao de escravo o Disque 100 registrou no primeiro semestre de 2022? E no mesmo período em 2023?
+ Quais foram os casos de violações mais registrados no primeiro semestre de 2022 e no mesmo período em 2023? 
+ Quantas denúncias de trabalho análogo ao de escravo o Disque Direitos Humanos recebeu no período analisado em 2022 e 2023?
+ Qual estado mais registrou casos de violação aos direitos humanos relacionado à condição de trabalho análogo ao de escravo?

## **O que mais pode ser explorado sobre o tema nessa base?**

Por conta de sua amplitude e densidade de dados, essa base permite realizar vários tipos de investigação socialmente relevantes, como a que escolhemos fazer. Com isso em mente, pensamos também em explorar o perfil dos violadores dentro da proposta de pré-pauta, já que a base fornece informações como raça e município do suspeito, além de relação de proximidade com a vítima. Outro ponto que pode ser explorado por meio dos dados desta base é mensurar a faixa etária das vítimas por violação, o que colabora para explorar também o perfil destas pessoas. Outra análise que poderia ser feita é sobre a nacionalidade das vítimas, uma vez que vemos cada vez mais imigrantes e refugiados sendo submetidos a esses tipos de condições precárias e análogas à escravidão. Acreditamos que, com mais tempo focado na filtragem dos dados, essa pauta também pode trazer outras informações de grande relevância.

## **Visualização e tratamento dos dados**

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

+ 4º - Com a base original, fizemos outro tipo de agrupamento, dessa vez usando os códigos de denúncias. A contagem única dos códigos resultou no número de denúncias que foram feitas com uma ou mais violações relacionadas à condição de trabalho análogo ao de escravo em cada um dos anos.

+ 5º - Usando a mesma lógica anterior, agrupamos por "UF" para analisar onde os casos aumentaram entre o primeiro de semestre de 2022 e 2023. Por meio da ferramenta [Flourish](https://flourish.studio/), plotamos os dados em um mapa coroplético para melhor visualização da evolução das denúncias. O mapa pode ser acessado por [aqui](https://public.flourish.studio/visualisation/15129320).

<hr>

## **Análise dos dados**

A análise dos dados revelou que no primeiro semestre de 2023, o Disque 100 recebeu **3.024** casos de violações aos direitos humanos caracterizadas como trabalho análogo ao de escravo. O número representa um aumento de **76,53%** em relação ao total de violações dessa natureza registradas no mesmo período de 2022, que somou **1.713** registros. 

No Disque 100, há cinco tipos de violações em que denúncias relacionadas ao trabalho escravo se enquadram. Durante a análise dos dados, foi encontrada uma semelhança entre os casos de violações mais registrados no primeiro semestre de 2022 e no mesmo período em 2023. Denúncias de jornadas de trabalho exaustivas foram os casos mais registrados nos dois períodos pelos canais do Disque Direitos Humanos. 

O estado que mais registrou violações relacionadas a casos de trabalho análogo ao de escravo foi São Paulo em ambos os períodos analisados. Em 2022, o estado mais populoso do país registrou **367** casos de violações e, neste ano, o número subiu para **701** registros no Disque 100. Em segundo lugar vem Minas Gerais com **268** casos em 2022 e **513** em 2023. 

Além disso, o número de denúncias também cresceu. Enquanto o primeiro semestre de 2022 registrou **1.096** denúncias de violações, no mesmo período de 2023 foram realizadas **1.603** denúncias, o que representa um aumento de **46,26%**. É importante destacar que uma denúncia registrada no Disque 100 pode conter uma ou mais violações relacionadas à condição de trabalho análogo ao de escravo. 

Em relação às denúncias, São Paulo e Minas Gerais foram os estados que mais registraram denúncias no primeiro semestre de 2022 e 2023. O resultado pode ser conferido no mapa coroplético como indicado acima.

Tendo em vista a riqueza e novidade dos dados, é possível explorar pautas que tratem não só sobre o aumento nos casos de violações e denúncias, mas que também utilize os dados para produzir reportagens mais aprofundadas com personagens, por exemplo. Um ponto interessante seria buscar saber o que ocorre após as denúncias serem registradas no Disque 100 e quantos casos se transformam em resgate de pessoas em condições análogas ao trabalho de escravo, por exemplo.

<hr>

## **Importante!** 

As perguntas realizadas à base não combinam denúncias e violações, pois durante o tratamento dos dados o grupo observou que uma denúncia pode conter uma ou mais violações. Desta forma, o número de denúncias não necessariamente revela quantas violações foram registradas.

## **Integrantes do Grupo 1**
Ana Carolina Andrade, Giovanna Serafim, Jeová Pereira, Maria Eduarda Nascimento e Wanise Martinez

Email para contato: wanise@gmail.com
