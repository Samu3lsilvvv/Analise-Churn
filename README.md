# <font color='blue'>Análise Estatística de Churn em Telecomunicações</font>

### Visão Geral do Projeto
Este projeto consiste em uma análise estatística utilizando Regressão Logística para identificar e quantificar os principais fatores que influenciam o cancelamento de serviços (churn) em uma empresa fictícia de telecomunicações. O objetivo principal é extrair insights estatisticamente significativos dos dados, transformando coeficientes em recomendações estratégicas acionáveis para otimizar a retenção de clientes e reduzir custos associados ao churn.

O desenvolvimento foi realizado em Python utilizando o ambiente Jupyter Notebook, que permite uma abordagem interativa e visual para a modelagem estatística e análise de resultados.

A análise foi estruturada para responder às seguintes perguntas-chave:

1.  **Fatores Determinantes:** Quais variáveis têm impacto estatisticamente significativo na probabilidade de churn?
2.  **Tendências de Faturamento:** Qual é a força e direção do efeito de cada fator (medido através de Odds Ratio)?
3.  **Segmentação de Risco:** Como podemos identificar clientes com alto risco de cancelamento?
4.  **Otimização de Portfólio:**Quais intervenções específicas a empresa pode implementar para reduzir o churn?


### Tecnologias e Bibliotecas

O projeto foi desenvolvido em **Python** no ambiente **Jupyter Notebook**. As bibliotecas que foram utilizadas são:

* **Pandas e Numpy:** Utilizado para realizar a manipulação, limpeza e o pré-processamento dos dados.
* **Statsmodels:**  Para implementação e análise da Regressão Logística.
* **Matplotlib e Seaborn:** Para a criação e personalização de visualizações de dados estáticos.
* **Plotly:** Para criação de visualizações interativas e dinâmicas.
* **Scikit-learn:** Para métricas de avaliação do modelo.



### Metodologia e Estrutura do Notebook
O notebook analise_churn.ipynb está dividido em etapas que mostram o fluxo de trabalho padrão do projeto.

**Preparação dos Dados**

• Geração de Dados Fictícios: Uma função (gerador_dados_churn) é usada para criar um DataFrame simulado que representa 2.000 clientes de telecomunicações, garantindo que o projeto seja totalmente auto-suficiente e replicável. A lógica de geração incorpora relações realistas entre variáveis.

• Inspeção e Limpeza Inicial: Verificação de tipos de dados (dtypes), statísticas descritivas e estrutura das variáveis categóricas e numéricas.

**Análise Exploratória de Dados**

### Principais Questões de Negócio e Insights

##### A. Performance de Produtos (O que é mais vendido?)

**Questão:** Quais são os Top 10 produtos mais vendidos?

**Análise Realizada:** Agregação por Nome_Produto e soma de Quantidade

##### B. Otimização de Portfólio (Onde está o dinheiro?)

**Questão:** Qual categoria gera mais receita?

**Análise Realizada:** Agregação por Categoria e soma de Valor_Total_Venda.

##### C. Tendências e Sazonalidade (Quando devemos investir?)

**Questão:** Como o faturamento evoluiu ao longo do tempo?

**Análise Realizada:** Agregação mensal do Valor_Total_Venda e visualização em gráfico de linha.

##### D. Foco Regional (Para onde expandir?)

**Questão:** Qual estado tem o maior faturamento?

**Análise Realizada:** Agregação por Estado e soma de Valor_Total_Venda (Top 5).

### Como Executar o Projeto
Pré-requisitos: Certifique-se de ter o Python (preferencialmente com o ambiente Anaconda/Miniconda) e o VS Code (com a extensão Jupyter) instalados.

#### 1. Pré-requisitos: 

Necessária o Python (preferencialmente com o ambiente Anaconda) e o VS Code (com a extensão Jupyter) instalados.

#### 2. Clone o Repositório:

```bash
git clone <https://github.com/Samu3lsilvvv/Analise-Vendas-Ecommerce>
cd Analise-Vendas-Ecommerce-Python
```

#### 3. Instalar as Dependências:

Instale as bibliotecas necessárias para rodar o Notebook (Pandas, NumPy, Matplotlib, etc.).

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

#### 4.Iniciar o Notebook:

Execute o Notebook usando o comando jupyter notebook e abra o arquivo codigo.ipynb no seu navegador. Alternativamente, abra o arquivo diretamente pelo VS Code.

```bash
jupyter notebook
```
