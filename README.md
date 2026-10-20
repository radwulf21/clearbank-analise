# ClearBank - Analise Financeira com Python

Este repositorio contem a solucao do Desafio Final do modulo de Python, focado no processamento, validacao e analise de transacoes bancarias para a fintech ClearBank.

## Descricao do Projeto

O objetivo do projeto e ler um arquivo CSV de transacoes bancarias (transacoes.csv) contendo inconsistencias frequentes (registros vazios, formatos incorretos de data e valores invalidos), aplicar regras de limpeza rigorosas, calcular metricas financeiras mensais, sinalizar movimentacoes suspeitas acima de R$ 10.000,00 e exportar o resultado consolidado em formato JSON, alem de gerar uma visualizacao grafica dos dados.

## Estrutura do Repositorio

clearbank-analise/

├── desafio-final.ipynb     # Notebook principal com o codigo e saidas salvas

├── transacoes.csv          # Base de dados em CSV (gerada no notebook)

├── relatorio.json          # Arquivo JSON exportado com metricas e suspeitas

├── grafico.png             # Grafico de barras (Credito vs Debito por mes)

└── README.md               # Documentacao do projeto

## Tecnologias e Modulos Utilizados

* Python 3.10+
* csv: Leitura nativa e estruturada de arquivos CSV via DictReader.
* datetime: Conversao de texto para objetos de data, agrupamento por mes e calculo do intervalo de dias.
* json: Exportacao dos dados consolidados em formato JSON formatado (indent=2, utf-8).
* matplotlib: Geracao e exportacao do grafico de barras comparativo (grafico.png).

## Como Executar o Projeto

### Opcao 1: No Google Colab
1. Abra o arquivo desafio-final.ipynb no Google Colab.
2. Va ao menu Ambiente de execucao e clique em Executar tudo (ou aperte Ctrl + F9).
3. A primeira celula cria a massa de dados transacoes.csv automaticamente e executa todas as etapas de validacao, relatorio e exportacao.

### Opcao 2: Localmente (Jupyter Notebook / VS Code)
1. Clone o repositorio:
   git clone https://github.com/seu-usuario/clearbank-analise.git
   cd clearbank-analise

2. Instale as bibliotecas necessarias para a visualizacao de dados:
   pip install matplotlib numpy

3. Abra o notebook desafio-final.ipynb e execute as celulas sequencialmente.

## Arquivos Gerados na Execucao

1. transacoes.csv: Massa de dados de entrada contendo registros validos e invalidos para testes do pipeline de validacao.
2. relatorio.json: Contem a data da execucao, contagem de registros validos e invalidos, resumo mensal detalhado (credito, debito, saldo, media, maior e menor valor) e a lista de transacoes com valor superior a R$ 10.000,00.
3. grafico.png: Grafico comparativo exibindo a evolucao financeira dos creditos e debitos ao longo dos meses analisados.
