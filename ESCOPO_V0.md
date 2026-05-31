# Escopo da V0

Este documento define a linha de corte da V0 do primeiro produto, usando
`Radar Escola` como nome publico candidato atual.

O fluxo ponta a ponta esta descrito em `FLUXO_E2E_V0.md`.

A V0 deve entregar uma experiencia util, instalavel/local e pequena o suficiente
para ser implementada, testada e validada sem transformar a primeira versao em um
produto amplo demais.

## Objetivo da V0

Permitir que uma escola registre necessidades operacionais, acompanhe o que esta
em andamento, mantenha historico basico e faca backup local dos dados.

Frase-guia:

> Instalar, abrir, registrar uma necessidade, acompanhar andamento, resolver e
> preservar historico.

## Linha de corte

A V0 termina quando o Radar Escola permite:

- configurar o primeiro acesso local;
- entrar com usuario e senha;
- registrar uma necessidade;
- listar necessidades no Radar de Necessidades;
- visualizar detalhe de uma necessidade;
- atualizar andamento;
- marcar envolvidos como texto simples ou selecao basica;
- registrar resolucao;
- consultar historico de necessidades resolvidas;
- cadastrar equipamento basico;
- vincular uma necessidade a um equipamento;
- fazer backup manual;
- restaurar backup com confirmacao;
- executar testes automatizados dos fluxos criticos.

Qualquer funcionalidade fora dessa lista deve ser considerada fora da V0, salvo
decisao explicita posterior.

## Entra na V0

### Primeiro uso

- Nome da escola.
- Nome da pessoa responsavel.
- Usuario de acesso.
- Senha.
- Geracao de salvaguarda local de acesso.

### Acesso

- Login com usuario e senha.
- Recuperacao local de acesso por salvaguarda, se implementada no primeiro
  ciclo.
- Sem e-mail pessoal para recuperacao.
- Sem dependencia de internet.

### Necessidades

- Criar necessidade.
- Campos minimos:
  - titulo;
  - descricao;
  - local;
  - prioridade simples;
  - status;
  - envolvidos;
  - equipamento vinculado opcional.
- Listar necessidades em andamento.
- Listar necessidades paradas.
- Listar resolvidas recentemente.
- Visualizar detalhe.
- Registrar atualizacao.
- Alterar status.
- Registrar resolucao.

### Envolvidos

- Envolvidos podem ser texto simples, lista local ou cadastro basico.
- Cada envolvido deve poder consultar o aplicativo no computador instalado, se
  tiver usuario e senha.
- Sem notificacao automatica.

### Equipamentos

- Cadastro basico de equipamento:
  - nome;
  - local;
  - patrimonio ou identificacao;
  - estado atual;
  - observacoes.
- Vinculo entre necessidade e equipamento.
- Listagem simples de equipamentos.

### Historico

- Necessidades resolvidas devem continuar consultaveis.
- Historico deve mostrar atualizacoes relevantes e resolucao.
- Busca simples pode existir se for barata, mas nao deve bloquear a V0.

### Backup e restauracao

- Backup manual.
- Restauracao manual.
- Confirmacao antes de restaurar.
- Validacao basica do arquivo de backup.
- Preferencialmente criar backup preventivo antes de restaurar.

### Testes

- Testes unitarios para regras de necessidade e validacoes.
- Testes de persistencia para SQLite.
- Testes de backup/restauracao.
- Testes de interface dos fluxos principais.
- Testes de integracao desktop quando o empacotamento Tauri estiver disponivel.

## Fica fora da V0

- Nomes, e-mails, documentos, matriculas ou dados pessoais de estudantes.
- E-mail automatico.
- WhatsApp.
- Push notification.
- Mensageria externa.
- Recuperacao por e-mail pessoal.
- Perfis e permissoes complexas.
- Multiunidade.
- Sincronizacao entre computadores.
- Servidor em rede local como requisito.
- Aplicativo mobile.
- Dashboard analitico.
- Graficos.
- Relatorios avancados.
- Importacao em massa.
- Anexos.
- Fotos.
- Comentarios ricos.
- Editor formatado.
- SLA.
- Calendario.
- Reserva de salas.
- Controle completo de patrimonio.
- Base de conhecimento.
- Telemetria.
- Nuvem.
- IA.

## Pode aparecer apenas como estrutura futura

Algumas decisoes podem ser preparadas de forma leve, sem virar funcionalidade da
V0:

- organizacao do codigo por dominio;
- campos que facilitem evolucao para rede local;
- separacao entre interface e persistencia;
- migracoes de banco;
- testes que reduzam risco de mudanca futura;
- nomenclatura que permita crescimento para EduInventory, EduLab, EduRooms e
  EduContinuity.

Preparar nao significa implementar a funcionalidade agora.

## Criterios de aceite da V0

A V0 pode ser considerada entregue quando:

- roda localmente em ambiente de desenvolvimento;
- possui caminho claro para empacotamento desktop;
- permite primeiro uso local;
- permite login;
- cria necessidade;
- mostra a necessidade no Radar de Necessidades;
- atualiza andamento;
- registra resolucao;
- preserva historico;
- cadastra equipamento basico;
- vincula equipamento a necessidade;
- faz backup manual;
- restaura backup com confirmacao;
- possui testes automatizados dos fluxos criticos;
- documenta como executar, testar e validar a V0.

## Regra de protecao de escopo

Se uma nova ideia nao ajudar diretamente a completar o fluxo:

> registrar -> acompanhar -> atualizar -> resolver -> preservar historico ->
> fazer backup

ela deve ficar fora da V0.

Ideias boas podem virar backlog futuro, mas nao devem entrar no primeiro corte
sem uma razao forte de utilidade imediata.
