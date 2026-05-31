# Visao Prototipal v0

Este documento registra uma primeira visao prototipal em baixa fidelidade para o
primeiro produto do OpenEduOps.

O objetivo ainda nao e definir layout visual, componentes finais ou tecnologia de
interface. O objetivo e validar fluxo, linguagem, prioridade das acoes e
experiencia esperada para uma pessoa nao tecnica usando o produto em uma escola.

Esta visao deve ser lida junto com `CONTEXTO_INICIAL.md` e `GUARDRAILS_V0.md`.

## Produto

Nome candidato do produto:

> Radar Escola

Tela principal/conceito operacional:

> Radar de Necessidades

Frase de valor:

> Veja o que sua escola precisa resolver.

Principio do produto:

> Acao conjunta para cuidar das necessidades da escola.

## Primeira abertura

```text
+------------------------------------------------------+
| Radar Escola                                        |
| Veja o que sua escola precisa resolver.              |
+------------------------------------------------------+
|                                                      |
| Bem-vinda(o). Vamos preparar o uso nesta escola.     |
|                                                      |
| Nome da escola                                      |
| [ Escola Municipal __________________________ ]      |
|                                                      |
| Seu nome                                            |
| [ Maria Silva ________________________________ ]     |
|                                                      |
| E-mail para receber avisos                          |
| [ maria@escola.gov.br _______________________ ]      |
|                                                      |
| E-mail pessoal para recuperacao de senha             |
| [ maria.pessoal@email.com ___________________ ]      |
|                                                      |
| Senha de acesso                                     |
| [ __________________________________________ ]       |
|                                                      |
| [ Comecar ]                                         |
|                                                      |
+------------------------------------------------------+
```

## Radar de Necessidades

```text
+------------------------------------------------------+
| Radar Escola                         [Backup] [Ajuda]|
| Veja o que sua escola precisa resolver.              |
+------------------------------------------------------+
|                                                      |
| [ Tenho algo para resolver ]                         |
| [ Preciso pedir ajuda ]                              |
|                                                      |
| Em andamento                                        |
| ---------------------------------------------------- |
| #12 Projetor da sala 8 nao liga       Urgente        |
|     Sala 8 | Ana | Em execucao                       |
|                                                      |
| #11 Impressora da secretaria falhando  Aguardando    |
|     Secretaria | Marta | Aguardando material         |
|                                                      |
| Paradas                                              |
| ---------------------------------------------------- |
| #08 Computador 12 sem internet        3 dias parado  |
|     Laboratorio | Joao | Em analise                  |
|                                                      |
| Resolvidas recentemente                              |
| ---------------------------------------------------- |
| #07 Troca de mouse no laboratorio     Resolvido      |
|                                                      |
+------------------------------------------------------+
```

## Registrar Necessidade

```text
+------------------------------------------------------+
| Registrar necessidade                         [Voltar]|
+------------------------------------------------------+
|                                                      |
| O que precisa ser resolvido?                         |
| [ Projetor da sala 8 nao liga ________________ ]     |
|                                                      |
| Onde aconteceu?                                     |
| [ Sala 8 _____________________________________ ]     |
|                                                      |
| Descreva com suas palavras                           |
| [ Ontem o projetor nao ligou durante a aula...  ]    |
| [ ____________________________________________ ]     |
|                                                      |
| Isso atrapalha aula ou atendimento?                  |
| ( ) Sim, agora                                      |
| ( ) Sim, mas pode aguardar                           |
| ( ) Nao tenho certeza                                |
|                                                      |
| Tem equipamento envolvido?                           |
| [ Selecionar equipamento ] [ Cadastrar novo ]        |
|                                                      |
| Quem precisa acompanhar?                             |
| [ Ana, Coordenacao, Tecnico __________________ ]      |
|                                                      |
| [ Registrar necessidade ]                            |
|                                                      |
+------------------------------------------------------+
```

## Detalhe da Necessidade

