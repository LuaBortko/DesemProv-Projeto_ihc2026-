# Feedback do Professor > Entrega 11 > Equipe 05

## Avaliação geral

A equipe apresenta uma Entrega 11 bastante completa do ponto de vista de materialização da interface. Em vez de construir um novo protótipo no Figma, vocês utilizaram telas da própria aplicação de alta fidelidade desenvolvida no TCC. Essa decisão é adequada para esta atividade.

Há um conjunto consistente de telas cobrindo o fluxo principal e diversos estados alternativos: envio da prova, validação do arquivo, preenchimento dos parâmetros, ajuda contextual, configuração de dificuldade, inclusão de métricas dos estudantes, consulta dos resultados, filtros, explicações, exportação e mensagens de erro. A documentação também está acima do mínimo exigido, porque vocês explicaram objetivos, signos, origem no MoLIC, sistema visual e aspectos de acessibilidade.

O ponto forte da entrega é que a interface não apareceu “do nada”. É possível enxergar uma cadeia razoável entre M02 e as telas de upload, M01 e as telas de parametrização, e M03 e as telas de resultados.

Entretanto, a rastreabilidade ainda contém inconsistências importantes herdadas das entregas anteriores. Em alguns pontos, a documentação afirma uma cobertura maior do que aquela efetivamente representada pelas telas. O principal exemplo é O03: na Entrega 09, O03 significa comparar duas provas para verificar discrepâncias de exigência. Essa comparação não está materializada na interface apresentada, embora a tabela “Cobertura MoLIC → Figma” atribua O03 a M01, M02 e M03.

Também existem problemas de comunicação na interface de resultados. Em estados de erro, o sistema expõe termos internos como BERT e RoBERTa e, em uma das telas documentadas, apresenta diretamente um JSON da prova. Para um sistema cujo usuário prioritário é um docente, isso desloca a interface para a perspectiva do desenvolvedor. A aplicação precisa comunicar o efeito do processamento sobre a tarefa do professor, não os detalhes internos da implementação.

A entrega está em bom nível de maturidade visual e funcional. O trabalho agora é principalmente de **alinhamento conceitual, rastreabilidade e refinamento da comunicação da interface**.

## Pontos positivos

- A equipe apresentou 20 screenshots de alta fidelidade da aplicação, permitindo analisar diretamente a interface.
- A opção de utilizar a aplicação do TCC em vez de um novo protótipo Figma está adequadamente explicada.
- F01 representa claramente o ponto de entrada para envio da prova.
- F02 mantém o arquivo selecionado visível e permite cancelamento antes de prosseguir.
- A equipe materializou estados de erro específicos para formato inválido, falha de preparação da prova, tamanho excedido e erro interno.
- F03 apresenta os parâmetros necessários para a análise em uma organização visual clara.
- A ajuda contextual de F03.1 está coerente com a necessidade anteriormente identificada de explicar parâmetros técnicos.
- F03.2, F03.3 e F03.4 mostram estados concretos das opções de configuração, o que favorece a rastreabilidade com M01.
- F03E1 materializa a validação de duração máxima e utiliza mensagem textual associada ao alerta.
- F04 apresenta uma área de resultados organizada em cards, mantendo hierarquia visual consistente.
- A tela de resultados explicita valores como duração total, quantidade de questões e velocidade de leitura considerada, ajudando o usuário a lembrar quais parâmetros deram origem à análise.
- A equipe incluiu explicações textuais junto aos gráficos, em vez de apresentar apenas visualizações isoladas.
- F04.1 demonstra a existência de filtros.
- F04.2 demonstra ajuda contextual sobre os cálculos.
- F04.3 materializa a exportação em diferentes formatos.
- F04.4 apresenta o uso dos acertos reais dos alunos quando esses dados foram fornecidos.
- F04E3 comunica corretamente que a correlação não pode ser mostrada quando os acertos por questão não foram informados e orienta o usuário sobre como obter esse resultado.
- O sistema utiliza texto e cor conjuntamente nos estados de alerta e erro, evitando depender exclusivamente da cor.
- A documentação de sistema visual é detalhada e procura justificar tipografia, paleta, componentes e feedback.
- A equipe registrou preocupações com foco por teclado, alternativa ao drag-and-drop, rótulos ARIA e redimensionamento.
- A entrega distingue explicitamente alguns estados simulados, o que é uma boa prática para não confundir protótipo/interface com funcionalidade técnica efetivamente disponível.
- Existe uma tentativa explícita de relacionar cada tela às cenas MoLIC correspondentes.

## Correções prioritárias

