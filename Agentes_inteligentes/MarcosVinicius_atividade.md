# Atividade sobre agentes inteligentes

Aula 20/10/2026 \| Professora Kadidja Valéria \| Inteligência artificial

**Disciplina:** Linguagens Formais e Autômatos \| Ciência da Computação\
**Estudante:** Marcos Vinicius De Souza Duarte \| **Turma:** N1

Realize os exercícios 2.3, 2.4 e 2.5 do Capítulo 2 sobre agentes
inteligentes. Analise a racionalidade, descreva ambientes de tarefa por
meio do modelo PEAS e explique os conceitos com suas próprias palavras.
Utilize o capítulo disponibilizado e justifique suas respostas.

**Modalidade sugerida:** individual com consulta. **Tempo estimado:**
2h30. **Prazo:** conforme orientação da professora.

## Preparação

Leia os tópicos sobre racionalidade, ambientes e estrutura dos agentes,
especialmente a Seção 2.3.2.

## Exercício 2.3

Para cada afirmação, indique V ou F, justifique e forneça exemplo ou
contraexemplo. Explicite as hipóteses utilizadas.

### a. Um agente que detecta apenas informações parciais sobre o estado não pode ser perfeitamente racional.

-   **Julgamento: Falso.**
-   **Justificativa:** Racionalidade não exige conhecer todo o estado do
    ambiente; significa escolher a ação que maximiza o desempenho
    esperado com base nas percepções e no conhecimento disponíveis.
-   **Exemplo ou contraexemplo:** Um jogador de pôquer não vê as cartas
    dos adversários, mas pode escolher a melhor jogada com base nas
    probabilidades.

### b. Existem ambientes de tarefa nos quais nenhum agente reativo puro pode comportar-se racionalmente.

-   **Julgamento: Verdadeiro.**
-   **Justificativa:** Um agente reativo puro considera somente a
    percepção atual. Se a ação correta depender de informações
    anteriores que não aparecem na percepção atual, ele não consegue
    agir racionalmente em todas as situações.
-   **Exemplo ou contraexemplo:** Um aspirador que não lembra os cômodos
    já limpos pode repetir movimentos e deixar áreas sem limpar; um
    agente com estado interno pode evitar isso.

### c. Existe um ambiente de tarefa em que todo agente é racional.

-   **Julgamento: Verdadeiro.**
-   **Justificativa:** Pode-se definir um ambiente em que a medida de
    desempenho atribui o mesmo resultado a todas as ações. Nesse caso,
    todas maximizam o desempenho esperado.
-   **Exemplo ou contraexemplo:** Em um ambiente cuja pontuação é sempre
    zero, qualquer ação produz o mesmo desempenho.

### d. A entrada para o programa de agente é a mesma que a entrada para a função de agente.

-   **Julgamento: Falso.**
-   **Justificativa:** A função de agente associa a sequência completa
    de percepções a uma ação. O programa recebe a percepção atual e pode
    usar um estado interno para guardar informações relevantes do
    histórico.
-   **Exemplo ou contraexemplo:** A função pode considerar todas as
    percepções anteriores; o programa pode receber apenas a percepção
    atual e atualizar uma memória interna.

### e. Toda função de agente é implementável por uma combinação de programa/máquina.

-   **Julgamento: Falso.**
-   **Justificativa:** Algumas funções exigiriam memória ilimitada,
    recursos fisicamente impossíveis ou resolveriam problemas não
    computáveis. Nem toda função matemática pode ser executada por uma
    máquina real.
-   **Exemplo ou contraexemplo:** Uma tabela infinita com uma resposta
    para toda sequência possível de percepções não pode ser armazenada
    integralmente em um computador físico.

### f. Suponha que um agente selecione sua ação uniformemente ao acaso do conjunto de ações possíveis. Existe um ambiente de tarefa determinista em que esse agente é racional.

-   **Julgamento: Verdadeiro.**
-   **Justificativa:** Se todas as ações possíveis tiverem o mesmo
    resultado, a escolha aleatória será tão boa quanto uma escolha fixa.
    O ambiente pode ser determinista mesmo que o agente escolha ao
    acaso.
-   **Exemplo ou contraexemplo:** Todas as portas de um jogo levam ao
    mesmo prêmio, independentemente da porta escolhida.

### g. É possível para um dado agente ser perfeitamente racional em dois ambientes de tarefa distintos.

