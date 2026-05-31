# Escopo da V0

Este documento define a linha de corte da V0 do primeiro produto, usando
`Radar Escola` como nome publico candidato atual.

O fluxo ponta a ponta esta descrito em `FLUXO_E2E_V0.md`.

A V0 deve entregar uma experiencia util, instalavel/local e pequena o suficiente
para ser implementada, testada e validada sem transformar a primeira versao em um
produto amplo demais.

## Objetivo da V0

Permitir que uma escola registre necessidades operacionais, acompanhe o que esta
em andamento, mantenha historico basico e exporte copias CSV de seguranca dos
dados.

Frase-guia:

> Instalar, abrir, registrar uma necessidade, acompanhar andamento, marcar como
> resolvido e preservar historico.

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
- exportar necessidades em CSV;
- exportar equipamentos em CSV;
- executar testes automatizados dos fluxos criticos.

Qualquer funcionalidade fora dessa lista deve ser considerada fora da V0, salvo
decisao explicita posterior.

## Entra na V0

### Primeiro uso

- Nome da escola.
- Nome da direcao ou pessoa responsavel principal.
- Usuario de acesso.
- Senha.
- Alerta sobre a importancia de nao perder usuario, senha e salvaguarda.
- Geracao de token simples de recuperacao.
- Cadastro de pergunta secreta e resposta secreta.

### Acesso

- Login com usuario e senha.
- Recuperacao local de acesso com usuario ou nome, token simples e pergunta
  secreta, se implementada no primeiro ciclo.
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

### Exportacao de seguranca

- Exportacao manual em CSV.
- A exportacao de seguranca deve ser responsabilidade do perfil direcao ou da
  pessoa responsavel principal.
- Exportacao de necessidades.
- Exportacao de equipamentos.
- Orientacao explicita para salvar a exportacao em pendrive, pasta de rede ou
  outra maquina.
- O CSV deve servir como copia de seguranca e tambem como formato simples de
  leitura fora do aplicativo.

### Testes

- Testes unitarios para regras de necessidade e validacoes.
- Testes de persistencia para SQLite.
- Testes de exportacao CSV.
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
- exporta necessidades em CSV;
- exporta equipamentos em CSV;
- possui testes automatizados dos fluxos criticos;
- documenta como executar, testar e validar a V0.

## Regra de protecao de escopo

Se uma nova ideia nao ajudar diretamente a completar o fluxo:

> registrar -> acompanhar -> marcar envolvidos -> atualizar -> marcar como
> resolvido -> preservar historico

ela deve ficar fora da V0.

Ideias boas podem virar backlog futuro, mas nao devem entrar no primeiro corte
sem uma razao forte de utilidade imediata.
