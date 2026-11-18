# Feedback do Professor > Entrega 09 > Equipe 05

## Avaliação geral

A equipe atende quantitativamente à responsabilidade da Entrega 09. Há três integrantes e foram apresentados três cenários de interação identificados por autoria e origem - CI01, CI02 e CI03 - além de três soluções correspondentes de Design Centrado na Comunicação. Também existe um mapa de objetivos consolidado da equipe e um esquema conceitual de signos único, bastante extenso.

Os três cenários de interação apresentam continuidade explícita com os cenários de problema da Entrega 04. Isso é um ponto positivo importante: a equipe não reiniciou o projeto nesta etapa. C01 evolui para CI01, C02 para CI02 e C03 para CI03. Em cada caso, parte da situação atual é preservada e a solução passa a participar da narrativa.

O principal problema da entrega não é quantidade, e sim **formalismo do modelo conceitual**.

O **mapa de objetivos** precisa de revisão significativa. No estado atual, ele está parcialmente representando uma sequência de ações da interface - enviar PDF, informar dados, consultar métricas, explorar resultados, escolher formato, exportar - em vez de organizar objetivos finais e instrumentais do usuário. Além disso, as relações indicadas pelas setas estão conceitualmente invertidas em vários pontos: os objetivos finais parecem “levar” às ações instrumentais, quando o objetivo instrumental é que deve instrumentar o alcance do objetivo final. Há também divergências entre os IDs/nome dos objetivos no desenho e no dicionário.

No **Design Centrado na Comunicação**, a equipe identificou tópicos, subtópicos e falas de usuário/preposto, mas a coluna “falas e signos” não identifica de modo suficientemente explícito quais signos estão sendo manipulados em cada conversa. Em vários casos, a fala é boa, mas o signo precisa ser inferido pelo leitor. Como esta atividade prepara a modelagem MoLIC, essa ligação deve ficar inequívoca.

O **esquema conceitual de signos** possui boa riqueza e demonstra esforço de levantamento, porém se aproxima em vários trechos de um inventário de componentes de tela. Há muitos signos de expressão e widgets - dropzone, botão, ícone, tooltip, menu - misturados aos signos conceituais do domínio. Também aparecem mensagens sobre BERT e RoBERTa, que são detalhes internos de implementação e não conceitos que deveriam necessariamente fazer parte da linguagem do docente.

A entrega possui uma base bastante aproveitável, mas precisa separar melhor quatro níveis: **objetivo do usuário, conversa usuário–sistema, conceito/signo e elemento concreto de interface**.

## Pontos positivos

- Há um cenário de interação completo e identificado para cada integrante.
- Cada cenário informa claramente qual cenário de problema lhe deu origem.
- CI01 preserva a situação posterior a uma avaliação e introduz a análise pelo sistema sem apagar a motivação original da professora.
- CI02 preserva a revisão preventiva da prova antes da aplicação, que continua sendo o cenário mais diretamente alinhado ao núcleo do projeto.
- CI03 preserva a necessidade de comparar versões destinadas a turmas diferentes e procura transformar a comparação manual em uma atividade apoiada pelo sistema.
- As alterações em relação aos cenários de problema foram destacadas visualmente em negrito e também resumidas em “Diferenças relevantes”.
- Os cenários procuram representar respostas do sistema, feedback, validação, processamento e tratamento de falhas.
- A equipe evita, na maior parte dos cenários, detalhar widgets específicos dentro da narrativa.
- Foram produzidas três estruturas de Design Centrado na Comunicação, uma para cada cenário.
- As conversas utilizam a convenção `U` para usuário e `D` para preposto do designer/sistema.
- CI01 possui uma boa fala sobre interpretação das métricas, incluindo a ressalva de que características estruturais isoladas não comprovam causalidade.
- O mapa consolidado diferencia visualmente alguns objetivos como finais e outros como instrumentais por meio de caixas cheias e tracejadas.
- O esquema de signos está consolidado em uma única estrutura e contém origem, semântica, tipo, restrição, valor padrão, prevenção e recuperação.
- Há bons signos do domínio, como prova, duração, dificuldade, métricas estruturais, tempo estimado de leitura, formalismo, similaridade de distratores, correlação com desempenho e resultados por questão.
- A equipe registra explicitamente que associação/correlação não implica causalidade, o que é importante para a comunicação dos resultados técnicos.
- Há preocupação com prevenção e recuperação de rupturas em situações de upload, duração, processamento e filtragem.

