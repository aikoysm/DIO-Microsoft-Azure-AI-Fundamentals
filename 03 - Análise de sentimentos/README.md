# Análise de Sentimentos com Language Studio no Azure AI
Neste repositório, estarei documentando o passo a passo da execução dos laboratórios "Conhecimento o Azure Speech Studio" e "Analisando textos com o Azure Language Studio", fornecidos pela Microsoft Learn, e a minha experiência de aprendizado dos laboratórios. 


## Objetivo dos laborátorios
São dois laboratórios curtos, que visam o entendimento do funcionamento dos serviços de análise de fala com o Azure IA Speech e Language Studios, e praticar com exemplos disponibilizados pela Microsoft Learn.

*******
### Índice
  - [Criação do recurso](#criação-do-recurso)
  - [Conversão de fala em texto](#conversão-de-fala-em-texto)
  - [Analisando sentimentos em um texto](#analisando-sentimentos-em-um-texto)
  - [Conclusão](#conclusão)

*******

## Criação do recurso
Começando pela a criação do recurso onde o laboratório de **Conversão de fala em texto** será desenvolvido, dentro do [Portal Azure](https://portal.azure.com), na aba de "Serviços Cognitivos", configurei a instância para pertencer à região *East US*, com o nome de "labIA900".  
Para o laboratório **Analisando sentimentos em um texto**, criei outro recurso, dessa vez na aba de "Análise de Texto", e também o configurei para pertencer à região *East US*, com o nome de "lablanguage".
Com o recurso criado, pude partir para o [Azure AI Speech Studio](https://speech.microsoft.com/portal), para o desenvolvimento do primeiro laboratório.

## Conversão de fala em texto
Dentro do estúdio, selecionei o recurso criado e parti para o serviço **Conversão de fala em texto em tempo real**, que será o foco desse laboratório.  
Utilizando um arquivo de áudio disponibilizado pela **Microsoft Learn**, pude experimentar o serviço, onde, enquanto o arquivo de áudio tocava, a plataforma já extraia o texto automaticamente, resultando em uma conversão extremamente precisa.  
Também vi que serviço possui suporte para diversos idiomas, incluindo português, então resolvi testar o quão preciso ele realmente é inserindo músicas brasileiras. E, por mais que houve alguns erros, fiquei surpreso com o quanto o serviço foi capaz de transcrever a letra.  
![ ](https://imgur.com/0FzLWho.png)  
Após brincar mais um pouco com as possibilidades do serviço, também vi sobre as diferentes formas de aplicá-lo, incluindo o [repositório no GitHub](https://github.com/Azure-Samples/cognitive-services-speech-sdk) do serviço, disponibilizado pela Microsoft.  
 
## Analisando sentimentos em um texto
Partindo para o próximo laboratório, dessa vez no [Azure IA Language Studio](https://language.cognitive.azure.com/home). Após selecionar o recurso criado anteriormente, parti para o serviço de **análise de sentimentos e opiniões em um texto**.  
Assim como no laboratório anterior, comecei a testar o serviço utilizando um texto de exemplo fornecido pela Microsoft Learn. Com isso, pude ver como é feito a análise do texto e como a IA categoriza cada fala, trazendo um resultado em porcentagem que alterna entre "Positivo", "Neutro" e "Negativo", onde no caso, o texto teve o resultado de 96% negativo e 3% neutro.  
Para testar um pouco mais o serviço, decidi utilizar um trecho da letra da mesma música que eu havia usado para o laboratório anterior que, na minha interpretação, é relativamente negativa. E, para a minha surpresa, a IA apontou como sendo 100% negativo, mas após olhar melhor, vi que não era pelos motivos que eu esperava, já que esse resultado foi com base em somente uma frase do trecho, e não dos diferentes versos da música.
![ ](https://imgur.com/4G8o5BJ.png)

## Conclusão
Por mais que os laboratórios foram curtos e mais fáceis de serem realizados, gostei bastante de ter contato com essas serviços e suas possibilidades.  
Além de que, também pude ver guias e informações sobre as formas de aplicar esses serviços no mundo real.

### Referências
* ###### https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/09-speech.html 
* ###### https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/06-text-analysis.html
