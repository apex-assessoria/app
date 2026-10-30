# APEX — `app.marketingapex.com.br`

Instruções do projeto. Quem abrir esta pasta lê isto automaticamente, de
qualquer máquina e de qualquer conta.

Atualize junto com o código: decisão que não está escrita aqui some na primeira
troca de mão.

---

## O que é

Página do subdomínio `app` da Apex. **HTML estático**, sem build, sem framework,
sem dependência.

```
index.html    a página
404.html      a página de erro
vercel.json   cleanUrls e trailingSlash
```

O `index.html` nasceu como cópia do site no ar em `www.marketingapex.com.br`.
A identidade visual mora nas variáveis CSS do `<style>` dele — `--ink`, `--fg`,
`--gold` e as demais. **Cor nova se declara como variável ali**, não solta no
meio do documento.

⚠ **O repositório `apex-assessoria/site` tem a paleta antiga** (`#E79E14`,
Inter) e não serve de referência visual para nada aqui.

## O que este projeto não tem, de propósito

Não há servidor, banco de dados nem etapa de build. **Nenhuma página grava dado
nenhum.** Se algo pedir formulário que persiste, é projeto novo, não é esta
página — e a decisão de onde ele mora vem antes do código.

## A regra que explica a estrutura

**Transferência não é migração.** Um repositório por projeto, nunca um
repositório só para tudo — é o que permite um projeto sair sem levar o histórico
do vizinho. Projeto novo nasce como pasta irmã desta, com `git init` próprio.

## Como contribuir sem atropelar o deploy

O deploy sai do Git. Push direto no branch de produção **publica sem ninguém
ver**.

```
git switch -c <autor>/<o-que-mudou>
git push -u origin <autor>/<o-que-mudou>
gh pr create
```

O Pull Request é o ponto de entrega: quem é dono revisa e faz o merge, e **o
merge é que publica**.

## O DNS deste subdomínio

A zona fica no registro.br e o apontamento é por **CNAME no nome `app`**, com o
valor que o painel da Vercel mostrar para este projeto.

⚠ **O nameserver nunca é apontado para a Vercel.** O DNSSEC está ligado no
`marketingapex.com.br` e a Vercel não assina zona: trocar nameserver faz o
domínio inteiro parar de resolver — site e e-mail, para todo mundo.

## O que nunca entra em commit

`.env` e variantes, `node_modules/`, `.vercel/` — já cobertos pelo
`.gitignore`. Chave de API, token e senha não entram neste repositório.

`.claude/settings.local.json` é pessoal de cada máquina e fica de fora.
