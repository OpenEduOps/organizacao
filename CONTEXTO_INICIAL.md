# Contexto Inicial

Este documento registra uma fotografia inicial do raciocinio estrategico do
OpenEduOps. Ele nao pretende ser definitivo. A ideia e preservar o contexto como
esta agora, para que a organizacao possa evoluir suas decisoes com mais clareza
ao longo do tempo.

## Recorte do problema

Ao observar o contexto educacional brasileiro como um todo, especialmente a
realidade publica e mais precarizada, existe uma cadeia longa de desafios desde
a entrada do individuo no sistema educacional ate a saida da universidade.

Muitos desses desafios sao pedagogicos, sociais, economicos ou politicos. O
OpenEduOps, neste momento inicial, nao deve tentar resolver todos eles.

O ponto de partida mais saudavel parece estar na intersecao entre:

- dor institucional real;
- simplicidade tecnica;
- baixo custo de implantacao;
- utilidade imediata para escolas, institutos e universidades;
- potencial de formacao pratica para novos contribuidores;
- possibilidade de evolucao incremental.

Por esse motivo, o primeiro foco recomendado nao esta na sala de aula, em
plataformas pedagogicas, em ambientes virtuais de aprendizagem ou em solucoes
baseadas em inteligencia artificial.

O primeiro foco recomendado esta na operacao basica das instituicoes
educacionais.

## Hipotese central

Instituicoes educacionais publicas e comunitarias frequentemente sofrem com
problemas operacionais invisiveis, mas essenciais:

- laboratorios de informatica quebrados ou subutilizados;
- computadores, projetores, roteadores, impressoras e notebooks sem inventario
  confiavel;
- manutencoes solicitadas por WhatsApp, papel, e-mail solto ou conversas
  informais;
- falta de historico sobre problemas recorrentes;
- disputa por salas, laboratorios e equipamentos compartilhados;
- equipes tecnicas pequenas e sobrecarregadas;
- direcoes sem dados simples para justificar compras, manutencoes ou
  prioridades;
- perda de continuidade quando servidores, tecnicos, coordenadores ou
  voluntarios saem da instituicao.

Esses problemas parecem administrativos, mas afetam diretamente a experiencia
educacional.

Um laboratorio sem manutencao pode significar aula cancelada. Um equipamento
sem controle pode significar recurso publico desperdicado. Um chamado esquecido
pode impedir um professor de executar uma atividade. A falta de historico torna
cada troca de equipe um recomeco.

## Ponto de partida recomendado

A aposta inicial do OpenEduOps deve ser uma solucao simples para chamados,
ativos e manutencao em instituicoes educacionais.

Uma formulacao possivel:

> Uma central operacional simples para escolas e instituicoes educacionais,
> combinando chamados internos, inventario basico de equipamentos e historico
> de manutencao.

Esse recorte e promissor porque:

- resolve uma dor real e recorrente;
- pode ser demonstrado com facilidade;
- nao depende de integracoes externas complexas;
- nao exige acesso a sistemas institucionais sensiveis;
- pode funcionar em rede local ou infraestrutura simples;
- gera muitas oportunidades de contribuicao pequenas, reais e educativas;
- atende desde escolas pequenas ate departamentos universitarios;
- permite evolucao por modulos.

## Primeiro produto possivel

Um primeiro produto pode ser chamado provisoriamente de `EduDesk`.

O nome ainda nao e uma decisao final. Ele representa a ideia de uma central
operacional simples para instituicoes educacionais.

### MVP inicial

O MVP deve priorizar:

- abertura de chamados internos;
- acompanhamento de status;
- cadastro basico de equipamentos;
- vinculo entre chamado e equipamento;
- registro de manutencoes;
- comentarios e historico do chamado;
- categorias e prioridades simples;
- perfis basicos, como solicitante, tecnico e gestor;
- relatorios simples;
- exportacao em CSV;
- instalacao simples para Windows;
- banco de dados local;
- possibilidade de uso sem internet;
- uso em pt-BR;
- interface acessivel e responsiva.