```text
+------------------------------------------------------+
| Necessidade #12                              [Voltar] |
| Projetor da sala 8 nao liga                          |
+------------------------------------------------------+
| Status: Em execucao              Prioridade: Urgente |
| Local: Sala 8                    Criado por: Ana     |
| Envolvidos: Ana, Coordenacao, Joao Tecnico           |
+------------------------------------------------------+
|                                                      |
| Plano de acao                                        |
| [x] Verificar tomada e cabo                          |
| [ ] Testar outro cabo HDMI                           |
| [ ] Avaliar troca da lampada                         |
|                                                      |
| Atualizacoes                                         |
| ---------------------------------------------------- |
| Joao: Verifiquei a tomada. Esta funcionando.         |
| Ana: A aula de amanha tambem depende do projetor.    |
| Sistema: Coordenacao foi notificada por e-mail.      |
|                                                      |
| Escrever atualizacao                                 |
| [ ____________________________________________ ]     |
| [ Avisar envolvidos ]                                |
|                                                      |
| [ Atualizar status ] [ Registrar como resolvido ]    |
|                                                      |
+------------------------------------------------------+
```

## Registrar Solucao

```text
+------------------------------------------------------+
| Registrar solucao da necessidade #12          [Voltar]|
+------------------------------------------------------+
|                                                      |
| O que foi feito?                                    |
| [ O cabo HDMI foi substituido e o projetor voltou ]  |
| [ a funcionar normalmente. _____________________ ]   |
|                                                      |
| Quem resolveu?                                      |
| [ Joao Tecnico _______________________________ ]     |
|                                                      |
| Precisa acompanhar depois?                           |
| ( ) Nao                                             |
| ( ) Sim, lembrar em [ 7 ] dias                       |
|                                                      |
| Avisar envolvidos por e-mail?                        |
| [x] Sim                                             |
|                                                      |
| [ Registrar como resolvido ]                         |
|                                                      |
+------------------------------------------------------+
```

## Equipamentos

```text
+------------------------------------------------------+
| Equipamentos                                 [Voltar] |
+------------------------------------------------------+
| [ Cadastrar equipamento ]                            |
|                                                      |
| Buscar                                               |
| [ projetor, sala, patrimonio... ______________ ]     |
|                                                      |
| ---------------------------------------------------- |
| Projetor Epson X100                                  |
| Sala 8 | Patrimonio 12345 | Com problema             |
| Necessidades vinculadas: #12                         |
|                                                      |
| Computador 12                                        |
| Laboratorio | Patrimonio 99321 | Em analise          |
| Necessidades vinculadas: #08                         |
|                                                      |
+------------------------------------------------------+
```

## Entrar no Sistema

```text
+------------------------------------------------------+
| Radar Escola                                        |
| Veja o que sua escola precisa resolver.              |
+------------------------------------------------------+
|                                                      |
| E-mail                                               |
| [ maria@escola.gov.br _______________________ ]      |
|                                                      |
| Senha                                                |
| [ __________________________________________ ]       |
|                                                      |
| [ Entrar ]                                           |
|                                                      |
| Esqueci minha senha                                  |
|                                                      |
+------------------------------------------------------+
```

## Recuperar Senha

```text
+------------------------------------------------------+
| Recuperar senha                              [Voltar] |
+------------------------------------------------------+
|                                                      |
| Informe seu e-mail pessoal de recuperacao,            |
| se essa opcao tiver sido configurada.                 |
|                                                      |
| E-mail pessoal                                       |
| [ maria.pessoal@email.com ___________________ ]      |
|                                                      |
| O sistema tentara enviar instrucoes para recuperar    |
| o acesso. Tambem pode haver uma alternativa local.    |
|                                                      |
| [ Enviar instrucoes ]                                |
|                                                      |
+------------------------------------------------------+
```

## Cadastrar Equipamento