### 1. Corrigir a cobertura de O03: a interface apresentada não materializa a comparação entre duas provas

Na Entrega 09, O03 está definido como:

> analisar duas provas para verificar se não há discrepâncias de exigência.

Na Entrega 11, entretanto, a tabela “Cobertura MoLIC → Figma” registra O03 em M01, M02 e M03.

As telas apresentadas não mostram um fluxo de comparação entre duas provas.

O conjunto atual materializa:

- envio de uma prova;
- informação de parâmetros;
- processamento;
- consulta de resultados de uma prova;
- filtros;
- exportação.

Isso não é o mesmo que comparar duas avaliações.

A equipe já havia indicado na Entrega 10 que a comparação automática talvez não permanecesse no escopo. Se essa decisão foi mantida, agora ela precisa ser formalizada: retirem O03 da cobertura das telas que não o implementam, atualizem a Entrega 09 e registrem a mudança na rastreabilidade.

Se O03 continuar no escopo, então precisa existir um fluxo de interface que permita selecionar/obter duas análises e compará-las.

Atualmente, a documentação declara uma cobertura que o protótipo não demonstra.

### 2. Corrigir a tabela “Cobertura MoLIC → Figma” para refletir os objetivos reais de cada MoLIC

Na Entrega 10:

- M01 foi definido para O05 - informar os dados necessários para a análise;
- M02 foi definido para O04 - enviar a avaliação em PDF;
- M03 deveria estar relacionado principalmente aos objetivos de consultar, explorar e compreender resultados, embora tenha sido incorretamente registrado como O03.

Na Entrega 11, entretanto:

- M01 aparece cobrindo O01, O02, O03 e O05;
- M02 aparece cobrindo O01, O02, O03 e O04;
- M03 aparece cobrindo O01, O02 e O03.

Isso mistura **objetivos finais dos cenários** com **objetivos instrumentais diretamente modelados pelos MoLICs**.

Uma tela pode contribuir para O01 ou O02, mas isso não significa que cada MoLIC individual “modela” integralmente esses objetivos.

A equipe deve separar duas ideias:

1. **objetivo diretamente modelado pela conversa**, por exemplo O04 ou O05;
2. **objetivo final para o qual essa conversa contribui**, por exemplo analisar uma prova antes de aplicá-la.

Essa distinção deixará a cobertura muito mais confiável.

### 3. A `RASTREABILIDADE.md` usa F01–F04 com significados diferentes da Entrega 11

Este é um problema importante.

Na Entrega 11:

- F01 = tela principal de upload;
- F02 = arquivo válido enviado;
- F03 = informar dados da prova;
- F04 = resultados da análise.

Porém, na seção “Rastreabilidade de padrões de interface”:

- F01 = dashboard;
- F02 = upload;
- F03 = detalhamento pós-processamento;
- F04 = exportação/download.

Os mesmos IDs estão representando coisas diferentes.

Isso inviabiliza a função principal da rastreabilidade. Se alguém lê “F01”, precisa saber exatamente qual artefato está sendo citado.

Antes das avaliações das próximas entregas, escolham uma única convenção e atualizem todas as referências.

Não criem uma segunda semântica para o mesmo identificador.

### 4. A tabela principal de rastreabilidade está estruturalmente desalinhada

A tabela possui as colunas:

- MoLIC;
- Tela(s) Figma;
- Heurística/problema;
- Tarefa no teste;
- Decisão/melhoria.

Entretanto, nas linhas R01–R04, depois das telas aparecem diretamente `UT01 e UT02`.

Isso coloca tarefas de teste na coluna destinada às violações heurísticas e desloca a decisão para a coluna seguinte.

Como resultado, as linhas não representam corretamente a cadeia prevista pelo cabeçalho.

Isso precisa ser corrigido antes das Entregas 12, 13 e 14, porque a matriz deverá relacionar:

**modelo → tela → problema heurístico → tarefa de teste → decisão de melhoria.**

### 5. F04 está documentada com o objetivo errado

A tela F04 é “Ver estatísticas da avaliação”.

Entretanto, o documento registra:

> Objetivo do usuário: Iniciar a análise da prova.

Nesse momento, a análise já foi iniciada e os resultados já estão sendo apresentados.

O objetivo da tela está relacionado a consultar, compreender e interpretar os resultados.

Essa diferença importa porque o catálogo de telas deveria explicar **por que aquela tela existe**, e não apenas repetir uma ação anterior do fluxo.

### 6. F01 também está descrita como ação de interface, e não como objetivo do usuário

Em F01 consta:

> Objetivo do usuário: Anexar um arquivo na tela.

“Anexar um arquivo” descreve uma ação da interface.

