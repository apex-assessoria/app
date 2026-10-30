# APEX — `app.marketingapex.com.br`

Projeto do subdomínio `app` da Apex. HTML estático, sem build e sem
dependência: abre do disco com dois cliques.

Criado em 29/10/2026.

---

## De onde ele nasceu

O `index.html` e o `404.html` são uma **cópia do site que está no ar** em
`www.marketingapex.com.br`, baixada do próprio ar em 29/10/2026. A cópia é o
ponto de partida: garante que o subdomínio nasça com a identidade visual certa,
sem ninguém reconstruir paleta e fonte de cabeça.

⚠ **O repositório `apex-assessoria/site` não serve de referência visual.** Ele
usa uma paleta antiga (`#E79E14`, fonte Inter) que não é mais a da Apex.

## A identidade

Os tokens vivem no `<style>` do `index.html`, como variáveis CSS:

```
--ink   #070605    fundo          --gold       #FCBE09   primária
--fg    #F3EEE2    texto          --on-gold    #120e00   texto sobre dourado
--mute  #A39C8B    texto fraco    --gold-soft  #FFDA6B
--line  rgba(255,236,190,.10)     --gold-deep  #8A6400

Archivo (display) · Instrument Serif · JetBrains Mono (mono)
raios 12 / 18 / 24px · altura da nav 64px
```

## O que ainda não foi decidido

**O que esta página vai ser.** Hoje ela é a cópia do site institucional, e o
conteúdo próprio do `app` ainda não existe. Enquanto não existir, o que está
aqui é ponto de partida, não entrega.

## O que este projeto não tem, de propósito

Sem servidor, sem banco e sem etapa de build. **Nenhuma página grava dado
nenhum.** Se algo pedir formulário que persiste, é projeto novo — e a decisão de
onde ele mora vem antes do código.