## Correções prioritárias

### 1. Corrigir o mapa de objetivos: hoje ele está parcialmente funcionando como fluxo de tarefas

O mapa de objetivos deve representar **o que o usuário deseja alcançar**, sem descrever como ele executará a interface.

A parte superior do mapa possui três bons candidatos a objetivos finais:

- analisar a estrutura de uma prova antes de aplicá-la;
- analisar uma avaliação após um desempenho abaixo do esperado;
- comparar versões de uma avaliação para identificar diferenças relevantes.

Esses objetivos expressam razões para o docente utilizar o sistema.

A partir daí, porém, o mapa passa a representar uma sequência operacional:

- enviar avaliação em PDF;
- informar dados necessários;
- consultar métricas;
- explorar resultados;
- compreender resultados;
- escolher formato;
- exportar.

Nem todos esses itens possuem o mesmo status conceitual.

“Compreender e interpretar os resultados” pode representar um objetivo instrumental relevante.

“Escolher o formato de exportação”, por outro lado, descreve essencialmente **como** a exportação será feita. É uma decisão/interação da interface, não um objetivo autônomo do usuário.

Da mesma maneira, “enviar PDF” é uma atividade instrumental específica da solução. Se permanecer no mapa, deve estar claramente classificada como objetivo instrumental e sua relação com o objetivo maior deve ser justificada.

A equipe precisa revisar cada caixa perguntando:

**O docente abriria o sistema porque quer atingir este resultado ou esta caixa apenas descreve uma etapa necessária da interface?**

Se for apenas passo operacional, provavelmente pertence ao modelo de tarefas ou à conversa, e não como objetivo independente no mapa.

### 2. Corrigir a direção e a semântica das relações no mapa

No mapa atual, O01, O02 e O03 apontam para O04 e a sequência segue em direção aos passos da interação.

Isso faz o desenho parecer:

**objetivo final → upload → dados → resultados → interpretação**

Entretanto, em um mapa de objetivos, um objetivo instrumental **instrumenta** outro objetivo. A relação não representa simplesmente “o próximo passo do fluxo”.

Por exemplo, se interpretar resultados ajuda o professor a revisar uma avaliação, então a relação deve expressar que esse objetivo instrumental contribui para alcançar o objetivo final de revisão/análise - não que o objetivo final “leva” mecanicamente ao objetivo instrumental.

A equipe precisa reconstruir as relações com a semântica de:

- objetivo final;
- objetivo instrumental direto;
- objetivo instrumental indireto;
- relação de instrumentação.

Não utilizem o mapa de objetivos como um fluxograma da interface.

### 3. Corrigir a classificação visual dos objetivos finais e instrumentais

Na imagem, O01, O02, O03, O04, O05, O06, O07 e O08 aparecem com caixas de linha contínua.

Somente O09 e O10 aparecem tracejados.

Isso sugere que O04–O08 estão sendo classificados visualmente como objetivos finais, o que não parece correto.

“Enviar avaliação”, “informar dados” e “consultar métricas” não parecem ser razões finais pelas quais o professor utiliza a solução; eles servem para atingir algo maior.

A equipe deve revisar a notação e classificar corretamente cada objetivo.

### 4. Alinhar o dicionário de objetivos com a imagem

Há divergências objetivas entre a imagem e o dicionário.

Na imagem:

- O06 = consultar as métricas/análise da prova;
- O07 = explorar os resultados por característica estrutural;
- O09 = escolher o melhor formato para exportação;
- O10 = exportar os resultados.