```text
+------------------------------------------------------+
| Cadastrar equipamento                         [Voltar]|
+------------------------------------------------------+
|                                                      |
| Nome do equipamento                                  |
| [ Projetor Epson X100 _______________________ ]      |
|                                                      |
| Onde fica?                                           |
| [ Sala 8 _____________________________________ ]      |
|                                                      |
| Patrimonio ou identificacao                          |
| [ 12345 ______________________________________ ]      |
|                                                      |
| Estado atual                                         |
| ( ) Funcionando                                      |
| ( ) Com problema                                     |
| ( ) Em manutencao                                    |
| ( ) Fora de uso                                      |
|                                                      |
| Observacoes                                          |
| [ Usado principalmente no turno da manha... ____ ]   |
|                                                      |
| [ Salvar equipamento ]                               |
|                                                      |
+------------------------------------------------------+
```

## Envolver Pessoas

```text
+------------------------------------------------------+
| Envolver pessoas na necessidade #12           [Voltar]|
+------------------------------------------------------+
| Projetor da sala 8 nao liga                          |
+------------------------------------------------------+
|                                                      |
| Quem precisa acompanhar?                             |
| [ Buscar pessoa ou setor _____________________ ]     |
|                                                      |
| Sugestoes                                            |
| [ ] Coordenacao                                      |
| [ ] Direcao                                          |
| [ ] Equipe tecnica                                   |
| [ ] Secretaria                                       |
|                                                      |
| Envolvidos atuais                                    |
| ---------------------------------------------------- |
| Ana                     Solicitante                  |
| Joao Tecnico            Responsavel                  |
| Coordenacao             Acompanhamento               |
|                                                      |
| Avisar novos envolvidos por e-mail?                  |
| [x] Sim                                             |
|                                                      |
| [ Salvar envolvidos ]                                |
|                                                      |
+------------------------------------------------------+
```

## Criar Plano de Acao

```text
+------------------------------------------------------+
| Plano de acao da necessidade #12              [Voltar]|
+------------------------------------------------------+
| Projetor da sala 8 nao liga                          |
+------------------------------------------------------+
|                                                      |
| Proximos passos                                      |
| ---------------------------------------------------- |
| [x] Verificar tomada e cabo                          |
|     Responsavel: Joao Tecnico                        |
|                                                      |
| [ ] Testar outro cabo HDMI                           |
|     Responsavel: Joao Tecnico                        |
|                                                      |
| [ ] Avaliar troca da lampada                         |
|     Responsavel: Coordenacao                         |
|                                                      |
| Adicionar passo                                      |
| [ ____________________________________________ ]     |
| Responsavel                                          |
| [ Selecionar pessoa ou setor _________________ ]     |
|                                                      |
| [ Adicionar passo ]                                  |
| [ Salvar plano ]                                     |
|                                                      |
+------------------------------------------------------+
```

## Atualizar Andamento

```text
+------------------------------------------------------+
| Atualizar andamento da necessidade #12        [Voltar]|
+------------------------------------------------------+
| Projetor da sala 8 nao liga                          |
+------------------------------------------------------+
|                                                      |
| Novo status                                          |
| ( ) Nova                                             |
| ( ) Em analise                                       |
| ( ) Em execucao                                      |
| ( ) Aguardando material                              |
| ( ) Aguardando autorizacao                           |
| ( ) Pausada                                          |
|                                                      |
| O que mudou?                                         |
| [ Testamos outro cabo HDMI e o problema continua. ]  |
| [ ____________________________________________ ]     |
|                                                      |
| Avisar envolvidos por e-mail?                        |
| [x] Sim                                             |
|                                                      |
| [ Salvar atualizacao ]                               |
|                                                      |
+------------------------------------------------------+
```

## Ver Necessidades Paradas