-   **Julgamento: Verdadeiro.**
-   **Justificativa:** A racionalidade depende do ambiente e da medida
    de desempenho. Um mesmo agente pode maximizar o desempenho esperado
    em mais de um ambiente.
-   **Exemplo ou contraexemplo:** Um aspirador que mapeia o local pode
    limpar racionalmente uma casa de dois cômodos e outra de quatro,
    adaptando seu percurso.

### h. Todo agente é racional em um ambiente não observável.

-   **Julgamento: Falso.**
-   **Justificativa:** A falta de percepções não torna automaticamente
    racional qualquer ação. As ações ainda podem ter consequências
    diferentes, e o agente deve escolher considerando o conhecimento
    disponível e o desempenho esperado.
-   **Exemplo ou contraexemplo:** Um robô que, sem enxergar, avança
    sempre mesmo quando pode cair de uma escada não está necessariamente
    escolhendo a melhor ação.

### i. Um agente jogador de pôquer perfeitamente racional nunca perde.

-   **Julgamento: Falso.**
-   **Justificativa:** Um agente racional maximiza o desempenho
    esperado, mas não controla todos os resultados de um ambiente
    incerto.
-   **Exemplo ou contraexemplo:** Mesmo com uma mão estatisticamente
    forte e uma decisão correta, o adversário pode receber uma carta
    improvável e vencer.

## Exercício 2.4

Para cada caso, delimite o agente, preencha o PEAS e justifique todas as
classificações. Titã é considerado um cenário hipotético.

### Caso 1 --- Jogar futebol

-   **Agente analisado:** Um jogador individual.
-   **Objetivo e hipóteses:** Ajudar a equipe a vencer, marcar gols,
    criar oportunidades e evitar faltas.
-   **P --- Desempenho:** Gols, vitórias, passes corretos, recuperação
    de bola e faltas.
-   **E --- Ambiente:** Campo, bola, colegas, adversários, árbitro e
    condições climáticas.
-   **A --- Atuadores:** Pernas, pés, cabeça, tronco e voz.
-   **S --- Sensores:** Visão, audição e percepção corporal.

  -----------------------------------------------------------------------
  Propriedade             Classificação           Justificativa
  ----------------------- ----------------------- -----------------------
  Observabilidade         Parcialmente observável O jogador não vê tudo
                                                  ao seu redor nem
                                                  conhece as intenções
                                                  dos demais.

  Número de agentes       Multiagente; cooperação Coopera com sua equipe
                          e competição            e compete contra os
                                                  adversários.

  Previsibilidade         Estocástico             As ações dos jogadores
                                                  e os desvios da bola
                                                  tornam os resultados
                                                  incertos.

  Dependência entre       Sequencial              Cada passe ou movimento
  decisões                                        afeta as jogadas
                                                  seguintes.

  Mudança durante a       Dinâmico                O jogo continua
  decisão                                         enquanto o jogador
                                                  decide.

  Natureza dos elementos  Contínuo e discreto     Movimento é contínuo;
                                                  gols, faltas e placar
                                                  são discretos.

  Conhecimento do         Conhecido quanto às     As regras são
  funcionamento           regras                  conhecidas, mas as
                                                  estratégias dos rivais
                                                  não.
  -----------------------------------------------------------------------

### Caso 2 --- Explorar os oceanos subterrâneos de Titã

-   **Agente analisado:** Submarino robótico autônomo hipotético.
-   **Objetivo e hipóteses:** Explorar, coletar amostras, mapear e
    transmitir dados sem perder o robô; o ambiente ainda não foi
    totalmente mapeado.
-   **P --- Desempenho:** Qualidade e quantidade das amostras, dados
    transmitidos, área mapeada e preservação do robô.
-   **E --- Ambiente:** Oceano subterrâneo hipotético, rochas,
    obstáculos, correntes e limitações de comunicação.
-   **A --- Atuadores:** Propulsores, leme, braço mecânico, coletor e
    sistema de comunicação.
