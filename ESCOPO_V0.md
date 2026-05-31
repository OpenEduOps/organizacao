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
- cadastrar pessoas/usuarios locais com cargo ou funcao;
- entrar com usuario e senha;
- registrar uma necessidade;
- listar necessidades no Radar de Necessidades;
- visualizar detalhe de uma necessidade;
- atualizar andamento;
- marcar envolvidos a partir de pessoas/usuarios cadastrados;
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
- Cadastro de frase de recuperacao e resposta.

### Acesso

- Login com usuario e senha.
- Recuperacao local de acesso com usuario ou nome e salvaguarda local, usando
  token simples ou frase de recuperacao.
- Sem e-mail pessoal para recuperacao.
- Sem dependencia de internet.

### Pessoas e usuarios

- A V0 deve ter cadastro local de pessoas/usuarios desde o inicio.
- Campos minimos:
  - nome;
  - usuario;
  - cargo ou funcao;
  - senha inicial;
  - status de primeiro acesso.
- Cargo ou funcao deve usar lista simples cadastravel localmente.
- Se o cargo ou funcao ainda nao existir durante o cadastro de pessoa, a V0 deve
  permitir criar essa opcao no proprio fluxo e continuar o cadastro.
- Na V0, pessoas cadastradas podem ver necessidades, historico, envolvidos e
  andamentos.
- Acoes sensiveis devem ficar restritas a direcao ou pessoa responsavel
  principal, incluindo exportacao de seguranca e gestao de acessos/senhas.
- A direcao ou pessoa responsavel principal pode delegar o cadastro de novos
  usuarios para pessoas ou cargos/funcoes especificos, preferencialmente
  coordenadores ou funcoes imediatamente abaixo da direcao.
- Alem da direcao, no maximo duas pessoas podem receber essa atribuicao na V0.
- Essa delegacao deve permitir cadastrar pessoas/usuarios, mas nao deve liberar
  automaticamente exportacao de seguranca nem recuperacao administrativa da
  propria direcao.
- Pessoas cadastradas podem ser marcadas como envolvidas em necessidades.
- A senha inicial padrao para pessoas cadastradas pode ser `123456`, mas apenas
  para primeiro acesso.
- No primeiro login da pessoa cadastrada, a troca de senha deve ser obrigatoria
  antes de usar o sistema.
- Ao trocar a senha inicial, a pessoa deve definir sua propria salvaguarda local
  de recuperacao.
- A salvaguarda individual deve permitir recuperacao por token simples ou por
  frase de recuperacao.
- O token de recuperacao deve ser exibido no momento de configuracao da
  salvaguarda e nao deve poder ser regenerado.
- O primeiro acesso da pessoa cadastrada deve ser privado. A direcao ou pessoa
  responsavel principal nao deve ver a nova senha, o token, a frase de
  recuperacao nem a resposta.
- A interface deve explicitar que a pessoa deve fazer esse procedimento
  preferencialmente sem a presenca da direcao ou com distancia segura da tela.
- Se uma pessoa cadastrada perder senha e salvaguarda, a direcao ou pessoa
  responsavel principal pode redefinir a senha dessa pessoa para `123456`.
- Apos redefinicao administrativa, o proximo login deve obrigar nova troca de
  senha. Essa redefinicao nao deve gerar novo token.

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

- Envolvidos devem ser pessoas/usuarios cadastrados.
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
- permite cadastrar pessoa/usuario local com cargo ou funcao;
- obriga troca da senha inicial padrao no primeiro acesso da pessoa cadastrada;
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
