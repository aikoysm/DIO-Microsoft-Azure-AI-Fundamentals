# Reconhecimento Facial e transformação de imagens em Dados no Azure ML
Neste repositório, estarei documentando o passo a passo da execução dos laboratórios "Detecção facial no Vision Studio", "Leitura de textos no Vision Studio" e "Análise de imagens no Vision Studio", fornecido pela Microsoft Learn, e a minha experiência de aprendizado do laborátorio. 

## Objetivo dos laborátorios
São três laboratórios curtos, que visam o entendimento do funcionamento dos serviços de análise de imagem com o Azure IA Vision, e praticar com exemplos disponibilizados pela Microsoft Learn.

*******
### Índice
- [Reconhecimento Facial e transformação de imagens em Dados no Azure ML](#reconhecimento-facial-e-transformação-de-imagens-em-dados-no-azure-ml)
  - [Objetivo dos laborátorios](#objetivo-dos-laborátorios)
    - [Índice](#índice)
  - [Criação do recurso](#criação-do-recurso)
  - [Detectando rostos em uma imagem](#detectando-rostos-em-uma-imagem)
  - [Lendo textos em um arquivo](#lendo-textos-em-um-arquivo)
  - [Analisando imagens](#analisando-imagens)
  - [Conclusão](#conclusão)

*******

## Criação do recurso
Começando pela a criação do recurso onde o laboratório será desenvolvido, dentro do [Portal Azure](https://portal.azure.com), na aba de "Serviços Cognitivos", configurei a instância para pertencer à região *East US*, com o nome de "labIA900".  
Com o recurso criado, pude partir para o [Azure AI Vision studio](https://portal.vision.cognitive.azure.com), para o desenvolvimento da tarefa.

## Detectando rostos em uma imagem
Dentro do estúdio, comecei definindo o recurso criado como *recurso padrão*, e parti para o serviço **Detect faces in an image**, que será o foco desse laboratório.  
De cara já pude ter um contato básico com o serviço com alguns exemplos disponibilizados na página do estúdio, e também pude entender o seu funcionamento pela [documentação](https://learn.microsoft.com/en-us/azure/ai-services/computer-vision/concept-face-detection) disponibilizada.  
Também pude praticar a detecção de rostos com imagens que eu mesmo inseri na plataforma, onde pude ver alguns detalhes interessantes de como é feito o reconhecimento com base nas características do rosto.  
![ ](https://imgur.com/suMGrIW.png)  

## Lendo textos em um arquivo
Partindo para o próximo laboratório, ainda no estúdio, acessei o serviço **Extract text from images**, que será o foco dessa atividade.  
Assim como a atividade anterior, esse serviço também disponibiliza alguns exemplos para teste, e a [documentação](https://learn.microsoft.com/en-us/azure/ai-services/computer-vision/concept-ocr) com algumas informações adicionais.  
Partindo para a prática, inseri algumas imagens para praticar e novamente pude ver  como é feito o reconhecimento do texto dentro da imagem.  
![ ](https://imgur.com/be0loQf.png)  
Testando mais algumas imagens, pude ver o quão preciso essa tecnologia é. Onde até em imagens com a escrita feita a mão o serviço foi capaz de reconhecer o texto.   
![](https://imgur.com/iQIt07Q.png)  

## Analisando imagens
Finalizando as atividades, no último laboratório, utilizei os serviços **Add captions to images** e **Add dense captions to images**.  
Ambos os serviços são de analisar imagens e construir descrições com base nas características da imagem. Porém enquanto o primeiro serviço fornece uma breve descrição, o segundo fornece descrições sobre diferentes características da imagem.    
![ ](https://imgur.com/39K2m08.png)   
Também utilizei o serviço **Extract common tags from images**, que, assim como o Add dense captions to images, ele analisa diversas características da imagem, e retorna quais as características encontradas.  
![ ](https://imgur.com/hGF41nN.png)  

## Conclusão
Por mais que os laboratórios foram curtos e mais fáceis de serem realizados, achei as atividades propostas super interessantes, pois pude ter contato com essas três possibilidades de análise de imagem por meio de uma IA.  
Além de que, em cada serviço que visitei, a página também conta com guias e informações sobre as formas de aplicar esses serviços no mundo real.
