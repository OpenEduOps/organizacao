# Guardrails da V0

Este documento registra guardrails iniciais para a V0 do primeiro produto do
OpenEduOps.

Ele deve ser lido junto com:

- `CONTEXTO_INICIAL.md`;
- `VISAO_PROTOTIPAL_V0.md`;
- `ESCOPO_V0.md`;
- `FLUXO_E2E_V0.md`.

O objetivo e proteger a experiencia do usuario final, reduzir riscos de escopo e
evitar que decisoes tecnicas enfraquecam a proposta inicial.

## Identidade e linguagem

- O nome publico candidato atual do produto e `Radar Escola`.
- `EduDesk` deve ser tratado apenas como nome anterior/codinome historico, ate
  decisao contraria.
- A tela principal/conceito operacional e `Radar de Necessidades`.
- A frase de valor e: "Veja o que sua escola precisa resolver."
- O principio do produto e: "Acao conjunta para cuidar das necessidades da
  escola."
- A unidade central do produto e `necessidade`, nao ticket ou chamado.
- A interface deve priorizar linguagem de intencao do usuario, como "Tenho algo
  para resolver" e "Quero ver o que esta parado".

## Experiencia do usuario final

- A V0 deve priorizar Windows desktop local.
- O fluxo principal deve ser: baixar, instalar, abrir e registrar a primeira
  necessidade em poucos minutos.
- O usuario final nao deve precisar entender Tauri, Rust, React, TypeScript,
  SQLite, banco de dados, servidor local, Docker ou infraestrutura.
- Docker nao deve fazer parte da experiencia do usuario final.
- O produto deve continuar util mesmo sem internet.
- E-mail, WhatsApp, mensageria e notificacoes automaticas nao devem fazer parte
  da V0.

## Escopo da V0

A V0 deve privilegiar o menor conjunto funcional que demonstre valor real:

- primeira abertura;
- Radar de Necessidades;
- registro de necessidade;
- detalhe da necessidade;
- envolvidos;
- andamento;
- registro de resolucao;
- historico;
- exportacao CSV de seguranca;
- equipamentos basicos quando necessarios para vincular uma necessidade.

Funcionalidades que devem ser tratadas com cuidado para nao inflar a V0:

- recuperacao de senha por e-mail;
- notificacoes automaticas;
- relatorios avancados;
- permissoes complexas;
- integracoes externas;
- modo multiunidade;
- sincronizacao entre computadores;
- importacao em massa;
- dashboards analiticos.

## Dados, privacidade e LGPD

- Coletar apenas os dados necessarios para a V0.
- Nao coletar nomes, e-mails, documentos, matriculas ou outros dados pessoais de
  estudantes na V0.
- O Radar Escola e um produto operacional, nao pedagogico ou academico. A V0 deve
  registrar necessidades da instituicao, equipamentos, locais, envolvidos
  operacionais e historico de resolucao.
- Se uma necessidade envolver estudantes indiretamente, o registro deve
  descrever o problema operacional sem identificar estudantes.
- Deixar claro que os dados ficam no computador da instituicao.
- Nao enviar dados para nuvem por padrao.
- Nao adicionar telemetria por padrao.
- Nao exigir e-mail pessoal para recuperacao de acesso na V0.
- O acesso normal deve usar usuario e senha.
- A V0 deve prever salvaguarda local para esquecimento de usuario e senha, como
  token simples, pergunta secreta, pessoa responsavel ou fluxo manual
  documentado.
- Senhas nunca devem ser armazenadas em texto claro.
- O produto deve salvar os dados no banco local e permitir exportacao CSV de
  seguranca.
- O produto deve prever caminho futuro para editar ou remover dados pessoais.

## Recuperacao de acesso

- Recuperacao por e-mail pessoal nao deve fazer parte do fluxo principal da V0.
- O produto deve usar usuario e senha como forma normal de acesso.
- A direcao da escola deve ser tratada como responsavel maxima inicial pelo
  cadastro da escola, primeira senha e salvaguarda de acesso.
- Durante a configuracao inicial, o produto deve exibir alerta claro sobre a
  importancia de nao perder usuario, senha e salvaguarda.
- A salvaguarda local deve combinar usuario ou nome do responsavel, token simples
  e pergunta secreta.
- O token e a pergunta secreta devem ser apresentados de forma que a direcao ou
  pessoa responsavel consiga anotar e guardar em local seguro.
- A resposta secreta nao deve ser armazenada em texto claro.
- Se usuario, senha e salvaguarda forem perdidos, o acesso administrativo pode
  ser perdido. Nesse caso, a recuperacao dependera de um procedimento tecnico
  documentado, se existir.
- A recuperacao de acesso nao deve quebrar a promessa de uso local/offline.

## Acompanhamento pelos envolvidos

