# Redes Complexas Aplicadas ao Mercado Financeiro Brasileiro

Este repositório contém o código, análises e resultados do (TCC)  **"Redes Complexas Aplicadas ao Mercado Financeiro Brasileiro"**.  
O objetivo principal do estudo é aplicar técnicas de redes complexas para investigar a estrutura de interdependência entre ativos da bolsa brasileira (B3) ao longo de diferentes períodos. Utilizando dados financeiros reais, o trabalho realiza:

- Redução de dimensionalidade com Análise de Componentes Principais (PCA)  
- Construção de redes de correlação entre ativos  
- Detecção de comunidades usando o algoritmo de Louvain  
- Cálculo de centralidades para identificar ativos influentes  
- Construção de carteiras experimentais baseadas em estrutura de rede  
- Comparação de desempenho das carteiras frente a benchmarks do mercado  

---

## 📁 Estrutura das Pastas e Descrição

### `1-coleta-precos-ajustados-b3-yfinance-jan-fev-2024`  
Realiza a leitura e limpeza dos arquivos da B3 (`COTAHIST`) para janeiro e fevereiro de 2024. Filtra os papéis relevantes e coleta dados de preços ajustados dos ativos via Yahoo Finance (`yfinance`).

---

### `2-retornos-log-janeiro-fevereiro-2024`  
Calcula e plota os retornos logarítmicos diários dos ativos com base nos preços de fechamento ajustado para janeiro e fevereiro de 2024. Inclui tratamento de dados e visualização dos retornos ao longo do tempo.

---


### `3-pca-redes-carteiras-jan-fev-2024`  
Aplica padronização dos retornos e Análise de Componentes Principais (PCA) nos dados dos ativos. Utiliza os componentes principais para calcular a matriz de correlação e construir redes com threshold 0.7, representando as inter-relações entre os ativos.

---

### `4-louvain-centralidade-redes-financeiras-jan-fev-2024`  
Aplica o algoritmo de Louvain nas redes construídas para identificar comunidades de ativos. Calcula métricas de centralidade (grau, betweenness, autovetor, closeness) e realiza 100 execuções do algoritmo para avaliar a robustez da partição em fevereiro.

---

### `5-carteiras-experimentais-comunidades-top-grau-jan-fev-2024`  
Seleciona os dois ativos com maior centralidade de grau dentro das cinco maiores comunidades para cada mês. Constrói carteiras experimentais e compara seus preços normalizados ao longo do tempo.

---

### `5-avaliacao-carteiras-benchmark-jan-fev-2024`  
Compara o desempenho das carteiras experimentais frente a benchmarks do mercado (IBOV, Small Caps, Dividendos). Calcula retorno total, volatilidade anualizada e índice de Sharpe, com visualizações comparativas dos preços normalizados.

---