```text
+------------------------------------------------------+
| Necessidades paradas                         [Voltar] |
+------------------------------------------------------+
| Essas necessidades precisam voltar para o radar.      |
+------------------------------------------------------+
|                                                      |
| #08 Computador 12 sem internet        3 dias parado  |
| Laboratorio | Joao | Em analise                      |
| [ Ver caso ] [ Avisar envolvidos ]                   |
|                                                      |
| #05 Impressora sem toner              5 dias parada  |
| Secretaria | Marta | Aguardando material             |
| [ Ver caso ] [ Avisar envolvidos ]                   |
|                                                      |
| #03 Porta da biblioteca emperrada     8 dias parada  |
| Biblioteca | Coordenacao | Aguardando autorizacao     |
| [ Ver caso ] [ Avisar envolvidos ]                   |
|                                                      |
+------------------------------------------------------+
```

## Historico

```text
+------------------------------------------------------+
| Historico                                    [Voltar] |
+------------------------------------------------------+
| Buscar no historico                                  |
| [ projetor, sala, pessoa, equipamento... _____ ]     |
|                                                      |
| Filtros                                              |
| [Resolvidas] [Canceladas] [Todas]                    |
|                                                      |
| ---------------------------------------------------- |
| #07 Troca de mouse no laboratorio     Resolvido      |
| Resolvido por Joao Tecnico em 12/05/2026             |
|                                                      |
| #04 Cabo de rede rompido na secretaria Resolvido     |
| Resolvido por Equipe tecnica em 08/05/2026           |
|                                                      |
| #02 Projetor sem imagem na sala 3     Resolvido      |
| Resolvido por Marta em 01/05/2026                    |
|                                                      |
+------------------------------------------------------+
```

## Backup e Restauracao

```text
+------------------------------------------------------+
| Backup e restauracao                         [Voltar] |
+------------------------------------------------------+
| Seus dados ficam neste computador.                    |
| Faca backup em uma pasta segura ou pendrive.          |
+------------------------------------------------------+
|                                                      |
| Ultimo backup                                        |
| 20/05/2026 as 14:32                                  |
|                                                      |
| [ Fazer backup agora ]                               |
| [ Escolher pasta de backup ]                         |
|                                                      |
| Restaurar dados                                      |
| [ Selecionar arquivo de backup ]                     |
|                                                      |
| Exportar                                             |
| [ Exportar necessidades em CSV ]                     |
| [ Exportar equipamentos em CSV ]                     |
|                                                      |
+------------------------------------------------------+
```

## Configurar Avisos

```text
+------------------------------------------------------+
| Configurar avisos                            [Voltar] |
+------------------------------------------------------+
|                                                      |
| E-mail usado para avisos da escola                   |
| [ maria@escola.gov.br _______________________ ]      |
|                                                      |
| E-mail pessoal para recuperacao de senha             |
| [ maria.pessoal@email.com ___________________ ]      |
|                                                      |
| Avisar envolvidos quando:                            |
| [x] Uma necessidade for registrada                   |
| [x] Alguem comentar ou atualizar andamento           |
| [x] Uma necessidade ficar parada por muito tempo     |
| [x] Uma necessidade for resolvida                    |
|                                                      |
| Frequencia de resumo                                 |
| ( ) Nunca                                            |
| ( ) Diario                                           |
| ( ) Semanal                                          |
|                                                      |
| [ Salvar configuracoes ]                             |
|                                                      |
+------------------------------------------------------+
```

## Perguntas em Aberto

- A primeira tela deve iniciar pelo cadastro da escola ou pelo radar com
  configuracao guiada?
- O cadastro inicial deve separar e-mail de avisos institucionais e e-mail
  pessoal para recuperacao de senha?
- O botao principal deve ser "Tenho algo para resolver" ou "Registrar
  necessidade"?
- "Preciso pedir ajuda" deve ser uma acao separada ou apenas outra porta para
  registrar uma necessidade?
- A tela principal deve priorizar "Em andamento" e "Paradas" antes de qualquer
  grafico?
- "Avisar envolvidos" deve aparecer como botao explicito em atualizacoes?

## Hipotese Principal

O coracao da experiencia deve ser o Radar de Necessidades.

Essa tela deve tornar muito visivel o que esta em andamento, o que esta parado,
quem esta envolvido e o que precisa de atencao para nao esfriar ate ser
resolvido.