No dicionário:

- O06 = explorar os resultados por característica estrutural;
- O07 = consultar as métricas e a análise da prova;
- O09 = exportar os resultados;
- O010 = escolher o formato de exportação.

Ou seja, O06/O07 e O09/O10 foram trocados.

Também há inconsistência entre `O10` e `O010`.

Isso precisa ser corrigido antes da Entrega 10, porque os identificadores deverão ser reutilizados no MoLIC. Identificador instável hoje vira confusão de rastreabilidade amanhã.

### 5. Revisar CI01 para não prometer uma relação que o sistema talvez não consiga estabelecer

CI01 diz que o sistema apresenta visões que:

> “relacionam essas características com o desempenho observado na turma”.

Para que isso aconteça, a plataforma precisaria possuir os dados reais do desempenho daquela turma ou receber essas informações.

O cenário e o esquema de signos indicam, em outros pontos, que métricas reais dos estudantes podem ser opcionais.

A equipe precisa deixar claro o que CI01 realmente consegue analisar quando a professora envia apenas a prova.

Se houver dados reais da turma, eles devem aparecer como signos e entradas dessa conversa.

Se não houver, o sistema pode comparar características da prova com relações observadas nos dados de referência do TCC/ENEM, mas não deve apresentar isso como se estivesse explicando diretamente o desempenho daquela turma.

Essa distinção é central para a credibilidade da interface.

### 6. Revisar CI02 para separar “resultado científico” de “garantia prática”

CI02 afirma que o DesemProv permite:

> “compará-las com os impactos observados em questões do ENEM”

e que isso cria uma análise:

> “muito mais comprovada”

do que pedir opinião aos colegas.

Cuidado com a palavra “comprovada”.

A interface pode fornecer dados, indicadores e relações observadas na pesquisa, mas isso não transforma automaticamente cada decisão sobre uma prova específica em conclusão comprovada.

A própria equipe acerta em outros trechos ao afirmar que associação não implica causalidade.

É preciso manter essa mesma cautela em todo o cenário e no Design Centrado na Comunicação.

### 7. CI03 ainda depende de uma hipótese aberta e precisa deixar isso explícito

C03 foi criado anteriormente como nova situação hipotética: comparar versões para turmas diferentes.

Essa necessidade continua registrada como H11 e permanece aberta.

Em CI03, entretanto, a solução passa a oferecer:

- processamento comparativo;
- relatório comparativo direto;
- alertas de discrepâncias;
- indicação de questões a ajustar;
- “confirmação do equilíbrio das versões”.

Isso é uma evolução bastante grande.

A equipe pode projetar uma intervenção para explorar essa hipótese, mas não deve apresentar como fato que o sistema **assegura equivalência** ou que confirma que as versões ficaram equilibradas.

A ferramenta pode apresentar diferenças estruturais. A decisão sobre equivalência pedagógica continua pertencendo ao docente e depende de aspectos que vão além dessas métricas.

Preservem a última frase de CI03, que corretamente afirma que o sistema apoia sem substituir os critérios pedagógicos, e façam o restante da narrativa seguir a mesma lógica.

### 8. Não utilizar o cenário de interação para detalhar prematuramente componentes da interface

Os cenários de interação devem especificar ações do usuário e respostas do sistema, mas sem antecipar detalhes concretos de interface desnecessários.

Em CI03 aparecem expressões como:

- “painel comparativo”;
- “alertas visuais”;
- “relatório comparativo direto”.

Em CI02 aparece detalhamento de “inputs”, conjunto obrigatório/opcional de campos e diversas características específicas.

Esses elementos podem existir na solução, mas o cenário de interação deveria privilegiar:

- o que o usuário informa;
- o que solicita;
- o que o sistema comunica;
- como a atividade progride;
- qual feedback é necessário.

O widget ou representação concreta deve permanecer para etapas de interface/prototipação, salvo quando for essencial à compreensão do cenário.