## Estrategia de adocao desktop local

Uma evolucao importante da ideia inicial e priorizar a experiencia de uso
concreta de instituicoes com baixa maturidade tecnica.

Para muitas escolas publicas, bibliotecas, laboratorios e pequenos setores
administrativos, a melhor porta de entrada nao e um ambiente Docker, um servidor
Linux ou uma implantacao em nuvem.

A melhor porta de entrada tende a ser:

> Baixar, instalar e usar.

O OpenEduOps deve considerar como principio que seus primeiros produtos precisam
ser programas desktop locais, amigaveis para Windows e utilizaveis com banco de
dados local, sem depender de servicos externos, contas institucionais, internet
constante ou equipe tecnica especializada.

Essa direcao favorece uma experiencia de adocao mais proxima de softwares livres
tradicionais, como LibreOffice, VLC, GIMP, Audacity e 7-Zip: o usuario baixa,
instala, abre pelo icone e usa.

A aplicacao pode usar tecnologias modernas de interface internamente, caso isso
ajude na produtividade, na manutenibilidade e na formacao de contribuidores. No
entanto, a experiencia entregue ao usuario final deve ser a de um programa
desktop comum, nao a de um sistema que precisa ser implantado, hospedado ou
configurado.

Uma formulacao possivel:

> Experiencia do usuario final primeiro, tecnologia depois.

Outra formulacao complementar:

> Desktop local primeiro, infraestrutura depois.

## Modos de uso esperados

### Modo local individual

O usuario instala o sistema em uma maquina Windows, abre o aplicativo e comeca a
usar com banco local.

Esse modo favorece pilotos, testes, secretarias pequenas, bibliotecas,
laboratorios e setores que precisam experimentar a ferramenta sem depender de
uma implantacao institucional formal.

### Modo rede local

Uma maquina pode funcionar como ponto central dentro da escola, biblioteca ou
departamento, permitindo que outras maquinas acessem o sistema pela rede local.

Esse modo preserva a simplicidade, mas ja permite uso coletivo.

### Modo institucional

Instituicoes com equipe tecnica podem optar por uma instalacao mais robusta,
usando Docker, Linux, banco externo e processos formais de backup.

Esse modo deve existir como caminho avancado, nao como requisito inicial para
experimentar o produto.

## Diretriz de produto inicial

Para o primeiro MVP, uma direcao de produto coerente e:

- aplicacao desktop local;
- instalador amigavel para Windows;
- icone na area de trabalho e no menu iniciar;
- banco local, preferencialmente SQLite no inicio;
- backup e restauracao simples;
- exportacao e importacao de dados;
- uso sem internet obrigatoria;
- experiencia de abertura semelhante a um software comum;
- interface simples, direta e em Portugues Brasileiro;
- primeiro uso guiado;
- tecnologia interna escolhida em funcao da experiencia final;
- possibilidade de usar tecnologias modernas de interface internamente, desde
  que isso nao apareca como complexidade para o usuario;
- possibilidade futura de migracao para banco externo;
- Docker como opcao para desenvolvimento, testes e implantacoes tecnicas.

O objetivo nao e abandonar ambientes tecnicos mais robustos. O objetivo e nao
transforma-los em barreira de entrada.

## Regra arquitetural inicial

A arquitetura do primeiro produto deve preservar a experiencia desktop local e
manter a complexidade tecnica invisivel para o usuario final.

Stack escolhida para o primeiro produto:

> Tauri + React + TypeScript + SQLite.

Como regra inicial:

- React e TypeScript devem concentrar a experiencia de uso, telas, componentes,
  formularios, estados, validacoes e regras simples de aplicacao;