-   **S --- Sensores:** Sonar, câmeras, sensores de pressão,
    temperatura, orientação e proximidade.

  -----------------------------------------------------------------------
  Propriedade             Classificação           Justificativa
  ----------------------- ----------------------- -----------------------
  Observabilidade         Parcialmente observável Os sensores só medem
                                                  uma parte do ambiente e
                                                  podem não detectar
                                                  obstáculos distantes.

  Número de agentes       Agente único            Considera-se somente o
                                                  submarino como decisor
                                                  autônomo.

  Previsibilidade         Estocástico             Correntes, falhas e
                                                  condições ambientais
                                                  introduzem incerteza.

  Dependência entre       Sequencial              A rota e as coletas
  decisões                                        anteriores afetam
                                                  recursos e decisões
                                                  futuras.

  Mudança durante a       Dinâmico                Correntes e condições
  decisão                                         podem mudar durante a
                                                  exploração.

  Natureza dos elementos  Contínuo e discreto     Posição e pressão são
                                                  contínuas; amostras e
                                                  estados operacionais
                                                  podem ser discretos.

  Conhecimento do         Parcialmente            O robô conhece seus
  funcionamento           desconhecido            instrumentos, mas não o
                                                  relevo nem todas as
                                                  condições locais.
  -----------------------------------------------------------------------

### Caso 3 --- Comprar livros usados de IA na Internet

-   **Agente analisado:** Programa autônomo de compras (softbot).
-   **Objetivo e hipóteses:** Comprar um livro adequado, em boas
    condições e pelo menor custo total, incluindo frete; anúncios e
    estoque podem mudar.
-   **P --- Desempenho:** Adequação, conservação, preço total, frete,
    confiabilidade do vendedor e sucesso da compra.
-   **E --- Ambiente:** Lojas virtuais, marketplaces, anúncios,
    vendedores, compradores e conexões de rede.
-   **A --- Atuadores:** Requisições HTTP, pesquisas, filtros, carrinho
    e confirmação de compra.
-   **S --- Sensores:** Respostas HTTP, HTML, preços, descrições,
    avaliações, estoque e confirmações.

  -----------------------------------------------------------------------
  Propriedade             Classificação           Justificativa
  ----------------------- ----------------------- -----------------------
  Observabilidade         Parcialmente observável O anúncio pode não
                                                  mostrar a condição real
                                                  do livro ou o estoque
                                                  atualizado.

  Número de agentes       Multiagente e           Outros compradores
                          competitivo             podem adquirir o mesmo
                                                  exemplar; vendedores
                                                  definem preço e
                                                  condições.

  Previsibilidade         Estocástico             Estoque, anúncios e
                                                  rede podem mudar, e
                                                  outros compradores agem
                                                  independentemente.

  Dependência entre       Sequencial              Pesquisa, comparação,
  decisões                                        verificação do frete e
                                                  compra são etapas
                                                  relacionadas.

  Mudança durante a       Dinâmico                Preços e
  decisão                                         disponibilidade podem
                                                  mudar durante a busca.

  Natureza dos elementos  Predominantemente       Produtos e estados de
                          discreto, com valores   compra são discretos;
                          numéricos               preços e fretes são
                                                  numéricos.

  Conhecimento do         Parcialmente conhecido  O agente conhece o uso
  funcionamento                                   do site, mas não os
                                                  processos internos nem
                                                  a condição real do
                                                  livro.
  -----------------------------------------------------------------------

### Caso 4 --- Jogar uma partida de tênis

-   **Agente analisado:** Um dos jogadores.
-   **Objetivo e hipóteses:** Vencer a partida, escolhendo golpes e
    posicionamentos que aumentem a chance de ganhar pontos.
-   **P --- Desempenho:** Pontos, games e sets vencidos, vitória e erros
    não forçados.
-   **E --- Ambiente:** Quadra, rede, bola, adversário, árbitro e clima.
-   **A --- Atuadores:** Braços, mãos, pernas, tronco e raquete.
-   **S --- Sensores:** Visão, audição, equilíbrio e percepção corporal.

  -----------------------------------------------------------------------
  Propriedade             Classificação           Justificativa
  ----------------------- ----------------------- -----------------------
  Observabilidade         Parcialmente observável O jogador vê a bola,
                                                  mas não conhece
                                                  exatamente a intenção
                                                  do adversário.

  Número de agentes       Multiagente e           Os jogadores tentam
                          competitivo             vencer um ao outro.

  Previsibilidade         Estocástico             Golpes, ressaltos e
                                                  decisões adversárias
                                                  geram incerteza.

  Dependência entre       Sequencial              Cada golpe influencia a
  decisões                                        resposta e os golpes
                                                  seguintes.

  Mudança durante a       Dinâmico                Bola e jogadores
  decisão                                         continuam em movimento.

  Natureza dos elementos  Contínuo e discreto     Movimento é contínuo;
                                                  pontos, games e sets
                                                  são discretos.

  Conhecimento do         Conhecido quanto às     As regras são
  funcionamento           regras                  conhecidas, mas as
                                                  ações futuras do rival
                                                  não.
  -----------------------------------------------------------------------