### 9. No Design Centrado na Comunicação, identificar explicitamente os signos de cada fala

A estrutura da seção utiliza a coluna:

> “Falas e signos envolvidos”

Porém, na prática, a maioria das linhas contém apenas as falas.

O leitor consegue inferir signos como:

- prova;
- arquivo;
- duração;
- dificuldade;
- métrica;
- formalismo;
- desempenho;
- filtro;
- formato de exportação.

Mas a equipe precisa explicitar esses signos.

Por exemplo, após a fala ou em uma indicação associada, registrem quais conceitos estão sendo manipulados naquela conversa.

Isso cria a ponte necessária entre:

**cenário de interação → conversa → signos → esquema conceitual → MoLIC**

Atualmente essa ligação ainda exige interpretação do leitor.

### 10. Corrigir tópicos e subtópicos que representam ações ou estados pouco claros

Alguns tópicos estão adequados, mas outros precisam ser revisados.

Em CI01:

> “Explorar os resultados da avaliação”

funciona como tópico, mas a resposta do sistema:

> “você já pode acessar os resultados como preferir”

é vaga e pouco comunicativa.

O preposto deve comunicar algo concreto que permita ao usuário compreender possibilidades e estado da conversa.

Em CI02:

> “Escolher o melhor formato para exportação”

não deveria pressupor que existe um formato “melhor”; é o usuário quem escolhe o formato adequado à sua intenção.

Em CI03, algumas linhas possuem apenas fala do usuário e nenhuma fala do preposto, embora representem um diálogo/conversa mediada pelo sistema.

A equipe deve revisar a estrutura para que cada subtópico represente uma conversa coerente e não apenas uma lista de ações.

### 11. Revisar CI03 no Design Centrado na Comunicação: “Versão B” está nomeada como primeira avaliação

Há um erro simples, mas relevante para a clareza do modelo.

A linha:

> “Enviar e validar primeira avaliação (Versão B)”

deveria representar a segunda avaliação.

Como o cenário depende justamente da distinção entre duas versões, esses rótulos precisam ser precisos.

### 12. Revisar a presença da exportação nos três cenários

No dicionário, O09/O10 são associados a CI01, CI02 e CI03.

Porém, a exportação aparece claramente apenas na conversa de CI02.

Além disso, a necessidade de exportação já vinha sendo tratada nas entregas anteriores como uma funcionalidade secundária cuja necessidade deveria ser validada.

Se exportar é objetivo instrumental relevante nos três cenários, isso precisa aparecer nas três conversas e ser justificado.

Caso contrário, não generalizem o objetivo para todos os cenários.

### 13. Reorganizar o esquema conceitual de signos para privilegiar conceitos antes de widgets

O esquema contém muitos bons signos conceituais, mas o início da tabela é dominado por elementos de expressão/interface:

- área tracejada;
- ícone de upload;
- texto instrucional;
- botão “Escolher arquivo”;
- botão “Cancelar”;
- título do formulário;
- ícone de ajuda;
- tooltip;
- controle de paginação;
- botão “Iniciar Análise”;
- botão “Exportar”.

Esses elementos podem ser signos de expressão e são úteis em etapas posteriores, mas a Entrega 09 deve construir primeiro a estrutura conceitual da conversa.

A equipe deve garantir destaque e completude para os conceitos que o docente precisa compreender, por exemplo:

- avaliação/prova;
- questão;
- alternativa;
- gabarito;
- duração;
- dificuldade;
- características estruturais;
- formalismo;
- distrator;
- tempo de leitura;
- resultado;
- correlação;
- desempenho;
- filtro/critério de visualização, se realmente necessário;
- versão da avaliação, em CI03.

O esquema não deve virar simplesmente um inventário de cada componente existente na tela.

### 14. Retirar detalhes internos do algoritmo da linguagem oferecida ao usuário

O esquema inclui:

- “Falha ao carregar RoBERTa”;
- “Falha ao carregar BERT”.

BERT e RoBERTa são detalhes de implementação.

