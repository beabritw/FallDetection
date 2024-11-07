# <span style="font-size: 2em;"> Fall Detection - Detecção de Quedas em Idosos com Lógica Fuzzy </span>

Este projeto usa lógica fuzzy para estimar o risco de quedas em idosos com base em dados de sensores de movimento e orientação. O objetivo é monitorar continuamente as atividades físicas de pessoas idosas para identificar situações de risco de queda, podendo auxiliar em sistemas de monitoramento para cuidados com a saúde.

## Índice

- [Visão Geral](#visão-geral)
- [Funcionamento do Projeto](#funcionamento-do-projeto)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)
- [Visualizações](#visualizações)


###Visão Geral
Este projeto processa dados de sensores (acelerômetros e giroscópios) que registram o movimento e a orientação do corpo. Usando lógica fuzzy, ele determina o nível de risco de queda para cada entrada de dados dos sensores. O sistema cria um modelo que atribui uma pontuação de risco de queda de acordo com o padrão de movimentação.

###Funcionamento do Projeto
- Carregamento de Dados: O dataset contendo dados dos sensores é carregado, e as colunas relevantes (aceleração e giroscópio) são selecionadas.
- Pré-processamento: As colunas são convertidas para valores numéricos, substituindo dados inválidos por NaNs e removendo-os para evitar erros.
- Normalização: Os dados de aceleração e giroscópio são normalizados para o intervalo de -10 a 10.
- Lógica Fuzzy:
  - Cria variáveis fuzzy para aceleração e giroscópio.
  - Define regras fuzzy para determinar o risco de queda (baixo, médio, alto).
  - O modelo de controle fuzzy é executado sobre os dados para calcular o risco de queda.
- Visualização: O código fornece gráficos das funções de pertinência e uma matriz de correlação entre os sensores.

###Tecnologias Utilizadas
- Python: Linguagem principal do projeto.
- Bibliotecas:
  - numpy e pandas para manipulação de dados.
  - skfuzzy para implementação da lógica fuzzy.
  - matplotlib e seaborn para visualização de dados.
