# Trabalhando com Machine Learning na Prática no Azure ML
Neste repositório, estarei documentando o passo a passo da execução do laboratório "Explorando Machine Learning automatizado dentro do Azure ML", fornecido pela Microsoft Learn, e a minha experiência de aprendizado com o laboratório.

## Objetivo do laborátorio
Usar dados de histórico de um serviço de aluguel de bikes para treinar um modelo que prevê o número de bicicletas alugadas esperadas em dias especificos, baseado em características sazonais e meteorológicas.

*******
### Índice  
  - [Criação do Workspace](#criação-do-workspace)
  - [Criando o modelo](#criando-o-modelo)
  - [Configurando a tarefa](#configurando-a-tarefa)
  - [Avaliação dos resultados](#avaliação-dos-resultados)
  - [Conclusão](#conclusão)

*******

## Criação do Workspace
Começando pela a criação do espaço de trabalho, pelo [Portal Azure](https://portal.azure.com), onde os recursos de Machine Learning serão aplicados. O espaço de trabalho teve o nome de "labIA900" e foi criado na região *East US*.  
Com o ambiente de trabalho criado, pude partir para o [Azure Machine Learning studio](https://ml.azure.com), para o desenvolvimento da tarefa. Mas antes disso, aproveitei para explorar o ambiente do Portal Azure, onde aprendi mais sobre os serviços ofertados e encontrei [guias](##Referências), que viriam a ser úteis para o desenvolvimento do laboratório.

## Criando o modelo
É dentro dos espaços de trabalho que definimos o que a IA fará. No caso da atividade proposta, precisamos que a IA estude um banco de dados e preveja um valor com base nas características definidas.
Para isso, foi criado uma tarefa com o nome de "mslearn-bike-automl" e, dentro dessa tarefa, foi definido informações como:  
* **Tipo de tarefa:** Regressão;
* **Tipo do ativo de dados:** Tabular;
* **Fonte de dados:** Arquivo da Web.

## Configurando a tarefa
Com as configurações básicas da tarefa criada, agora podemos configurar quais dados serão estudados e o que exatamente será retornado para o usuário.  
Primeiro foi necessário especificar o [banco de dados](https://aka.ms/bike-rentals) e quais seus delimitadores para examinação dos dados.  
Após isso, foi definido a coluna de destino e suas configurações, como qual métrica seria utilizada e quais modelos seriam estudados.  
Também foram definidas configurações como:  
* **Limite máximo de avaliações:** 3;
* **Limite de pontuação da métrica:** 0.085;
* **Limite de tempo do experimento:** 15 min;
* **Tipo de validação:** Divisão de validação do treinamento.  
  
Por fim, foi definido o poder computacional utilizado, e a máquina estava pronta para aprender.


## Avaliação dos resultados
![Resultado](https://imgur.com/sNOA61h.png) 
A tarefa teve duração de 27 minutos e 59 segundos, e com os resultados pude observar algumas informações interessantes, como o melhor modelo de algoritmo para a tarefa e a taxa de erro da métrica primária.  
Por fim, realizei o teste de ponto de extremidade, onde obtive os seguintes resultados:  
![Ponto de extremidade](https://imgur.com/NGu7BHl.png)



## Conclusão
Esse laboratório foi meu primeiro contato com os serviços do Azure, e serviu não só para que eu pudesse praticar Machine Learning, como também para me integrar aos serviços Azure e, principalmente, entender os fundamentos de inteligência artificial.  
Esse laboratório também me motivou a buscar mais informações sobre o assunto, visto que, apesar de eu ter seguido o passo a passo à risca, o tempo de computação da tarefa foi quase o dobro do tempo proposto, me mostrando que havia potencial de otimização da configuração da tarefa.

### Referências
* ###### https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/01-machine-learning.html
* ###### https://learn.microsoft.com/en-us/azure/machine-learning/?view=azureml-api-2