- Cada envolvido deve consultar o Radar Escola no computador em que o aplicativo
  esta instalado, usando seu usuario e senha.
- A V0 nao deve enviar e-mails automaticos.
- A V0 nao deve depender de WhatsApp, mensageria, push notification ou qualquer
  vendor externo para acompanhar necessidades.
- O produto deve manter necessidades em andamento e paradas muito visiveis no
  Radar de Necessidades.
- A tela de necessidades paradas deve ajudar a manter o assunto quente sem
  depender de notificacoes externas.
- Integracoes de notificacao podem ser discutidas depois da V0, se houver
  necessidade real, baixo atrito de implantacao e guardrails de privacidade.

## Exportacao de seguranca

- O banco local e a persistencia principal da V0.
- Exportacao CSV de seguranca deve ser parte da V0.
- O sistema deve orientar explicitamente que a exportacao seja salva fora do
  computador principal, como pendrive, pasta de rede ou outra maquina.
- Exportar CSV deve ser simples para uma pessoa responsavel nao tecnica.
- O CSV deve ser legivel fora do aplicativo.
- Importacao/restauracao completa a partir de CSV pode ser avaliada depois, mas
  nao deve bloquear a V0.

## Arquitetura

- Stack inicial: Tauri + React + TypeScript + SQLite.
- React e TypeScript concentram experiencia, telas, componentes, formularios,
  estados, validacoes e regras simples de aplicacao.
- SQLite e o banco local, gratuito e embutido.
- Tauri e Rust atuam como casca desktop e ponte nativa minima.
- Rust nao deve ser o centro da regra de negocio na V0.
- A arquitetura deve favorecer componentes pequenos, pastas por dominio,
  validacoes centralizadas, testes focados e convencoes simples.
- Evitar abstracoes prematuras e dependencias desnecessarias.

## Testes automatizados

A V0 deve nascer com testes automatizados proporcionais ao risco do produto.

### Testes unitarios

Devem cobrir regras puras e validacoes, incluindo:

- criacao de necessidade;
- transicoes de status permitidas;
- marcacao de envolvidos;
- regras de prioridade;
- regras de necessidades paradas;
- validacao de campos obrigatorios;
- validacao de usuario;
- regras de token simples e pergunta secreta de recuperacao;
- regras de plano de acao;
- fechamento/resolucao de necessidade.

### Testes de persistencia

Devem cobrir o uso do SQLite em cenarios essenciais:

- criacao e leitura de necessidade;
- atualizacao de andamento;
- vinculo entre necessidade e equipamento;
- registro de historico;
- criacao e leitura de equipamento;
- migracoes basicas do banco;
- integridade minima dos dados.

### Testes de exportacao de seguranca

Devem cobrir fluxos criticos de dados:

- exportacao de necessidades em CSV;
- exportacao de equipamentos em CSV;
- cabecalhos esperados;
- dados essenciais presentes;
- erro ao exportar para caminho indisponivel;
- preservacao do banco local apos exportacao.

### Testes de interface

Devem cobrir os fluxos principais da experiencia:

- primeira abertura;
- registro de uma necessidade;
- exibicao da necessidade no radar;
- atualizacao de andamento;
- registro de resolucao;
- visualizacao de historico;
- criacao de equipamento basico;
- fluxo de exportacao CSV de seguranca.

### Testes de integracao desktop

Devem ser adicionados quando o empacotamento Tauri estiver disponivel:

- abertura do aplicativo;
- acesso ao banco local;
- leitura e escrita de arquivos permitidos;
- escolha de destino para exportacao CSV;
- funcionamento basico no Windows.

### Guardrail de cobertura

- A cobertura deve priorizar fluxos criticos, nao porcentagem artificial.
- Mudancas em regras de necessidade, persistencia, exportacao CSV,
  acompanhamento pelos envolvidos ou recuperacao de acesso devem incluir testes
  automatizados.
- Bugs corrigidos devem receber teste de regressao sempre que possivel.
- A ausencia de teste em area critica deve ser justificada no pull request.

## Acessibilidade e linguagem

- A interface deve ser em Portugues Brasileiro.
- Evitar termos tecnicos como ticket, service desk, incidente, workflow e
  dashboard na experiencia principal.
- Usar linguagem simples e orientada a intencao.
- Campos e botoes devem ser compreensiveis para pessoas nao tecnicas.
- Fluxos importantes devem funcionar com teclado.
- Estados vazios, erros e confirmacoes devem ser claros.

## Criterios de aceite para avancar alem da V0

Antes de ampliar escopo, a V0 deve demonstrar:

- instalacao ou execucao local funcional;
- registro de necessidade;
- acompanhamento no Radar de Necessidades;
- atualizacao de andamento;
- resolucao documentada;
- historico preservado;
- exportacao CSV de seguranca;
- testes automatizados dos fluxos criticos;
- documentacao minima para usuario e contribuidor.
