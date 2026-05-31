# Visao Prototipal Inicial

Este documento registra uma primeira visao prototipal em baixa fidelidade para o
primeiro produto do OpenEduOps.

O objetivo ainda nao e definir layout visual, componentes finais ou tecnologia de
interface. O objetivo e validar fluxo, linguagem, prioridade das acoes e
experiencia esperada para uma pessoa nao tecnica usando o produto em uma escola.

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

## Perguntas em Aberto

- A primeira tela deve iniciar pelo cadastro da escola ou pelo radar com
  configuracao guiada?
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
