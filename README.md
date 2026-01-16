# <font color='blue'>Análise Estatística de Churn em Telecomunicações</font>

### Visão Geral do Projeto
Análise estatística completa para identificar e quantificar os principais fatores que influenciam o cancelamento de serviços (churn) em uma empresa fictícia de telecomunicações. Utiliza **Regressão Logística** para modelar a probabilidade de churn e fornece insights acionáveis para estratégias de retenção. Este Projeto foi demonstrado no Curso de Fundamentos de Linguagem Python – Do Básico a Aplicações de IA, da escola Data Science Academy.

O desenvolvimento foi realizado em Python utilizando o ambiente Jupyter Notebook, que permite uma abordagem interativa e visual para a modelagem estatística e análise de resultados.

A análise foi estruturada para responder às seguintes perguntas-chave:

1.  **Fatores Determinantes:** Quais variáveis têm impacto estatisticamente significativo na probabilidade de churn?
2.  **Tendências de Faturamento:** Qual é a força e direção do efeito de cada fator (medido através de Odds Ratio)?
3.  **Segmentação de Risco:** Como podemos identificar clientes com alto risco de cancelamento?
4.  **Otimização de Portfólio:**Quais intervenções específicas a empresa pode implementar para reduzir o churn?


## Tecnologias Utilizadas

| Tecnologia | Versão | Uso |
|------------|---------|-----|
| Python | 3.9+ | Análise e modelagem |
| Pandas | 2.3.1 | Manipulação de dados |
| Statsmodels | 0.14.4 | Regressão Logística |
| Matplotlib/Seaborn | 3.10/0.13.2 | Visualizações estáticas |
| Plotly | 5.24.1 | Visualizações interativas |
| Jupyter | 1.0.0 | Ambiente de desenvolvimento |


### Metodologia e Estrutura do Notebook
O notebook analise_churn.ipynb está dividido em etapas que mostram o fluxo de trabalho padrão do projeto.

**Preparação dos Dados**

**• Geração de Dados Fictícios:** Uma função (gerador_dados_churn) é usada para criar um DataFrame simulado que representa 2.000 clientes de telecomunicações, garantindo que o projeto seja totalmente auto-suficiente e replicável. A lógica de geração incorpora relações realistas entre variáveis.

**• Inspeção e Limpeza Inicial:** Verificação de tipos de dados (dtypes), statísticas descritivas e estrutura das variáveis categóricas e numéricas.

**Análise Exploratória de Dados**

**• Análise Univariada:** Distribuição das variáveis independentes e da variável alvo (Churn).

**• Análise Bivariada:** Relação entre cada variável preditora e o status de churn, utilizando visualizações como boxplots e gráficos de barras.

**• Matriz de Correlação:** Identificação de relações lineares entre variáveis numéricas.

**Pré-processamento para Modelagem**

**• Codificação de Variáveis Categóricas:** Transformação das variáveis Tipo_Contrato e Servico_Internet em variáveis dummy (one-hot encoding) para inclusão no modelo estatístico.

**Modelagem Estatística - Regressão Logística**

Esta seção é o principal do projeto, onde será implementado e interpretado o modelo:

**• Formulação do Modelo: Definição da variável dependente (Churn) e independentes.**

**• Ajuste do Modelo: Treinamento da Regressão Logística utilizando a biblioteca Statsmodels.**

**• Interpretação dos Coeficientes: Análise dos parâmetros do modelo, valores-p e intervalos de confiança.**

**• Cálculo do Odds Ratio: Transformação dos coeficientes em razões de chance para interpretação prática.**

**Validação e Avaliação do Modelo**

**• Matriz de Confusão:** Avaliação do desempenho preditivo do modelo.

**• Métricas de Classificação:** Cálculo de precisão, recall e acurácia.

**• Curva ROC:** Análise da capacidade discriminatória do modelo.

### Principais Questões de Negócio e Insights

##### A. Fatores Determinantes do Churn (O que faz o cliente cancelar?)

**Questão:** Quais características do cliente e do serviço aumentam ou diminuem significativamente o risco de churn?

**Análise Realizada:** Modelagem com Regressão Logística e análise de significância estatística (p-valor < 0.05).

**Insight Principal:** O tipo de contrato é o fator mais determinante. Clientes com contrato mensal têm um risco 195 vezes maior de churn comparado à referência (contrato anual). Em contraste, contratos de 2 anos reduzem o risco em aproximadamente 72%.

##### B. Magnitude do Impacto (Quanto cada fator importa?)

