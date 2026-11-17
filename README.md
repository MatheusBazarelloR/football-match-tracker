# placar-dados

Repositório de estudo de Git e programação. O projeto principal é uma **base de dados de partidas de futebol**, construída em etapas. Cada etapa reforça uma linguagem ou tecnologia diferente, e no fim vira a base de um agregador de dados de futebol.

## Objetivo

Registrar partidas de futebol, guardá-las em um banco de dados e gerar estatísticas simples. Aprender de verdade cada linguagem, usando IA só para explicar, revisar e discutir, nunca para entregar código pronto.

## Etapa 1: estrutura e coleta de dados (Python + SQLite)

### O que o programa precisa fazer

- Cadastrar uma **partida** (data, competição, time da casa, time visitante, gols de cada um)
- Cadastrar e listar **times** e **competições**
- Listar as partidas de um mês, de uma competição ou de um time
- Mostrar a **campanha** de um time: jogos, vitórias, empates, derrotas, gols pró/contra, saldo e pontos
- Importar partidas de um arquivo CSV

### Modelagem dos dados

- Tabela `times`: id, nome
- Tabela `competicoes`: id, nome
- Tabela `partidas`: id, data, competicao_id, time_casa_id, time_fora_id, gols_casa, gols_fora
- Regras: o resultado não é guardado, é calculado a partir dos gols; gols nunca são negativos; um time não joga contra ele mesmo

### Estrutura de pastas planejada

- `src/` código Python
- `data/` banco SQLite e CSVs de exemplo (começar com 20 a 30 jogos reais do Cruzeiro)
- `tests/` testes simples

### Pronto quando

- [ ] O banco é criado automaticamente na primeira execução
- [ ] Consigo cadastrar e listar times, competições e partidas pelo terminal
- [ ] A campanha de um time bate com a conta feita à mão
- [ ] A importação de CSV recusa linhas inválidas e avisa qual linha falhou

## Decisões em aberto

- Guardar o resultado no banco ou calcular sempre? Por quê?
- Como tratar pênaltis em jogos de mata-mata?
- Como tratar data inválida, gols negativos ou partida duplicada (mesma data e mesmos times)?
- Competição é obrigatória na partida?

## Próximas etapas

2. Refazer o domínio em Java com JDBC e PostgreSQL
3. Programa em C que lê um CSV de partidas e soma pontos por time
4. API com os dados e front-end em JavaScript (o agregador em si)
5. Previsão de resultado ou gols com regressão linear (scikit-learn)
6. Subir o banco e a aplicação no Google Cloud

## Regras de aprendizado

- Tento escrever sozinho antes de perguntar
- Se não sei explicar uma linha, ela não entra no commit
- Escrevo os testes eu mesmo

## Como contribuir comigo mesmo

Uma branch por funcionalidade, commits pequenos e mensagens claras.