O objetivo instrumental é mais amplo: submeter/enviar uma avaliação para que ela possa ser analisada.

Essa distinção já apareceu em entregas anteriores e precisa ser mantida agora.

A interface pode usar upload, drag-and-drop ou outro mecanismo; o objetivo do usuário não deveria depender do widget utilizado.

### 7. O sistema continua expondo BERT e RoBERTa ao professor

Nas telas F04E1 e F04E2 aparecem mensagens como:

> Erro ao inicializar o modelo BERT

e

> Erro ao inicializar o modelo RoBERTa.

Esse problema já havia sido apontado no modelo conceitual e no MoLIC.

BERT e RoBERTa são detalhes internos da implementação.

Para o usuário docente, a informação relevante é:

- qual parte da análise não pôde ser realizada;
- que impacto isso possui sobre os resultados;
- se ele pode continuar usando as demais métricas;
- o que pode fazer para tentar recuperar a operação.

A mensagem já explica parcialmente o impacto, o que é positivo, mas o título continua sendo orientado à arquitetura interna.

Sugiro que vocês tratem o nome do modelo como informação técnica secundária, se realmente houver necessidade de apresentá-lo, e priorizem a linguagem da tarefa.

### 8. F04E1 expõe o JSON bruto da prova

Na tela F04E1, abaixo da mensagem de erro, a interface apresenta uma seção chamada:

> JSON da prova

com a estrutura interna dos dados.

Para o usuário prioritário definido pelo projeto, isso é um forte vazamento de detalhe de implementação.

O professor não deveria precisar interpretar chaves, listas ou estrutura JSON para compreender sua avaliação.

Se essa informação foi incluída para debug do desenvolvimento, ela não deveria permanecer na interface final destinada ao docente.

Se existir alguma necessidade real de apresentar os dados extraídos, criem uma representação orientada ao domínio:

- questões identificadas;
- alternativas;
- dificuldade informada;
- acertos;
- quantidade de palavras;
- outras informações relevantes.

Não apresentem a estrutura serializada do backend como conteúdo da interface de uso.

### 9. A origem de F04.3 está associada à cena errada do MoLIC

F04.3 representa:

> Usuário quer exportar o relatório da prova.

Porém, a origem está registrada como:

> M03 / cena de Consultar métricas da prova.

No próprio M03 existe uma cena específica de exportação.

Portanto, a tela deveria apontar para a conversa de exportar arquivo/resultados, e não para a cena genérica de consulta.

Esse tipo de ajuste é pequeno visualmente, mas importante para demonstrar que o protótipo realmente foi derivado do modelo.

### 10. A interface não evidencia no catálogo um estado de processamento entre “Iniciar Análise” e os resultados

A Entrega 11 documenta vários erros e estados alternativos, o que é muito positivo.

Entretanto, entre o acionamento de “Iniciar Análise” em F03 e a apresentação dos resultados em F04, o catálogo não mostra um estado específico de processamento/carregamento.

Esse é um momento relevante porque a análise envolve processamento textual e modelos computacionais que podem demandar algum tempo.

Se a resposta não for instantânea, o usuário precisa saber que:

- a solicitação foi recebida;
- o sistema está trabalhando;
- o processamento ainda não terminou;
- eventualmente é possível aguardar, cancelar ou tentar novamente.

Se a aplicação já apresenta esse feedback, ele deve ser documentado no catálogo. Se não apresenta, é uma oportunidade clara de melhoria.

### 11. O checklist declara cobertura integral dos MoLICs, mas isso ainda não está demonstrado

O checklist marca:

> Todos os MoLIC relevantes estão cobertos.

Isso é parcialmente verdadeiro para M01, M02 e o núcleo de M03.

Porém:

- O03/comparação entre provas continua sem materialização;
- a exportação está documentada com origem imprecisa;
- alguns estados de processamento não aparecem;
- a semântica de M03 já havia sido apontada como problemática na Entrega 10.

Portanto, a equipe precisa revisar o checklist depois de corrigir as inconsistências.

Checklist não deve funcionar como declaração de intenção; deve refletir aquilo que o artefato efetivamente comprova.

### 12. A rastreabilidade amplia CI01, CI02 e CI03 para praticamente todas as telas sem demonstrar as diferenças entre os cenários

R01–R04 vinculam CI01, CI02 e CI03 aos mesmos conjuntos de telas.

Porém, os três cenários possuem motivações diferentes:

- CI01: análise após desempenho abaixo do esperado;
- CI02: revisão preventiva antes da aplicação;
- CI03: comparação entre versões.

