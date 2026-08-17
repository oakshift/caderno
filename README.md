# Caderno

Registo diário de treino e nutrição, numa única página HTML sem dependências.

## O que faz

- **Suplementos** — quatro tomas diárias com contador de dias seguidos
- **Proteína** — lista de ~37 alimentos com a proteína por porção real, filtro vegan,
  e soma ao total do dia
- **Treino** — três sessões de força sem equipamento, cada exercício com dica de
  execução e uma escada de progressão (a progressão é por nível, não por carga)
- **Métricas** — peso, perímetro abdominal e razão cintura/altura
- **Dados** — resumo em texto para copiar, cópia de segurança em `.json` e restauro

## Privacidade

Todo o registo fica em `localStorage`, no browser onde a app é usada. Não há servidor,
não há conta, não há pedidos de rede. Limpar os dados de navegação apaga o registo —
use a cópia de segurança em `.json`.

## Usar no telemóvel

Abra a página e adicione ao ecrã principal:

- **iOS / Safari** — Partilhar → Adicionar ao ecrã principal
- **Android / Chrome** — menu → Adicionar ao ecrã principal

Use sempre a mesma forma de abrir (ícone *ou* browser), porque o armazenamento local
pode ser separado entre os dois contextos.

## Desenvolvimento

Não há build. `index.html` é o projeto inteiro — HTML, CSS e JavaScript num ficheiro.
Para testar localmente:

```sh
python3 -m http.server 8000
```