- SQLite deve ser o banco de dados local, gratuito e embutido;
- Tauri e Rust devem atuar como casca desktop e ponte nativa minima, cuidando
  apenas do que for necessario para janela, instalador, arquivos locais,
  integracao com o sistema operacional e acesso seguro aos recursos nativos.

Rust nao deve ser o centro da regra de negocio no inicio do projeto.

### Justificativa para Rust e Tauri

O uso de Rust neste contexto e justificado principalmente por Tauri e pela
experiencia desktop Windows-first que o OpenEduOps deseja entregar.

Rust nao entra como tecnologia central de produto, nem como objetivo de
aprendizado inicial para todos os contribuidores. Ele entra como base nativa
para permitir que a aplicacao seja distribuida como um programa desktop leve,
instalavel e integrado ao Windows.

Essa escolha ajuda a sustentar a experiencia desejada:

- instalador para Windows;
- abertura por icone, sem expor navegador ou servidor local ao usuario;
- janela propria de aplicativo desktop;
- acesso controlado a arquivos locais;
- suporte a backup e restauracao;
- integracao com recursos do sistema operacional;
- menor peso em comparacao com alternativas desktop mais pesadas;
- possibilidade de manter a maior parte da experiencia e das regras simples em
  React e TypeScript.

Portanto, Rust deve permanecer como infraestrutura discreta. Seu papel e
viabilizar a experiencia "baixar, instalar, abrir e usar" no Windows, mantendo a
complexidade tecnica fora do caminho do usuario final.

O usuario final nao deve precisar saber que existem React, TypeScript, SQLite,
Tauri, Rust, banco de dados ou camadas internas. Ele deve perceber apenas um
programa instalado, simples de abrir e capaz de cadastrar, acompanhar, organizar,
salvar e fazer backup.

## Formacao de contribuidores

O foco inicial deve ser a experiencia do usuario final. Depois disso, a
arquitetura e a tecnologia devem ser alinhadas para gerar boas oportunidades de
aprendizado para contribuidores iniciantes.

Isso significa que o projeto deve buscar um equilibrio entre:

- utilidade real para escolas e instituicoes educacionais;
- experiencia simples para pessoas nao tecnicas;
- codigo compreensivel;
- issues pequenas e bem descritas;
- testes acessiveis;
- documentacao clara;
- oportunidades de aprendizado em interface, regras de negocio, persistencia,
  acessibilidade, instalacao, empacotamento, backup e qualidade.

A formacao dos contribuidores deve nascer de um produto util, nao de um exercicio
artificial de tecnologia.

## Sequencia possivel de produtos

O OpenEduOps pode evoluir em uma sequencia de projetos independentes, mas
relacionados.

### EduDesk

Central de chamados internos, inventario basico e historico de manutencao.

### EduInventory

Inventario de equipamentos, ativos e patrimonio operacional.

### EduLab

Gestao de laboratorios de informatica, computadores, softwares instalados,
estado das maquinas, reservas e incidentes.

### EduRooms

Reserva e gestao de salas, laboratorios e equipamentos compartilhados.

### EduContinuity

Base de conhecimento operacional com procedimentos, contatos, checklists,
rotinas e documentacao institucional.

## Principios para o primeiro MVP

O primeiro MVP deve ser:

- simples de instalar;
- possivel de rodar em computador comum;
- utilizavel em rede local;
- acessivel por celular;
- independente de servicos pagos;
- independente de login institucional complexo;
- claro para contribuidores iniciantes;
- util para uma escola pequena;
- extensivel para institutos, universidades e bibliotecas;
- documentado em Portugues Brasileiro.

## Decisao inicial

O OpenEduOps deve comecar pelo "chao operacional" da educacao.

Antes de tentar transformar a experiencia pedagogica diretamente, o projeto deve
ajudar instituicoes a enxergar, organizar e manter os recursos que ja possuem.

Essa escolha permite impacto pratico, baixo custo inicial e um caminho saudavel
para formar uma comunidade tecnica em torno de problemas reais.