### Caso 5 --- Praticar tênis contra uma parede

-   **Agente analisado:** Pessoa que rebate a bola contra uma parede.
-   **Objetivo e hipóteses:** Treinar precisão, controle, movimentação e
    consistência, sem outro agente controlando a parede.
-   **P --- Desempenho:** Rebatidas consecutivas, precisão, controle e
    evolução técnica.
-   **E --- Ambiente:** Parede, quadra, bola, raquete, piso e condições
    físicas do local.
-   **A --- Atuadores:** Braços, mãos, pernas, tronco e raquete.
-   **S --- Sensores:** Visão, audição, equilíbrio e percepção corporal.

  -----------------------------------------------------------------------
  Propriedade             Classificação           Justificativa
  ----------------------- ----------------------- -----------------------
  Observabilidade         Parcialmente observável A bola e a parede são
                                                  visíveis, mas nem todos
                                                  os efeitos físicos são
                                                  medidos com precisão;
                                                  num modelo idealizado,
                                                  pode ser completamente
                                                  observável.

  Número de agentes       Agente único            A parede não decide nem
                                                  age intencionalmente;
                                                  apenas reflete a bola.

  Previsibilidade         Determinístico no       As leis físicas
                          modelo ideal;           determinam a trajetória
                          aproximadamente         ideal, mas pequenas
                          estocástico na prática  variações reais
                                                  dificultam a previsão
                                                  exata.

  Dependência entre       Sequencial              Cada rebatida define a
  decisões                                        trajetória seguinte.

  Mudança durante a       Dinâmico                A bola continua se
  decisão                                         movendo enquanto o
                                                  praticante se prepara.

  Natureza dos elementos  Contínuo e discreto     Trajetória e velocidade
                                                  são contínuas; número
                                                  de rebatidas é
                                                  discreto.

  Conhecimento do         Conhecido               O praticante entende o
  funcionamento           aproximadamente         exercício, mas não
                                                  calcula perfeitamente
                                                  todos os efeitos
                                                  físicos.
  -----------------------------------------------------------------------

### Caso 6 --- Realizar um salto de altura

-   **Agente analisado:** Atleta que executa o salto.
-   **Objetivo e hipóteses:** Superar a maior altura possível sem
    derrubar a barra e sem se lesionar.
-   **P --- Desempenho:** Altura superada, tentativas válidas, resultado
    e segurança.
-   **E --- Ambiente:** Pista, barra, suportes, colchão, árbitros e
    condições climáticas.
-   **A --- Atuadores:** Pernas, pés, braços e tronco.
-   **S --- Sensores:** Visão, audição, equilíbrio, propriocepção e
    tato.

  -----------------------------------------------------------------------
  Propriedade             Classificação           Justificativa
  ----------------------- ----------------------- -----------------------
  Observabilidade         Parcialmente observável O atleta vê a barra,
                                                  mas não mede
                                                  perfeitamente todas as
                                                  condições físicas nem
                                                  prevê sua execução.

  Número de agentes       Agente único durante a  O salto depende dos
                          execução                movimentos do atleta;
                                                  outros competidores
                                                  afetam a classificação
                                                  geral, não a mecânica
                                                  do salto.

  Previsibilidade         Estocástico na prática  Pequenas variações de
                                                  velocidade, impulsão e
                                                  postura tornam o
                                                  resultado incerto.

  Dependência entre       Sequencial              Corrida, impulsão e
  decisões                                        passagem pela barra
                                                  precisam estar
                                                  coordenadas.

  Mudança durante a       Dinâmico                O corpo se move durante
  decisão                                         toda a execução.

  Natureza dos elementos  Contínuo e discreto     Posição e altura são
                                                  contínuas; tentativas
                                                  válidas e faltas são
                                                  discretas.

  Conhecimento do         Conhecido em termos     Regras e técnicas são
  funcionamento           gerais                  conhecidas, mas a
                                                  resposta corporal exata
                                                  não é totalmente
                                                  previsível.
  -----------------------------------------------------------------------

### Caso 7 --- Participar de um leilão de um item, realizando lances

-   **Agente analisado:** Participante que decide quanto e quando
    oferecer lances.