A interface apresentada possui um fluxo genérico muito adequado para CI01 e CI02.

CI03 exige uma conversa adicional de comparação que não aparece.

Além disso, se CI01 envolve análise posterior ao desempenho dos alunos, o uso dos acertos reais deveria estar claramente relacionado a esse cenário.

A equipe precisa aproveitar a rastreabilidade para mostrar essas diferenças, e não apenas repetir `CI01, CI02 e CI03` em todas as linhas.

### 13. A interface materializa adequadamente a inclusão opcional dos acertos dos estudantes, mas a relação com CI01 precisa ficar mais explícita

F03.4 e F04.4 são bons exemplos de continuidade do projeto.

Quando o docente informa quantidade de participantes e acertos por questão, o sistema consegue apresentar análises relacionadas ao desempenho real daquela turma.

Isso ajuda a resolver uma dúvida conceitual que aparecia na Entrega 09: como o sistema poderia relacionar as características estruturais da prova ao desempenho observado?

Agora existe uma resposta concreta de interface.

A equipe deve registrar isso explicitamente na rastreabilidade:

**CI01 → informar métricas reais → F03.4 → análise/correlação em F04.4.**

Essa cadeia é muito mais útil do que simplesmente dizer que F03/F04 servem para todos os cenários.

### 14. Rever a alegação de acessibilidade quando ela depender de implementação não demonstrada pelas imagens

A seção de acessibilidade está bem elaborada e considera aspectos relevantes:

- contraste;
- reflow;
- tamanho de alvo;
- teclado;
- foco;
- ARIA;
- mensagens de erro.

Entretanto, screenshots permitem verificar visualmente apenas parte dessas afirmações.

Propriedades como:

- `aria-label`;
- ordem de foco;
- navegação completa por teclado;
- comportamento em zoom acima de 200%;
- ausência de perda de conteúdo;
- comportamento real de leitores de tela

dependem da implementação e de teste.

Não há problema em declarar que foram implementadas, mas, para uma afirmação forte de conformidade, a equipe deve conseguir demonstrá-las em avaliação ou inspeção.

Na Entrega 11, tratem essas afirmações como características implementadas/verificações realizadas, sem transformar isso automaticamente em certificação de conformidade WCAG AA.

### 15. Rever a frase de contraste “validada” e manter evidência quando houver números específicos

A equipe registra razões específicas, como:

- 12,6:1;
- 5,7:1;
- 5,1:1;
- 5,0:1.

É bom que a escolha de cores tenha sido analisada quantitativamente.

Porém, quando números exatos são apresentados, é interessante manter a ferramenta, procedimento ou registro usado para obtê-los.

Isso aumenta a verificabilidade e facilita a avaliação posterior.

### 16. Melhorar a comunicação de sucesso e conclusão do fluxo

A documentação informa explicitamente:

> “Sucesso: não há mensagem de sucesso no MVP, quando é sucesso apenas continua/habilita o fluxo feliz”.

Isso pode funcionar em algumas transições, mas merece reflexão.

Em operações importantes, principalmente upload e conclusão do processamento, o usuário precisa perceber claramente que sua ação foi aceita.

A mudança de estado pode ser feedback suficiente quando for muito evidente.

Porém, o projeto deve avaliar se o professor consegue distinguir:

- arquivo apenas selecionado;
- arquivo validado;
- processamento iniciado;
- processamento concluído;
- resultados disponíveis.

Essa questão pode ser verificada nas próximas avaliações.

## Recomendações de melhoria

### 1. Preservar o nível de documentação desta entrega

A descrição de cada estado com objetivo, signos e origem é uma boa prática e deve ser mantida.

O problema não está na quantidade de documentação, e sim em algumas relações incorretas.

Corrijam a semântica sem empobrecer o material.

### 2. Organizar os resultados prioritariamente pelo raciocínio do docente

A tela de resultados possui muitos blocos e métricas.

Na avaliação, observem se o professor consegue responder rapidamente perguntas como:

- existe alguma característica da prova que merece atenção?
- qual questão é mais problemática?
- que informação é apenas descritiva?
- o que pode indicar necessidade de revisão?
- o sistema está mostrando associação ou causalidade?

A interface não deve apenas “mostrar todas as métricas”; ela deve apoiar uma decisão.

### 3. Manter explicações junto aos gráficos, mas evitar transformar tooltip em manual técnico

Os textos explicativos são positivos.

O próximo cuidado é garantir que o professor não precise compreender detalhes estatísticos ou computacionais desnecessários para usar a informação.

A explicação deve responder principalmente:

**o que estou vendo, por que isso importa e o que posso ou não concluir?**

