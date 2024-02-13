# Utilizando AI Search para indexação e consulta de Dados
Neste repositório, estarei documentando o passo a passo da execução do laboratório "Explorando um índice do Azure IA Search (UI)", fornecido pela Microsoft Learn, e a minha experiência de aprendizado do laboratório. 

## Objetivo dos laborátorios
Construir uma solução de mineração de conhecimento que facilite a busca de insights sobre experiências de clientes.

*******
### Índice
  - [Criação dos recursos de IA](#criação-dos-recursos-de-ia)
  - [Criação da conta de armazenamento](#criação-da-conta-de-armazenamento)
  - [Importando os dados](#importando-os-dados)
  - [Adicionando um indexador de destino](#adicionando-um-indexador-de-destino)
  - [Adicionando índice para pesquisa](#adicionando-índice-para-pesquisa)
  - [Conclusão](#conclusão)

*******

## Criação dos recursos de IA
Começando pela a criação do recurso onde o laboratório será desenvolvido, dentro do [Portal Azure](https://portal.azure.com) selecionei o serviço **"IA Search"** configurei a instância para pertencer à região *East US*, com o nome de "lab900search".  
Para esse laboratório, também precisei criar outro recurso, dessa vez no serviço de **"Serviços Cognitivos"**, com o nome de "lab900searchIA".  

## Criação da conta de armazenamento
Após criar os recursos de IA, também precisei criar uma **"conta de armazenamento"**, onde os documentos utilizados para análise serão armazenados.  
Após criação desse recurso com o nome de "lab900storage", dentro dessa conta de armazenamento, também criei um contêiner com o nome de "coffeereviews", e depositei 9 documentos de exemplo disponibilizados pela Microsoft Learn.

## Importando os dados
Com todos os recursos criados, ainda no [Portal Azure](https://portal.azure.com), fui até a página do recurso de **IA Search**, onde o configurei para importar os dados do contêiner, extraindo o conteúdo e metadados relevante das informações do cliente.  
Após isso, também anexei o **Serviço Cognitivo** criado anteriormente e configurei os enrequecimentos da IA, onde ela irá:
- Extrair nome de localizações;
- Extrair frases-chave;
- Detectar sentimentos;
- Gerar marcações de imagens;
- Gerar legendas de imagens.  

E por fim, configurei para que os enrequecimentos sejam salvos em um contêiner novo, com o nome de "knowledge-store".

## Adicionando um indexador de destino
Ainda na configuração de importação de dados, comecei a criar um índice com o nome de "coffee-index" e criei um indexador de destino com o nome de "coffee-indexe" que, por meio dos filtros que adicionei, será responsável por:
- Extrair os metadados e o conteúdo dos documentos de origem;
- Executar o skillset do serviço congnitivo para gerar mais enrequecimentos;
- Mapear os dados extraídos para o índice.  

![ ](https://imgur.com/2srJe9m.png)  

## Adicionando índice para pesquisa
Agora com tudo configurado, comecei a testar o índice para pesquisa com os prompts de exemplo do laboratório, onde pude entender mais sobre como é possível utilizar essa aplicação para identificar palavras-chave dentro dos arquivos. Além de também experimentar com outros prompts de localizações, frases-chave e sentimentos.
![ ](https://imgur.com/5EgQ1SP.png)

## Conclusão
Achei esse laboratório mega interessante, principalmente pela forma como pude usar diferentes recursos para exercer uma única função juntos.  
Também fiquei pensando nas possibilidades de ter essa ferramenta de índice de pesquisa para um repositório onde está sempre sendo adicionado arquivos novos.

### Referências
* ###### https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/11-ai-search.html
