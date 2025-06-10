# Desafio_TelecomX_BR

# Análise de Evasão de Clientes (Churn Prediction)

![Badge de Status](https://img.shields.io/badge/Status-Conclu%C3%ADdo-brightgreen)
![Badge de Linguagem](https://img.shields.io/badge/Linguagem-Python-blue)
![Badge de Ferramentas](https://img.shields.io/badge/Ferramentas-Pandas%2C%20Numpy%2C%20Matplotlib%2C%20Seaborn-orange)

---

## 📝 Descrição do Projeto

Este projeto tem como objetivo principal **analisar e compreender os fatores que levam à evasão de clientes (Churn)** da empresa Telecom X BR. Através da **Análise Exploratória de Dados (EDA)**, limpeza e tratamento de dados, buscamos identificar padrões de comportamento e características dos clientes que cancelam seus serviços, fornecendo insights valiosos para a criação de estratégias de retenção.

### 🎯 Objetivo

* **Identificar os principais fatores de churn:** Quais características de clientes e serviços estão mais associadas à evasão.
* **Quantificar a taxa de churn:** Entender a dimensão do problema.
* **Gerar insights acionáveis:** Oferecer recomendações baseadas em dados para reduzir a evasão de clientes.

---

## 📊 Estrutura do Projeto

O projeto está organizado da seguinte forma:

* `[Desafio_TelecomX_BR_FinaL.ipynb]`: O notebook principal que contém todo o código de análise, desde a importação dos dados até a apresentação dos resultados e conclusões.
* `README.md`: Este arquivo de descrição do projeto.

---

## 🛠️ Tecnologias e Ferramentas Utilizadas

As seguintes tecnologias e bibliotecas Python foram utilizadas neste projeto:

* **Python** (versão [ex: 3.9+])
* **Pandas**: Manipulação e análise de dados.
* **NumPy**: Suporte a operações numéricas de alto desempenho.
* **Matplotlib**: Criação de visualizações estáticas.
* **Seaborn**: Criação de visualizações estatísticas atraentes.
* **Colab Notebook**: Ambiente de desenvolvimento interativo.

---

## 🚀 Como Executar o Projeto

Siga os passos abaixo para configurar e executar este projeto localmente:

### Pré-requisitos

Certifique-se de ter o Python instalado. Recomenda-se o uso de um ambiente virtual.

1.  **Clone o Repositório:**
    ```bash
    git clone [Desafio_TelecomX_BR_FinaL.ipynb]
    cd [(https://github.com/leandrotadeudcl/Desafio_TelecomX_BR)]
    ```

2.  **Crie um Ambiente Virtual (Opcional, mas Recomendado):**
    ```bash
    python -m venv venv
    ```

3.  **Ative o Ambiente Virtual:**
    * **Windows:**
        ```bash
        .\venv\Scripts\activate
        ```
    * **macOS/Linux:**
        ```bash
        source venv/bin/activate
        ```

4.  **Instale as Dependências:**
    ```bash
    pip install pandas numpy matplotlib seaborn jupyter
    ```
    *(Dica: Se você tiver um `requirements.txt`, use `pip install -r requirements.txt`)*

5.  **Inicie o Google Colaboratory:**
    ```bash
    Google Colaboratory
    ```

6.  **Abra o Notebook:**
    No navegador, navegue até o arquivo `[Desafio_TelecomX_BR_FinaL.ipynb]` (ou `main.ipynb`) e abra-o. Você pode executar as células sequencialmente para reproduzir a análise.

---

## 📈 Análise Realizada

O projeto percorreu as seguintes etapas principais:

1.  **Limpeza e Pré-processamento de Dados:**
    * Tratamento de valores ausentes (ex: na coluna `charges_Total`).
    * Conversão de tipos de dados (ex: `charges_Total` de `object` para `float`).
    * Remoção de linhas com `Churn` vazio.
    * Mapeamento de variáveis categóricas binárias (ex: `gender`, `Partner`, `Churn`) para valores numéricos (0 e 1).
    * Aplicação de One-Hot Encoding para variáveis categóricas multiclasse (ex: `InternetService`, `Contract`).
    * Criação da nova feature `Contas_Diarias`.

2.  **Análise Descritiva:**
    * Cálculo de métricas estatísticas (média, mediana, desvio padrão, etc.) para entender a distribuição das variáveis numéricas.
    * Análise da proporção geral de Churn.

3.  **Análise Exploratória de Dados (EDA):**
    * **Churn vs. Variáveis Categóricas:** Visualizações (gráficos de barras) para entender como o Churn se distribui entre diferentes categorias (gênero, tipo de contrato, método de pagamento, etc.). Foram identificados segmentos de clientes com maior propensão ao churn.
    * **Churn vs. Variáveis Numéricas:** Análise (histogramas, KDE, box plots) da distribuição de variáveis como `tenure`, `charges_Monthly`, `charges_Total` e `Contas_Diarias` para clientes com e sem churn, revelando tendências importantes.
    * **Análise de Correlação (Opcional):** Exploração da correlação entre as variáveis e a variável `Churn`, identificando os fatores com maior relação linear para futuras modelagens. Uma nova feature `Num_Servicos_Contratados` também foi criada e analisada em relação ao churn.

---

## 💡 Conclusões e Insights Principais

* **Desbalanceamento de Classes:** O dataset apresenta um desbalanceamento significativo na variável alvo (`Churn`), com a maioria dos clientes não evadindo.
* **Período Crítico de Churn:** Clientes com **menor tempo de contrato (`tenure` baixo)** são os mais suscetíveis à evasão.
* **Contrato Mês a Mês:** O tipo de contrato **mês a mês** é um forte preditor de churn, indicando menor fidelidade.
* **Método de Pagamento:** Clientes que utilizam **cheque eletrônico** possuem uma taxa de churn consideravelmente mais alta.
* **Valor Agregado do Serviço:** A ausência de serviços adicionais como **segurança online e suporte técnico** correlaciona-se com maior churn, enquanto clientes com mais serviços contratados tendem a ter menor churn.
* **Custo do Serviço:** Clientes com **cobranças mensais mais altas** também demonstram maior tendência a cancelar.

---

## 📝 Recomendações

Com base nas análises, as seguintes recomendações estratégicas podem ser consideradas:

* **Foco na Retenção de Novos Clientes:** Implementar programas de engajamento e ofertas especiais nos **primeiros meses de serviço** para clientes com baixo `tenure`.
* **Incentivo a Contratos de Longo Prazo:** Criar promoções ou benefícios exclusivos para clientes que optarem por contratos anuais ou bianuais.
* **Otimização do Processo de Pagamento:** Investigar a experiência dos clientes que utilizam cheque eletrônico e explorar alternativas ou melhorias para este método, ou incentivar a migração para métodos mais estáveis.
* **Promoção de Serviços de Valor Agregado:** Campanha de marketing para destacar os benefícios de serviços como segurança online e suporte técnico, mostrando como eles aumentam o valor percebido do plano.
* **Revisão de Planos de Alto Custo:** Avaliar a competitividade e o valor entregue nos pacotes de alta cobrança mensal, considerando a insatisfação de clientes que os contratam.

---

## 📧 Contato

Se você tiver alguma dúvida ou sugestão, sinta-se à vontade para entrar em contato:

* **[Leandro Tadeu Damasceno Castro Leite]**
* **[leandro.tadeu.dcl@gmail.com]**
* **[www.linkedin.com/in/leandro-tadeu]**
* **[Link para seu GitHub (Opcional)]**
