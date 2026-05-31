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
- `.github/workflows/security.yml`: valida postura de seguranca e dependency
  review em pull requests.
- `.github/workflows/thank-contributor.yml`: envia mensagem de boas-vindas para
  novas issues e pull requests.

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

Esses comandos nao devem ser adicionados a este repositorio enquanto o scaffold
do app nao existir.
