# Credit Risk Machine Learning

Projeto de Machine Learning para análise de risco de crédito e previsão de inadimplência.

## Objetivo do projeto

O objetivo deste projeto é construir modelos de classificação capazes de prever se um cliente possui maior risco de inadimplência.

Este projeto faz parte da minha evolução prática em Ciência de Dados, com foco em problemas reais de negócio, avaliação de modelos e interpretação de resultados.

## Tipo de problema

Este é um problema de classificação binária.

A variável alvo é:

- `inadimplente`
  - 0: cliente não inadimplente
  - 1: cliente inadimplente

## Dados utilizados

Foi utilizado um dataset simulado com 1.000 clientes, contendo variáveis financeiras e comportamentais relacionadas ao risco de crédito.

Principais variáveis:

- idade
- renda mensal
- valor do empréstimo
- histórico de atraso
- score de crédito
- tempo de emprego
- empréstimos anteriores
- relação entre empréstimo e renda
- inadimplente

## Etapas do projeto

- Criação do dataset inicial
- Salvamento dos dados em CSV
- Carregamento dos dados
- Análise exploratória
- Verificação da distribuição da variável alvo
- Análise de score de crédito
- Análise de renda mensal
- Criação da variável relação empréstimo/renda
- Análise do histórico de atraso
- Matriz de correlação
- Separação entre treino e teste
- Padronização dos dados para Logistic Regression
- Treinamento de modelos de classificação
- Avaliação com métricas de classificação
- Comparação entre modelos
- Salvamento dos resultados

## Modelos utilizados

Foram treinados dois modelos:

- Logistic Regression
- Random Forest Classifier

## Métricas de avaliação

As principais métricas utilizadas foram:

- Accuracy
- Precision
- Recall
- F1-score
- ROC AUC
- Matriz de confusão

Em problemas de risco de crédito, o recall da classe inadimplente é uma métrica muito importante, pois indica a capacidade do modelo de identificar clientes com maior risco.

## Resultados

| Modelo | Acurácia | Precision Classe 1 | Recall Classe 1 | F1-score Classe 1 | ROC AUC |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | 0.9200 | 0.9298 | 0.8154 | 0.8689 | 0.9812 |
| Random Forest Classifier | 0.9550 | 0.9118 | 0.9538 | 0.9323 | 0.9896 |

## Interpretação dos resultados

O modelo Random Forest Classifier apresentou o melhor desempenho geral.

O principal ganho foi no recall da classe 1, que representa os clientes inadimplentes.

Enquanto a Logistic Regression identificou cerca de 82% dos clientes inadimplentes, o Random Forest identificou cerca de 95%.

Em um contexto de risco de crédito, esse resultado é importante porque reduz a quantidade de falsos negativos, ou seja, clientes inadimplentes que poderiam ser aprovados sem identificação adequada de risco.

## Resultado visual

A tabela comparativa dos modelos foi salva em:

```text
outputs/comparacao_modelos_credito.png