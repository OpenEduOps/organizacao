# CI do OpenEduOps

Este documento explica a CI inicial do repositorio `OpenEduOps/organizacao`.

## Escopo atual

Este repositorio e de organizacao, governanca e documentacao. Ele ainda nao
contem o codigo do aplicativo Radar Escola.

Por isso, a CI atual valida:

- qualidade basica de Markdown;
- presenca dos documentos centrais;
- links internos;
- higiene do repositorio;
- typecheck e build do scaffold React/TypeScript;
- postura minima de permissoes dos workflows.

## Check protegido

O check que deve proteger `main` e:

```text
All CI checks
```

Esse check agrega os jobs internos da CI. A regra de branch protection deve usar
apenas esse nome para nao depender de nomes de matrix ou jobs auxiliares.

## Workflows

- `.github/workflows/ci.yml`: valida documentacao e higiene do repositorio.
  Tambem valida `npm ci`, `npm run typecheck` e `npm run build` para o scaffold
  frontend.
- `.github/workflows/security.yml`: valida postura de seguranca e dependency
  review em pull requests.
- `.github/workflows/thank-contributor.yml`: envia mensagem de boas-vindas para
  novas issues e pull requests.
- `.github/workflows/desktop-release.yml`: contrato futuro da esteira de
  instalador Windows. Hoje ele depende do scaffold do app Radar Escola para
  conseguir gerar artefatos reais. Em execucao manual, informa pendencias sem
  publicar artefatos; em tag `v*`, falha se o app ainda nao existir.

## Comandos locais equivalentes

Quando Node estiver disponivel:

```bash
npx --yes markdownlint-cli2@0.16.0 "**/*.md"
```

Os checks de consistencia documental e higiene estao descritos no proprio
workflow `ci.yml`.

## Futuro app Radar Escola

Quando o repositorio do app existir, a CI devera evoluir para validar:

- lint, typecheck, testes e build do frontend;
- checks Rust/Tauri;
- testes de persistencia SQLite;
- regras criticas de seguranca local;
- smoke test do fluxo minimo.

O scaffold minimo do app ja existe para validar a casca desktop e o pipeline de
release sem fingir funcionalidade de MVP.

## Esteira Desktop Futura

A esteira alvo de download, instalacao e execucao do app esta documentada em
[`docs/desktop-release.md`](desktop-release.md).

Ela devera gerar artefato baixavel, checksum SHA-256 e release versionada quando
o app desktop existir.
