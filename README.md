# PROJETO: Análise e Previsão de Churn - Telecom X

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-data_analysis-brightgreen?logo=pandas)](https://pandas.pydata.org/docs/)
[![Seaborn](https://img.shields.io/badge/Seaborn-visualization-blue?logo=seaborn)](https://seaborn.pydata.org/)
[![Scikit Learn](https://img.shields.io/badge/Scikit--Learn-machine_learning-yellow?logo=scikit-learn)](https://scikit-learn.org/stable/)
[![NumPy](https://img.shields.io/badge/NumPy-numerical-blueviolet?logo=numpy)](https://numpy.org/doc/)

# 🎯 **Objetivo**
Este projeto tem como propósito prever a **evasão de clientes (churn)** em uma empresa de telecomunicações fictícia — a **Telecom X** — utilizando técnicas de **Machine Learning** e **análise exploratória de dados**. Este projeto foi criado para o challenge 3 do programa da **Oracle One**, formação de Data Science, do qual faço parte.

Este projeto tem o objetivo de desenvolver e práticas os conhecimentos adquiridos na formação a fim de torná-lo em habilidades práticas.

---

## 🚀 Visão Geral

Este projeto, desenvolvido por **Lucas Esteves Costa** (GitHub: [@LucasEstevesCosta](https://github.com/LucasEstevesCosta)), tem como objetivo a análise exploratória e preditiva do *churn* (evasão de clientes) da empresa fictícia **Telecom X**. 

O projeto realiza um estudo completo que envolve desde o carregamento e limpeza dos dados até a criação de modelos de machine learning para previsão de churn.

---

## 📑 Conteúdo do Projeto: 
### 📋 Sumário

1. [📦 Extração dos Dados](#extração-dos-dados)
   - [⬇️ Carregamento do Dataset](#carregamento-do-dataset)
   - [🔍 Exploração Inicial](#exploração-inicial)
2. [🧹 Preparação dos Dados](#preparação-dos-dados)
   - [🗑️ Remoção de Colunas](#remoção-de-colunas)
   - [📝 Ajuste de Categorias](#ajuste-de-categorias)
   - [🚫 Tratamento de Valores Ausentes](#tratamento-de-valores-ausentes)
   - [🔢 Encoding de Variáveis](#encoding-de-variáveis)
3. [🧮 Análise de Multicolinearidade](#análise-de-multicolinearidade)
   - [🔗 Agrupamento de Categorias Colineares](#agrupamento-de-categorias-colineares)
   - [📊 Cálculo do VIF](#cálculo-do-vif)
   - [❌ Remoção de Variáveis Redundantes](#remoção-de-variáveis-redundantes)
4. [🤖 Construção e Teste dos Modelos](#construção-e-teste-dos-modelos)
   - [🔀 Separação Treino/Teste](#separação-treino-teste)
   - [🏗️ Criação dos Modelos](#criação-dos-modelos)
   - [⚖️ Balanceamento dos Dados](#balanceamento-dos-dados)
   - [📈 Avaliação dos Modelos](#avaliação-dos-modelos)
5. [💾 Exportação dos Modelos](#exportação-dos-modelos)
   - [📤 Salvando o Modelo](#salvando-o-modelo)
   - [📥 Carregando e Usando o Modelo](#carregando-e-usando-o-modelo)
6. [📊 Relatório Final](#relatório-final)

---

## 📦 Extração dos Dados

### ⬇️ Carregamento do Dataset
- O conjunto de dados é carregado diretamente do GitHub para facilitar o uso.

### 🔍 Exploração Inicial
- São verificadas as colunas, tipos de dados e valores ausentes.

## 🧹 Preparação dos Dados

### 🗑️ Remoção de Colunas
- Remoção de colunas sem valor preditivo (ex: `id_cliente`).

### 📝 Ajuste de Categorias
- Ajuste de categorias para facilitar a análise.

### 🚫 Tratamento de Valores Ausentes
- Tratamento de valores ausentes para garantir qualidade dos dados.

### 🔢 Encoding de Variáveis
- Transformação de variáveis categóricas em numéricas (OneHotEncoder).

## 🧮 Análise de Multicolinearidade

### 🔗 Agrupamento de Categorias Colineares
- Agrupamento de categorias colineares para evitar redundância.

### 📊 Cálculo do VIF
- Análise de VIF para identificar variáveis com alta multicolinearidade.

### ❌ Remoção de Variáveis Redundantes
- Remoção das variáveis identificadas como redundantes pelo VIF.

## 🤖 Construção e Teste dos Modelos

### 🔀 Separação Treino/Teste
- Separação dos dados em conjuntos de treino e teste.

### 🏗️ Criação dos Modelos
- Criação de diferentes modelos preditivos (Random Forest, XGBoost).

### ⚖️ Balanceamento dos Dados
- Aplicação de técnicas de balanceamento para melhorar o desempenho dos modelos.

### 📈 Avaliação dos Modelos
- Avaliação dos modelos por métricas como ROC AUC e F1 Score.

## 💾 Exportação dos Modelos

### 📤 Salvando o Modelo
- Após treinar os modelos, eles podem ser exportados para uso futuro em arquivos `.pkl` usando o módulo `pickle`.

Após treinar os modelos, eles podem ser exportados para uso futuro.  
**Como exportar e usar os modelos:**

- Os modelos são salvos em arquivos `.pkl` usando o módulo `pickle`.
- Para usar um modelo exportado:
  1. Instale Python e as bibliotecas necessárias (`scikit-learn`, `xgboost`).
  2. Carregue o modelo com o comando:
     ```python
     import pickle
     with open('nome_do_arquivo_modelo.pkl', 'rb') as f:
         modelo = pickle.load(f)
     # Para fazer previsões:
     resultado = modelo.predict(novos_dados)
     ```
  3. Substitua `novos_dados` pelos dados que deseja analisar.
- Não é necessário conhecimento avançado: basta seguir o exemplo acima.

## 📊 Relatório Final

- Apresenta as principais conclusões do projeto, como fatores que influenciam a evasão de clientes.
- Interpretações dos resultados dos modelos.
