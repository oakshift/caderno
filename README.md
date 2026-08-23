# Plano de treino e alimentação

Registo diário de treino e nutrição, numa única página HTML sem dependências.

## O que faz

- **Suplementos** — quatro tomas diárias com contador de dias seguidos
- **Proteína** — lista de ~37 alimentos com a proteína por porção real, filtro vegan,
  e soma ao total do dia
- **Treino** — três sessões de força sem equipamento, cada exercício com dica de
  execução e uma escada de progressão (a progressão é por nível, não por carga)
- **Métricas** — peso, perímetro abdominal e razão cintura/altura, com histórico
  de cada um e a variação face ao registo anterior
- **Tensão arterial** — sete dias, quatro medições por dia (duas de manhã, duas à
  noite). A média exclui o primeiro dia, que é sistematicamente o mais alto
- **Compras** — lista que se risca a um toque; o que arruma vai para os habituais e
  volta a entrar com um toque na semana seguinte
- **Dados** — exportação em `.json` e restauro

## Privacidade

Todo o registo fica em `localStorage`, no browser onde a app é usada. Não há servidor,
não há conta, não há pedidos de rede. Limpar os dados de navegação apaga o registo —
use a cópia de segurança em `.json`.

## Instalar no telemóvel

### Android

No Chrome (ou noutro browser Chromium):

1. Menu dos três pontos
2. **Instalar aplicação** ou **Adicionar ao ecrã principal**
3. Confirmar

No Android a app instalada partilha o armazenamento com o browser, na mesma origem —
pode alternar entre o ícone e o browser sem perder registos.

### iOS

Tem de ser no **Safari**: Partilhar → **Adicionar ao ecrã principal**.

⚠ No iOS, uma página adicionada ao ecrã principal pode ter armazenamento **separado**
do Safari. Escolha uma das duas formas de abrir e use sempre a mesma, ou os registos
de uma não aparecem na outra.

## Compatibilidade

Escrito em JavaScript ES5, sem `let`/`const`, arrow functions, template literals nem
`NodeList.forEach` — para correr em WebViews Android antigos. Erros não tratados são
mostrados na própria página em vez de falharem em silêncio.

## Desenvolvimento

Não há build. `index.html` é o projeto inteiro — HTML, CSS e JavaScript num ficheiro.
Para testar localmente:

```sh
python3 -m http.server 8000
```
