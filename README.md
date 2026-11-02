# Plano de treino e medicação

Registo diário de medicação e treino, numa única página HTML sem dependências.

## O que faz

- **Hoje** — a medicação do dia, um toque por item ou "Tomei tudo"; o treino marcado
  para hoje, ou quantos faltam na semana; e os últimos sete dias, para registar o que
  ficou por registar
- **Treino** — sessões de força sem equipamento, cada exercício com dica de execução,
  vídeo e uma escada de níveis (a progressão é por nível, não por carga)
- **Progresso** — treinos por semana, dias com a medicação toda, nível de cada
  exercício e histórico das subidas, peso
- **Ajustes** — lista de medicação, dias de treino, lembretes em `.ics` para o
  calendário, ligação ao GitHub

Carregar e manter premido o ícone da app mostra o atalho **Tomei tudo**.

## Onde ficam os dados

Num repositório **privado** à parte (`caderno-dados`, ficheiro `dados.json`), lido e
escrito pela app com um token do GitHub guardado só no browser. Cada registo é um
commit. Sem rede, os registos ficam no telemóvel e seguem quando houver ligação.

À primeira abertura, a app importa sozinha o registo da versão anterior que estiver no
mesmo browser (medicação, treinos, níveis e peso; a alimentação fica de fora).

## Instalar no telemóvel

No Chrome: menu dos três pontos → **Instalar aplicação** ou **Adicionar ao ecrã principal**.
