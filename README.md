##### NOTAS DE ESTUDO E DESENVOLVIMENTO DO MODELO ##
O modelo buscou prever o estoque dos produtos com dataset focado em produtos ofertados em produção,  consumo e previsao de estoque de produtos.
Foi criado um modelo de analise preditiva "PrevEstoque 2024-8-5 10:24:31 AM" no canvas  importando o arquivo "dataset-1000-com-preco-promocional-e-renovacao-estoque.csv" como nome de "ds1000precopromorenovaestoque_csv"
Foi configurado o campo "Quantidade estoque" como alvo de analise para predizer os valores de dados futuros e ajustada a amostra para 1000 linhas. O modelo foi ajustado para horizonte de tempo de 9 dias, considerando feriados no Brasil.
Valore faltantes de preço foram substituídos com o valor médio, enquanto valores omissos em quantidade de estoque foram preenchidos com valor ZERO.
Considerando este um modelo de apren e estudo, o build selecioando foi o "quick build".

Os seguintes indicadores foram obtidos no Preview e No quick build após a análise do modelo
[preview]
stimated Avg. wQL 0.188 (0.188 is a non-negative metric whose lower value indicates a more accurate model.)
Estimated WAPE 0.277
Estimated MAPE 1.075
Estimated MASE 1.092
Estimated RMSE 25.083

[Quick Build]
Avg. wQL 0.259
MAPE 1.803
WAPE 0.378
RMSE 29.146
MASE 1.393

O modelo quick build, como esperado, mostrou-se menos cartivo na maior parte dos indicadores, todavia os resultados encontrados em 'Avg. wQL' e  'WAPE' encontrado neste metodo foram mais adequados, representando menos erros nas preciões e menos erros nos valores previsoas em relacao aos valores reais , respectivamente.

Avg. wQL (Média da Perda Quantil Ponderada): Essa métrica mede o erro nas previsões, ponderado pela importância de cada item. 
Um valor menor indica maior precisão nas previsões. Em um cenário de estoque, isso ajuda a entender quais previsões estão mais próximas da realidade e onde podem estar os maiores riscos de erro, possibilitando ajustes mais precisos.
MAPE (Erro Percentual Médio Absoluto): Calcula a média da porcentagem de erro das previsões em relação aos valores reais. Um MAPE menor indica maior precisão nas previsões. Por exemplo, se o MAPE for 5%, significa que, em média, as previsões de demanda estão erradas em 5% em relação à demanda real, o que é um bom indicador da eficiência do modelo.
WAPE (Erro Percentual Absoluto Ponderado): Similar ao MAPE, mas leva em consideração a importância de cada item no estoque. Isso significa que itens de maior valor ou importância terão um impacto maior na métrica. Um WAPE menor é desejável, pois indica que o modelo está prevendo com mais precisão para os itens mais críticos, o que é essencial para uma gestão eficiente do estoque.
RMSE (Raiz do Erro Quadrático Médio): Mede a diferença média entre os valores previstos e os valores reais, dando mais peso a grandes erros. Um RMSE menor é melhor, pois indica que as previsões estão, em média, próximas dos valores reais. No contexto de estoque, isso ajuda a minimizar grandes discrepâncias que podem levar a super ou subestimativas críticas.
MASE (Erro Escalado Médio Absoluto): Compara o erro da previsão com um modelo simples. Um valor de MASE menor que 1 indica que o modelo está fazendo previsões mais precisas do que simplesmente usar a média histórica. Para controle de estoque, um MASE menor que 1 é um bom sinal de que o modelo está efetivamente melhorando a previsão em comparação com métodos mais básicos.





Recursos Adicionais

# 📊 Previsão de Estoque Inteligente na AWS com [SageMaker Canvas](https://aws.amazon.com/pt/sagemaker/canvas/)

Bem-vindo ao desafio de projeto "Previsão de Estoque Inteligente na AWS com SageMaker Canvas. Neste Lab DIO, você aprenderá a usar o SageMaker Canvas para criar previsões de estoque baseadas em Machine Learning (ML). Siga os passos abaixo para completar o desafio!

## 📋 Pré-requisitos

Antes de começar, certifique-se de ter uma conta na AWS. Se precisar de ajuda para criar sua conta, confira nosso repositório [AWS Cloud Quickstart](https://github.com/digitalinnovationone/aws-cloud-quickstart).


## 🎯 Objetivos Deste Desafio de Projeto (Lab)

![image](https://github.com/digitalinnovationone/lab-aws-sagemaker-canvas-estoque/assets/730492/72f5c21f-5562-491e-aa42-2885a3184650)

- Dê um fork neste projeto e reescreva este `README.md`. Sinta-se à vontade para detalhar todo o processo de criação do seu Modelo de ML para uma "Previsão de Estoque Inteligente".
- Para isso, siga o [passo a passo] descrito a seguir e evolua as suas habilidades em ML no-code com o Amazon SageMaker Canvas.
- Ao concluir, envie a URL do seu repositório com a solução na plataforma da DIO.


## 🚀 Passo a Passo

### 1. Selecionar Dataset

-   Navegue até a pasta `datasets` deste repositório. Esta pasta contém os datasets que você poderá escolher para treinar e testar seu modelo de ML. Sinta-se à vontade para gerar/enriquecer seus próprios datasets, quanto mais você se engajar, mais relevante esse projeto será em seu portfólio.
-   Escolha o dataset que você usará para treinar seu modelo de previsão de estoque.
-   Faça o upload do dataset no SageMaker Canvas.

### 2. Construir/Treinar

-   No SageMaker Canvas, importe o dataset que você selecionou.
-   Configure as variáveis de entrada e saída de acordo com os dados.
-   Inicie o treinamento do modelo. Isso pode levar algum tempo, dependendo do tamanho do dataset.

### 3. Analisar

-   Após o treinamento, examine as métricas de performance do modelo.
-   Verifique as principais características que influenciam as previsões.
-   Faça ajustes no modelo se necessário e re-treine até obter um desempenho satisfatório.

### 4. Prever

-   Use o modelo treinado para fazer previsões de estoque.
-   Exporte os resultados e analise as previsões geradas.
-   Documente suas conclusões e qualquer insight obtido a partir das previsões.

## 🤔 Dúvidas?

Esperamos que esta experiência tenha sido enriquecedora e que você tenha aprendido mais sobre Machine Learning aplicado a problemas reais. Se tiver alguma dúvida, não hesite em abrir uma issue neste repositório ou entrar em contato com a equipe da DIO.