### 4. Diferenciar claramente alerta, indisponibilidade parcial e erro bloqueante

As telas já possuem boa estrutura visual para alertas.

Agora vale classificar melhor os estados:

- erro que impede toda a análise;
- erro que deixa apenas uma métrica indisponível;
- dado opcional não informado;
- alerta de valor inadequado;
- falha temporária recuperável.

Essas categorias não deveriam parecer equivalentes.

### 5. Validar em uso real a densidade da página de resultados

A página F04 é extensa e possui diversos gráficos.

Isso não é necessariamente um problema; sistemas analíticos podem exigir densidade informacional.

Porém, a avaliação deve investigar se o docente:

- encontra a informação desejada;
- entende a hierarquia;
- percebe filtros e ajuda;
- não se perde em uma página longa;
- identifica rapidamente os pontos de atenção.

## Pontos que devem alimentar as próximas entregas

- **Entrega 12:** as tarefas de avaliação precisam usar o fluxo real F01 → F02 → F03 → F04 e seus estados alternativos.
- **Entrega 12:** inclua perguntas específicas sobre compreensão das métricas e capacidade de decidir o que revisar na prova.
- **Entrega 12:** inclua avaliação dos estados de erro e recuperação, principalmente upload inválido, falha no processamento e ausência de acertos dos alunos.
- **Entrega 12:** se BERT/RoBERTa permanecerem visíveis, avaliem explicitamente se esses termos são compreensíveis e úteis ao professor.
- **Entrega 12:** decidam se JSON bruto realmente pertence à interface destinada ao docente.
- **Entrega 13:** a avaliação heurística deverá inspecionar não apenas as telas felizes, mas F02E1–F02E4, F03E1 e F04E1–F04E3.
- **Entrega 13:** atenção especial às heurísticas de correspondência com o mundo real, visibilidade do estado do sistema, prevenção de erros e recuperação de erros.
- **Entrega 14:** observem se os participantes entendem quando fornecer métricas reais dos estudantes e o benefício obtido em F04.4.
- **Entrega 14:** observem se os usuários compreendem as limitações dos resultados e não interpretam correlação como causalidade.
- **Rastreabilidade:** estabilizar definitivamente os IDs F01–F04 antes de qualquer nova avaliação.
- **Rastreabilidade:** corrigir o deslocamento das colunas de heurística, tarefa de teste e decisão.
- **Escopo:** resolver definitivamente O03/CI03 antes que as avaliações sejam executadas.

## Síntese das ações recomendadas

1. **Corrigir a cobertura de O03**, porque a comparação entre duas provas não está materializada nas telas apresentadas.
2. **Reescrever a tabela MoLIC → telas** diferenciando objetivo diretamente modelado de objetivo final apoiado.
3. **Estabilizar os IDs F01–F04** na `RASTREABILIDADE.md` e na Entrega 11.
4. **Corrigir o desalinhamento das colunas da matriz de rastreabilidade.**
5. **Corrigir o objetivo registrado para F04**, que é consultar/interpretar resultados, e não iniciar análise.
6. **Reformular o objetivo de F01** para representar a intenção do usuário, e não apenas o gesto de anexar.
7. **Retirar ou rebaixar BERT/RoBERTa da linguagem principal destinada ao professor.**
8. **Retirar o JSON bruto da interface de uso**, caso ele seja apenas elemento de debug.
9. **Relacionar F04.3 à cena específica de exportação de M03.**
10. **Materializar/documentar o estado de processamento** entre F03 e F04 quando houver espera perceptível.
11. **Revisar o checklist** após corrigir a cobertura efetiva dos MoLICs.
12. **Registrar explicitamente a cadeia CI01 → métricas reais → F03.4 → F04.4.**
13. **Tratar declarações de acessibilidade como características verificáveis**, preservando evidência para aquilo que não pode ser demonstrado apenas por screenshot.
14. **Usar as Entregas 12–14 para verificar se a quantidade de informação da tela de resultados realmente ajuda o docente a tomar decisão.**

Esta é uma das entregas em que a aplicação começa a ficar muito mais concreta. A interface está visualmente organizada, há preocupação real com erros, ajuda e acessibilidade, e vocês documentaram bem o que foi construído. O próximo cuidado é não deixar a implementação correr mais rápido do que o modelo conceitual: se F01 significa upload aqui, não pode significar dashboard na rastreabilidade; se O03 significa comparar provas, não podemos dizer que uma tela de upload “cobre O03”; e se o usuário é professor, ele não deveria precisar conversar com BERT, RoBERTa ou JSON para entender o que aconteceu. 🙂
