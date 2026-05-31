# Fluxo E2E da V0

Este documento consolida o fluxo ponta a ponta da V0 do Radar Escola.

O objetivo e responder uma pergunta simples:

> O MVP entrega um ciclo util completo para uma escola?

## Resposta curta

Sim, desde que a V0 entregue um ciclo operacional completo:

> configurar -> entrar -> registrar necessidade -> acompanhar no radar ->
> atualizar andamento -> resolver -> consultar historico -> fazer backup.

Se qualquer etapa desse ciclo faltar, a V0 fica incompleta.

## Usuario principal da V0

Pessoa responsavel por organizar necessidades operacionais da escola.

Exemplos:

- secretaria;
- coordenacao;
- responsavel por laboratorio;
- pessoa da equipe tecnica;
- direcao em escola pequena.

Essa pessoa nao deve precisar entender banco de dados, servidor, Docker,
terminal, rede, cloud ou infraestrutura.

## Fluxo E2E principal

### 1. Primeiro uso

A pessoa abre o Radar Escola pela primeira vez.

O sistema pede apenas o essencial:

- nome da escola;
- nome da pessoa responsavel;
- usuario;
- senha;
- salvaguarda local de acesso.

Resultado esperado:

- a escola esta configurada;
- existe um primeiro usuario local;
- existe uma forma de salvaguarda contra esquecimento de acesso;
- o usuario chega ao Radar de Necessidades.

### 2. Registrar uma necessidade

A pessoa percebe algo que precisa ser resolvido.

Exemplo:

> O projetor da sala 8 nao liga.

Ela registra:

- o que precisa ser resolvido;
- onde aconteceu;
- descricao em linguagem simples;
- prioridade;
- envolvidos;
- equipamento relacionado, se existir.

Resultado esperado:

- a necessidade foi registrada;
- ela aparece no Radar de Necessidades;
- ela nao depende mais de memoria, WhatsApp, papel ou conversa informal.

### 3. Acompanhar no Radar de Necessidades

Ao entrar no sistema, a pessoa ve:

- necessidades em andamento;
- necessidades paradas;
- resolvidas recentemente.

Resultado esperado:

- o que precisa de atencao fica visivel;
- necessidades paradas nao desaparecem;
- a escola consegue enxergar o que ainda precisa ser cuidado.

### 4. Atualizar andamento

Uma pessoa envolvida acessa o computador onde o aplicativo esta instalado e
entra com seu usuario e senha.

Ela abre a necessidade e registra uma atualizacao.

Exemplo:

> Testamos outro cabo HDMI e o problema continua.

Tambem pode alterar o status:

- nova;
- em analise;
- em execucao;
- aguardando material;
- aguardando autorizacao;
- pausada.

Resultado esperado:

- o andamento fica documentado;
- outras pessoas podem consultar a situacao no Radar Escola;
- a necessidade continua viva ate ser resolvida.

### 5. Registrar resolucao

Quando o problema for resolvido, alguem registra:

- o que foi feito;
- quem resolveu;
- quando foi resolvido;
- se precisa acompanhar depois.

Exemplo:

> O cabo HDMI foi substituido e o projetor voltou a funcionar.

Resultado esperado:

- a necessidade sai do fluxo ativo;
- a solucao fica preservada;
- a escola cria memoria operacional.

### 6. Consultar historico

Depois, a escola pode consultar necessidades resolvidas.

Isso ajuda a responder perguntas como:

- isso ja aconteceu antes?
- quem resolveu?
- qual foi a solucao?
- esse equipamento tem problema recorrente?

Resultado esperado:

- a escola aprende com a propria rotina;
- problemas recorrentes ficam mais faceis de perceber;
- trocas de equipe nao apagam o historico.

### 7. Fazer backup

A pessoa responsavel faz backup manual dos dados.

Resultado esperado:

- os dados locais podem ser preservados;
- a escola reduz risco de perda por problema no computador;
- existe um caminho simples para restauracao.

## Fluxo minimo de valor

O menor fluxo que ainda entrega valor real e:

> registrar necessidade -> ver no radar -> atualizar andamento -> registrar
> resolucao -> consultar historico.

Backup nao e parte da dor diaria, mas e obrigatorio para a V0 porque o produto e
local e os dados precisam ser protegidos.

## O que torna o MVP util

A V0 e util se permitir que a escola deixe de depender de:

- memoria das pessoas;
- mensagens soltas;
- papel;
- conversas de corredor;
- planilhas improvisadas;
- historico informal.

E passe a ter:

- um lugar unico para registrar necessidades;
- visao do que esta em andamento;
- visao do que esta parado;
- registro de atualizacoes;
- resolucao documentada;
- historico consultavel;
- backup local.

## O que nao faz parte do fluxo E2E da V0

- notificacao por e-mail;
- WhatsApp;
- app mobile;
- acesso remoto;
- sincronizacao entre computadores;
- dashboards;
- relatorios avancados;
- anexos;
- fotos;
- permissao complexa;
- dados de estudantes;
- nuvem.

Essas ideias podem existir no futuro, mas nao sao necessarias para provar o ciclo
principal da V0.

## Criterio de corte

Antes de adicionar qualquer nova funcionalidade, a pergunta deve ser:

> Isso melhora diretamente o ciclo registrar, acompanhar, atualizar, resolver,
> consultar historico e fazer backup?

Se a resposta for nao, a funcionalidade deve ficar fora da V0.

## Teste narrativo da V0

A V0 deve ser validada com uma historia simples:

1. Maria instala e abre o Radar Escola.
2. Maria cria o primeiro acesso da escola.
3. Maria registra que o projetor da sala 8 nao liga.
4. A necessidade aparece no Radar de Necessidades.
5. Joao acessa o mesmo computador e registra uma atualizacao.
6. A necessidade aparece como em andamento.
7. Depois de resolver, Joao registra a solucao.
8. Maria consulta o historico e ve o que foi feito.
9. Maria faz backup dos dados.

Se essa historia funcionar de ponta a ponta, a V0 tem um MVP util.