**Questão:** Como quantificar o efeito de cada variável na probabilidade de cancelamento?

**Análise Realizada:** Cálculo e interpretação do Odds Ratio para cada variável significativa.

**Insight Principal:**

**• Fidelidade:** Cada mês adicional de relacionamento reduz o risco de churn em ~5.4%.

**• Fatura:** Cada aumento de R$ 1,00 na fatura mensal aumenta o risco em ~3.2%.

**• Serviço:** Clientes com Fibra Óptica têm 4.3 vezes mais chance de cancelar do que clientes com DSL.

##### C. Perfil de Cliente de Alto Risco (Quem pode cancelar?)

**Questão:** Como identificar proativamente os clientes com maior propensão ao churn?

**Análise Realizada:** Desenvolvimento de um sistema de scoring baseado nas probabilidades preditas pelo modelo.

**Insight Principal:** O perfil de alto risco combina: Contrato Mensal + Serviço Fibra + Baixa Fidelidade (< 6 meses) + Fatura Elevada. Para estes clientes, a probabilidade estimada de churn pode ultrapassar 85%.

##### D. Estratégias de Retenção (O que fazer para evitar o cancelamento?)

**Questão:** Quais ações concretas a empresa deve priorizar com base nos dados?

**Análise Realizada:** Tradução dos insights estatísticos em recomendações estratégicas com impacto e ROI estimado.

**Insight Principal:**

**Prioridade ALTA:** Converter contratos mensais em anuais/bienais (potencial de 40-50% de redução no churn deste grupo).

**Prioridade ALTA:** Programa de retenção intensivo para clientes nos 6 primeiros meses.

**Prioridade MÉDIA:** Revisão da precificação/valor percebido do serviço de Fibra Óptica.

### Como Executar o Projeto
Pré-requisitos: Certifique-se de ter o Python (preferencialmente com o ambiente Anaconda/Miniconda) e o VS Code (com a extensão Jupyter) instalados.

#### 1. Pré-requisitos: 

Necessário ter o Python (versão 3.9 ou superior) instalado. É recomendado a instalação do ambientes Anaconda. Para uma melhor experiência de edição, pode-se usar o VS Code com a extensão do Jupyter.

#### 2. Clone o Repositório:

```bash
git clone https://github.com/Samu3lsilvvv/Analise-Churn
cd Analise-Churn
```

#### 3. Instalar as Dependências:

Instale as bibliotecas Python necessárias

```bash
pip install pandas numpy statsmodels matplotlib seaborn plotly scikit-learn jupyter
```

#### 4.Iniciar o Notebook:

Execute o Jupyter Notebook e abra o arquivo analise_churn

```bash
jupyter notebook
```
## Principais Descobertas

## Fatores que AUMENTAM Churn:
1. **Contrato Mensal** → 195x maior risco (Odds Ratio: 195.18)
2. **Serviço Fibra Óptica** → 4.3x maior risco
3. **Fatura Elevada** → +3.2% por R$1

### Fatores que REDUZEM Churn:
1. **Fidelidade** → -5.4% por mês adicional
2. **Contrato de 2 Anos** → -72% menor risco

### Performance do Modelo:
- **Pseudo R²:** 0.6451 (65% de explicação)
- **Todas variáveis principais:** p-valor < 0.05

### Resultados e Visualizações

O projeto inclui visualizações como:

**Taxa de Churn Geral -** Gráfico de pizza interativo

**Churn por Tipo de Contrato -** Gráfico de barras

**Distribuição da Fidelidade -** Histograma com boxplot

**Impacto da Fatura -** Análise de distribuição

**Odds Ratio -** Impacto visual das variáveis

### Técnicas Aplicadas

**Análise Estatística:** Regressão Logística, Odds Ratio, Intervalos de Confiança

**Visualização de Dados:** Gráficos estáticos e interativos

**Python para Data Science:** Pandas, NumPy, Statsmodels

**Business Intelligence:** Recomendações acionáveis com ROI estimado

### Metodos utilizados

**Definição do Problema -** Contexto de negócio em telecomunicações

**Geração de Dados -** Dataset sintético realista (2.000 clientes)

**Análise Exploratória -** EDA completo com visualizações

**Modelagem Estatística -** Regressão Logística com validação

**Interpretação -** Coeficientes, Odds Ratio, significância

**Conclusões -** Insights acionáveis e recomendações

### Formação:

Curso em andamento: **Fundamentos de Python para Data Science (Data Science Academy)**
