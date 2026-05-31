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
- instalacao simples, preferencialmente com Docker;
- uso em pt-BR;
- interface acessivel e responsiva.

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
