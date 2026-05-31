# Security Policy

## Escopo

Este repositorio contem documentacao, governanca e requisitos da organizacao
OpenEduOps. Ele ainda nao contem o codigo do aplicativo Radar Escola.

## Reportando vulnerabilidades

Se voce encontrar um problema de seguranca, abra uma issue apenas se o conteudo
nao expuser dados sensiveis, credenciais, chaves ou caminhos de exploracao
detalhados.

Para problemas sensiveis, entre em contato com os maintainers antes de publicar
detalhes tecnicos.

## Guardrails atuais

- Workflows usam permissoes minimas por padrao.
- Forks nao devem executar codigo em `pull_request_target`.
- O futuro app deve armazenar senhas apenas como hash.
- O futuro app deve funcionar localmente sem depender de servicos privados.

## Fora de escopo atual

Como ainda nao existe codigo do app, este repositorio nao publica releases,
binarios, instaladores ou pacotes executaveis.