A menos que exista uma razão real para o professor conhecer qual modelo interno falhou, essa informação não deveria ser comunicada dessa forma.

Para o usuário, o signo relevante provavelmente é algo como:

- falha no processamento textual;
- análise indisponível;
- processamento não concluído.

O preposto deve comunicar a ruptura em linguagem compatível com o domínio e oferecer recuperação útil.

Expor nomes dos modelos internos não ajuda o docente a resolver o problema.

### 15. Corrigir a classificação de prevenção e recuperação no esquema de signos

A teoria distingue mecanismos como:

- prevenção passiva;
- prevenção ativa;
- prevenção apoiada/alerta;
- recuperação apoiada;
- captura de erro.

O esquema atual descreve ações em texto livre, mas em alguns casos mistura prevenção e recuperação.

Exemplo:

> signo “Texto de restrição”  
> recuperação: “Prevenir envio de arquivo errado”

Isso não é recuperação; é prevenção.

Outro caso:

> “Nenhum filtro escolhido”  
> prevenção: nenhum  
> recuperação: selecionar filtros

Aqui a equipe deveria avaliar se o sistema está apenas orientando o usuário depois da ruptura ou se poderia prevenir ativamente a submissão sem seleção.

A equipe deve classificar os mecanismos de forma consistente com a teoria e, se utilizar siglas, explicar a legenda.

### 16. Revisar a origem de alguns signos

O esquema utiliza corretamente três origens importantes:

- domínio;
- aplicação;
- convencional.

Porém, algumas classificações merecem revisão.

“Duração da prova” é claramente signo de domínio.

“Prova” também.

Já “Tipo de análise” pode ser um conceito criado pela própria aplicação, dependendo de como o TCC organiza as análises.

“Opção de incluir métricas reais” também é uma decisão da aplicação.

O importante é que a origem indique se o conceito já existe no universo do docente, se foi introduzido pelo sistema ou se é convenção comum de interface.

Essa distinção será útil no MoLIC, principalmente para prever rupturas de comunicação.

### 17. Incluir no esquema os signos específicos necessários para CI03, se CI03 permanecer no escopo

CI03 fala de:

- Versão A;
- Versão B;
- comparação;
- discrepância/diferença;
- equilíbrio/equivalência;
- reanálise.

Esses conceitos não estão claramente estruturados no esquema de signos atual.

Se a comparação entre versões permanecer como cenário real da solução, o esquema conceitual precisa representar os signos que essa conversa exige.

Caso contrário, CI03 e o esquema não estarão descrevendo o mesmo sistema conceitual.

### 18. Revisar “Dificuldade das questões” como informação de entrada

CI02 e o esquema assumem que o professor informa a dificuldade de cada questão.

Essa informação precisa de justificativa.

É importante distinguir:

- dificuldade que o docente atribui previamente à questão;
- dificuldade inferida/estimada pelo sistema;
- dificuldade observada empiricamente após aplicação;
- dificuldade associada a dados do ENEM.

Esses conceitos não são equivalentes.

Se o sistema pede uma classificação manual, o signo deve comunicar exatamente o que significa e por que essa informação é necessária.

### 19. Tornar a síntese útil para a Entrega 10

A síntese atual diz apenas:

> “Usaremos todos os objetivos e signos listados acima para o desenvolvimento do MoLIC”.

Isso é insuficiente.

Nem tudo que está na tabela precisa necessariamente aparecer com o mesmo peso no MoLIC.

A síntese deveria identificar:

- quais objetivos finais geram conversas principais;
- quais objetivos instrumentais geram subdiálogos;
- quais signos são indispensáveis para essas conversas;
- quais rupturas precisam de prevenção/recuperação;
- quais elementos são apenas expressão visual e não conceito central da conversa.

Essa seleção ajudará a evitar que o MoLIC vire um diagrama gigantesco tentando representar cada botão e tooltip.

### 20. Atualizar a rastreabilidade com os artefatos da Entrega 09