-   **Objetivo e hipóteses:** Tentar obter o item sem ultrapassar o
    orçamento; considera-se um leilão com outros licitantes e regras
    anunciadas.
-   **P --- Desempenho:** Conseguir o item por preço aceitável,
    respeitar o orçamento e evitar pagar acima do valor atribuído ao
    item.
-   **E --- Ambiente:** Plataforma de leilão, item, preço atual, regras,
    prazo, leiloeiro e participantes.
-   **A --- Atuadores:** Enviar lances, definir limite máximo,
    retirar-se quando permitido e confirmar participação.
-   **S --- Sensores:** Preço atual, histórico de lances disponível,
    tempo restante, regras, mensagens e resultado.

  -----------------------------------------------------------------------
  Propriedade             Classificação           Justificativa
  ----------------------- ----------------------- -----------------------
  Observabilidade         Parcialmente observável O participante vê os
                                                  lances divulgados, mas
                                                  não conhece os limites
                                                  e as intenções dos
                                                  concorrentes.

  Número de agentes       Multiagente e           Os participantes
                          competitivo             disputam o mesmo item.

  Previsibilidade         Estocástico             As ações estratégicas
                                                  dos concorrentes são
                                                  incertas, ainda que as
                                                  regras sejam
                                                  conhecidas.

  Dependência entre       Sequencial              Cada lance influencia o
  decisões                                        preço e as decisões
                                                  seguintes.

  Mudança durante a       Dinâmico                Preço e tempo restante
  decisão                                         mudam durante o leilão.

  Natureza dos elementos  Discreto com variáveis  Lances e estados são
                          numéricas               discretos; preço e
                                                  tempo são valores
                                                  numéricos.

  Conhecimento do         Regras conhecidas,      As regras podem ser
  funcionamento           concorrentes            públicas, mas os
                          parcialmente            limites e estratégias
                          desconhecidos           dos demais não são
                                                  conhecidos.
  -----------------------------------------------------------------------

### Opções para classificação

-   **Observabilidade:** Completamente observável, parcialmente
    observável ou não observável.
-   **Número de agentes:** Agente único ou multiagente; indique
    cooperação ou competição quando pertinente.
-   **Previsibilidade:** Determinístico ou estocástico; considere a
    influência estratégica de outros agentes.
-   **Dependência entre decisões:** Episódico ou sequencial.
-   **Mudança durante a decisão:** Estático, dinâmico ou semidinâmico.
-   **Natureza dos elementos:** Discretos, contínuos ou combinação;
    considere estados, tempo, percepções e ações.
-   **Conhecimento do funcionamento:** Conhecido ou desconhecido para o
    agente.

### Comparação final

1.  **O que muda entre jogar tênis contra outra pessoa e praticar contra
    uma parede?** Contra uma pessoa, o ambiente é multiagente e
    competitivo, pois o adversário escolhe ações próprias. Contra uma
    parede, há um único agente decisor e a bola retorna conforme as leis
    físicas, tornando o comportamento geralmente mais previsível.
2.  **Por que comprar livros usados pode exigir decisões com informações
    incompletas?** O anúncio pode não refletir a condição real do livro,
    o estoque pode estar desatualizado e outro comprador pode adquirir o
    exemplar antes da conclusão da compra.
3.  **Como outros agentes influenciam futebol e leilões?** No futebol,
    colegas e adversários mudam as oportunidades de passe, ataque e
    defesa. No leilão, os lances dos concorrentes alteram a disputa. O
    agente precisa antecipar ações alheias para melhorar seu resultado.

## Exercício 2.5

Defina cada termo com suas palavras em duas a quatro linhas e apresente
um exemplo.

### Agente

-   **Definição:** Algo que percebe o ambiente por sensores e age sobre
    ele por atuadores. Pode ser uma pessoa, um robô ou um programa.
-   **Exemplo:** Um termostato mede a temperatura e liga ou desliga o
    ar-condicionado.

### Função de agente

-   **Definição:** Descrição abstrata que associa cada sequência
    possível de percepções a uma ação. Define o comportamento esperado
    sem especificar necessariamente como ele foi programado.
-   **Exemplo:** Uma tabela que manda o aspirador aspirar ao detectar
    sujeira e se deslocar quando o local está limpo.

### Programa de agente

-   **Definição:** Implementação concreta da função de agente, executada
    em uma arquitetura computacional ou física. Processa percepções e
    produz ações.
-   **Exemplo:** Código Python que lê a temperatura e liga o
    ar-condicionado quando ela ultrapassa um limite.

### Racionalidade

-   **Definição:** Escolher a ação que oferece o melhor desempenho
    esperado com as percepções e o conhecimento disponíveis. Ser
    racional não significa acertar sempre ou prever o futuro.
-   **Exemplo:** Um sistema ABS ajusta a frenagem para reduzir o risco
    de travamento das rodas.

### Autonomia

-   **Definição:** Capacidade de agir com base nas próprias percepções e
    experiências, sem depender apenas de informações programadas
    previamente. Um agente autônomo pode aprender e se adaptar.
-   **Exemplo:** Um robô aspirador que mapeia uma casa desconhecida e
    ajusta sua rota.

### Agente reativo

-   **Definição:** Escolhe ações com base na percepção atual, sem usar o
    histórico completo nem manter necessariamente um modelo interno do
    mundo.
-   **Exemplo:** Um termostato simples que liga o ar-condicionado quando
    a temperatura passa de um limite.

### Agente baseado em modelo

-   **Definição:** Mantém um estado interno sobre aspectos do ambiente
    que não consegue perceber diretamente. Atualiza esse estado com
    novas percepções e conhecimento sobre como o mundo funciona.
-   **Exemplo:** Um robô que lembra quais áreas já percorreu para
    continuar a limpeza.

### Agente baseado em objetivos

-   **Definição:** Escolhe ações considerando um objetivo que deseja
    alcançar. Pode comparar sequências de ações para chegar ao estado
    desejado.
-   **Exemplo:** Um programa de xadrez que analisa jogadas para buscar o
    xeque-mate.

### Agente baseado em utilidade

-   **Definição:** Avalia resultados possíveis por uma medida de
    utilidade e escolhe a ação de maior valor esperado. Ajuda a
    equilibrar custo, tempo e qualidade.
-   **Exemplo:** Um aplicativo de rotas que compara duração, distância e
    pedágios.

### Agente com aprendizagem

-   **Definição:** Melhora seu comportamento com experiências e
    feedback, ajustando decisões conforme identifica padrões e observa
    resultados.
-   **Exemplo:** Um filtro de e-mail que aprende a reconhecer spam a
    partir das marcações do usuário.

## Síntese com autômatos

**Cenário:** Comprar livros usados de IA pela Internet (softbot).

**Estados internos:** `BuscandoLivro`, `ValidandoPreco`, `Comprando`.

**Percepções:** `[SemResultados]`, `[LivroEncontradoAbaixo50]`,
`[LivroEncontradoAcima50]`.

**Ações:** `PesquisarNovamente()`, `AdicionarAoCarrinho()`,
`Descartar()`.

**Regras:** -
`BuscandoLivro + [LivroEncontradoAbaixo50] → ValidandoPreco` e executa
`AdicionarAoCarrinho()`. -
`ValidandoPreco + [SemResultados] → BuscandoLivro` e executa
`PesquisarNovamente()`.

**Explicação:** O estado interno registra a etapa do processo e guarda
informações obtidas anteriormente, permitindo continuar a tarefa sem
reiniciar a busca a cada percepção. A modelagem é simplificada: não
representa todas as incertezas, como mudanças no estoque, falhas de
conexão ou relações entre reputação do vendedor, frete e preço. Uma
implementação real também precisaria de regras explícitas para confirmar
a compra e evitar transações duplicadas.

## Entrega e avaliação

Confira: identificação; nove análises no item 2.3; sete casos completos
no item 2.4; dez conceitos no item 2.5; síntese; referências.

Nome sugerido: `NomeSobrenome_Atividade_AgentesInteligentes`.
Prazo e envio conforme orientação da professora.

  Critério                                          Atividade avaliativa (1,0 ponto) A2
  ----------------------------------------------- -------------------------------------
  Item 2.3 --- correção e argumentação                                              30%
  Item 2.4 --- PEAS e classificação justificada                                     40%
  Item 2.5 --- precisão conceitual e exemplos                                       20%
  Síntese, organização e referências                                                10%

## Referências

Material-base: Capítulo 2 --- Agentes inteligentes, disponibilizado para
a aula de 19/10/2026.

Referência adicional: Russell, S.; Norvig, P. *Inteligência Artificial:
uma abordagem moderna*. Capítulo 2 --- Agentes inteligentes. Conferir a
edição utilizada pela disciplina.