A coluna “Cenário de interação / signos” da `RASTREABILIDADE.md` continua marcada como `Pendente` nas relações R01–R04.

Isso não corresponde mais ao estado do projeto.

Agora existem:

- CI01;
- CI02;
- CI03;
- O01–O10;
- vários signos conceituais.

A equipe deve atualizar a matriz para conectar necessidades e tarefas aos cenários de interação e signos relevantes.

Essa atualização é especialmente importante antes da Entrega 10, porque o MoLIC precisa nascer de uma cadeia rastreável.

### 21. Resolver identificadores antigos e inconsistências na rastreabilidade

A matriz ainda possui trechos comentados com placeholders e referências antigas.

Também existem identificadores `CO01`, `CO02` e `CO03` para concorrentes e `C01`, `C02`, `C03` para cenários, o que exige cuidado para não voltar à ambiguidade observada em entregas anteriores.

Nesta etapa, a equipe adiciona `CI01`, `CI02`, `CI03`.

A convenção está melhor, mas precisa ser aplicada de maneira uniforme em todos os documentos.

### 22. Revisar o checklist

O checklist marca:

> “O esquema de signos está em uma tabela única e sem duplicações conceituais.”

A tabela única existe, mas ainda há problemas conceituais e excesso de signos de interface.

Também aparece:

> “Mapas individuais foram consolidados” desmarcado, acompanhado do comentário “todos fizeram sua respectiva parte no mapa consolidado”.

Se a solução da equipe foi produzir diretamente um único mapa colaborativo, isso pode ser perfeitamente aceitável para a responsabilidade da atividade. O checklist deve ser adaptado para refletir o que realmente foi feito, em vez de deixar uma instrução contraditória.

## Recomendações de melhoria

### 1. Utilizar os três níveis da teoria como teste de consistência

Para cada elemento, perguntem:

**Objetivo:** o que o usuário quer alcançar?

**Conversa:** o que usuário e sistema precisam comunicar para alcançar esse objetivo?

**Signo:** quais conceitos precisam existir e ter significado compartilhado para essa conversa funcionar?

Só depois perguntem:

**Interface:** qual componente concreto expressará aquele signo?

Essa sequência ajuda a evitar que botão, dropdown e tooltip ocupem o lugar dos conceitos.

### 2. Manter o cenário de interação independente do protótipo atual

O protótipo pode sugerir soluções, mas o cenário de interação deve sobreviver a uma mudança de widget.

Se trocar um dropdown por radio buttons exigir reescrever o cenário, provavelmente o cenário está detalhado demais.

### 3. Usar linguagem do docente nas mensagens de ruptura

Mensagens como “falha ao carregar RoBERTa” podem fazer sentido para o desenvolvedor, mas não para o usuário final.

A interface deve explicar:

- o que aconteceu;
- o que isso impede;
- o que o usuário pode fazer agora.

### 4. Reduzir objetivos redundantes

“Consultar métricas” e “explorar resultados” podem representar objetivos diferentes, mas a equipe precisa demonstrar a diferença.

Se forem apenas etapas da mesma intenção, consolidá-los pode produzir um mapa mais claro.

### 5. Preservar a cautela sobre causalidade

Esse cuidado aparece em CI01 e em alguns signos. Deve ser uma regra transversal do projeto.

A interface não deve comunicar que uma característica estrutural “causou” determinado desempenho quando os dados sustentam apenas associação ou correlação.






A equipe avançou bastante na quantidade e na riqueza do modelo, principalmente no esquema de signos. Agora é preciso tomar cuidado para não confundir **modelo conceitual com catálogo de tela**. O professor não entra no sistema porque deseja “clicar em upload”, “usar um dropdown” ou “escolher um formato”; ele entra porque quer compreender uma avaliação e tomar uma decisão. A interface, os diálogos e os signos existem para sustentar essa intenção. Quando essa hierarquia fica clara, o MoLIC da próxima entrega fica muito mais simples - e muito mais correto.
