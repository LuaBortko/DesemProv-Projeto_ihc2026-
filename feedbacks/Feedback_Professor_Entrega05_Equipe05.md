# Feedback do Professor > Entrega 05 > Equipe 05

## Avaliação geral

A equipe cumpriu quantitativamente a responsabilidade mínima da Entrega 05. O grupo possui três integrantes e cada integrante apresentou um HTA, um GOMS e um CTT, totalizando nove modelos: T01 - Analisar a prova, de Beatriz; T02 - Analisar histórico de provas, de Luana; e T03 - Gerar novas questões baseadas em provas já elaboradas, de Nuno.

Os seis diagramas de HTA e CTT estão acessíveis e legíveis. Também há descrição textual para os modelos, tabelas auxiliares dos HTAs e legendas para os CTTs. Os HTAs, de modo geral, já apresentam uma estrutura hierárquica e não foram desenhados como simples fluxogramas. Nos três diagramas, os objetivos decompostos possuem dois ou mais filhos e as operações-folha são visualmente diferenciadas por sublinhado, o que preserva dois requisitos importantes da técnica.

A equipe também demonstra esforço de revisão. Existem versões corrigidas de T01, histórico de alterações e comentários internos indicando que vários aspectos formais foram revisitados. Isso produziu avanços concretos, principalmente no HTA e no CTT de T01.

Entretanto, ainda existem problemas importantes de formalismo nas três técnicas. Nos HTAs, a tabela auxiliar ainda mistura plano, ação e feedback em níveis onde esses elementos não deveriam aparecer. No GOMS, a principal dificuldade é estrutural: o leitor ainda não consegue enxergar de maneira uniforme e inequívoca a hierarquia `GOAL 0 → GOAL → METHOD/SELECTION RULE → operadores`, e alguns conjuntos de operadores terminam sem uma verificação interna do resultado. Nos CTTs, há algumas classificações e relações contraditórias e T02 não apresenta, antes da interação, uma tarefa externa do usuário que motive o uso do sistema.

Há ainda uma questão mais séria de continuidade do projeto: T02 e principalmente T03 introduzem tarefas que não derivam claramente dos cenários anteriores. T03, em particular, foi ligado a C03, mas C03 tratava da comparação entre versões de avaliações; ele não estabelecia como objetivo gerar novas questões automaticamente. A modelagem de tarefas não deve criar silenciosamente novas funcionalidades para depois justificá-las com o próprio diagrama.

Antes de usar esta entrega como base para prototipação, a equipe precisa corrigir o formalismo dos modelos e estabilizar quais tarefas realmente pertencem ao escopo do projeto.

## Pontos positivos

- A quantidade mínima foi atendida integralmente: cada um dos três integrantes produziu HTA, GOMS e CTT.
- Todos os artefatos possuem autoria identificada.
- Os diagramas de HTA e CTT estão legíveis e puderam ser analisados.
- Os três HTAs possuem uma tarefa 0 e realizam decomposição hierárquica.
- Nos HTAs, os nós decompostos possuem pelo menos dois filhos; não encontrei decomposição com apenas um filho.
- As operações-folha dos HTAs são representadas com sublinhado, distinguindo-as visualmente dos objetivos decompostos.
- Os três HTAs utilizam operadores de plano como sequência (`>`), alternativa (`/`) e paralelismo (`+`).
- T01 possui uma tabela auxiliar bastante mais completa do que uma simples repetição do diagrama e registra Input, Feedback e Plano no objetivo 0.
- T02 também apresenta Input e Feedback no objetivo 0 e descreve decisões de design associadas às subtarefas.
- O GOMS de T02 é o modelo mais próximo do formalismo esperado: apresenta GOAL 0, goals subsequentes, métodos alternativos, regras de seleção e operadores com atividades de exame/verificação ao final.
- Os CTTs utilizam diferentes tipos de tarefa - usuário, sistema, interação e abstração - e vários operadores temporais da técnica.
- T01 e T03 possuem uma tarefa externa do usuário antes da entrada efetiva no sistema: preparar a prova.
- Os três CTTs apresentam pelo menos uma tarefa de processamento do sistema.
- T01 mantém boa aderência ao objetivo central do projeto: preparar/enviar uma avaliação, fornecer informações necessárias e interpretar os resultados da análise.

## Correções prioritárias

### 1. Revisar a origem de T02 e T03 antes de corrigir os diagramas

A primeira pergunta da Entrega 05 não deveria ser “o diagrama está bonito?”, mas “esta tarefa realmente deriva do problema que já foi modelado?”.

T01 - **Analisar a prova** - possui boa continuidade com o projeto e com o cenário preventivo de revisão da avaliação antes da aplicação.

T02 - **Analisar histórico de provas** - já representa uma ampliação. C01 tratava de uma docente que, depois de obter um resultado abaixo do esperado, procurava compreender se características estruturais da avaliação poderiam ter contribuído para esse resultado. Isso não estabelece automaticamente a necessidade de possuir um histórico de provas armazenadas, filtros, comparação longitudinal e consulta posterior.

T03 apresenta uma ruptura ainda maior. Na Entrega 04, C03 descrevia Vera comparando duas versões de uma avaliação para identificar possíveis diferenças estruturais antes da aplicação. Na Entrega 05, essa origem foi transformada em **“Gerar novas questões baseadas em provas já elaboradas”**, incluindo geração automática, seleção de dificuldade, edição e exportação.

Esse objetivo não é equivalente ao objetivo do cenário.

A equipe precisa decidir uma das duas coisas:

- voltar a modelar a tarefa efetivamente derivada do cenário; ou
- assumir explicitamente uma mudança/ampliação de escopo, registrar a hipótese/evidência que motivou essa mudança e atualizar cenários e rastreabilidade.

Não utilizem a análise de tarefas para inventar funcionalidades que os artefatos anteriores ainda não justificaram.

### 2. Corrigir os planos nas tabelas auxiliares dos HTAs

Nos diagramas, os planos estão em geral representados de forma compreensível. O problema aparece principalmente na tabela auxiliar.

Um **plano existe em um objetivo que foi decomposto** e deve indicar como seus filhos se relacionam. Portanto, uma operação-folha não precisa de plano, pois não possui filhos.

Em T01, por exemplo, as operações `1.1.1`, `1.1.2`, `2.1`, `2.2`, `3.1`, `3.2`, `4.1`, `4.2` e `4.3` são folhas. Mesmo assim, várias delas possuem na coluna de plano explicações como “pode ser feito 1.1.1 ou 1.1.2” ou “o 3.1 deve ser feito em paralelo ao 3.2”. Essas relações pertencem ao **plano do pai**, não ao plano da folha.

O mesmo ocorre em T02, em operações como `1.1`, `1.2`, `2.1`, `2.2.1`, `2.2.2`, `3.1` e `3.2`.

A equipe deve deixar o plano somente nos nós decompostos e registrar as relações entre filhos no respectivo pai.

Um teste simples: **se o nó não possui filhos no diagrama, ele não possui um plano de decomposição**.

### 3. Manter Input e Feedback exclusivamente no objetivo 0 do HTA

A tabela auxiliar do HTA possui uma regra importante: o objetivo 0 precisa registrar Input, Feedback e Plano. Nos demais níveis, Input e Feedback não devem aparecer como se cada subtarefa reiniciasse o modelo.

T01 está mais próximo desse padrão, pois concentra Input e Feedback no objetivo 0 e usa majoritariamente recomendações nos demais níveis.

T02 ainda contém, em `2.2.1`, um campo explicitamente chamado **Feedback**.

T03 apresenta o problema com maior frequência. Há Feedback em `1.1`, `1.2`, `2`, `3.2`, `4.1` e `4.2`.

Esses conteúdos não precisam ser perdidos. Devem ser reclassificados.

Se a intenção é representar algo que a interface deverá mostrar, registrem como **ação** ou **recomendação de interação**, conforme o caso. Se for um problema de design, registrem como problema/recomendação. O campo Feedback, no formalismo desta atividade, deve permanecer associado ao fechamento da tarefa 0.

### 4. Corrigir a inconsistência interna do HTA de T03

O HTA de T03 possui divergências entre diagrama e tabela.

No diagrama, o plano do objetivo 0 aparece como:

`1 > 2 > 3`

porém o objetivo 0 possui também o filho `4 - Exportar novas questões`, e a própria tabela informa:

`1 > 2 > 3 > 4`.

O diagrama e a tabela precisam expressar o mesmo plano.

Há também um problema na tabela da tarefa 2. O item `2.2` é descrito como “Sub objetivo - Gerar novas questões”, mas aparece no diagrama como uma operação-folha equivalente a “Disparar geração”. Além disso, seu plano é registrado como `2.1 + 2.2`, isto é, o nó aparece utilizando a si próprio dentro do próprio plano.

Isso precisa ser refeito. O pai deve possuir o plano que relaciona seus filhos; uma folha não pode possuir um plano que se referencia.

### 5. Ajustar o uso de paralelismo no HTA

O operador `+` representa que mais de um subobjetivo precisa ser atingido em paralelo.

Em T01, o plano `3.1 + 3.2` declara que visualizar gráficos/tabelas e ler o detalhamento das métricas são realizados em paralelo. A justificativa textual, porém, diz que “ambos precisam ser atingidos ao mesmo tempo”.

A equipe precisa verificar se isso corresponde realmente à atividade humana. Um docente pode observar o gráfico e depois consultar a explicação, ou alternar entre ambos. Se não houver simultaneidade efetiva, o `+` não é o operador adequado.

O mesmo cuidado vale para T03, em `2.1 + 2.2` e `3.1 + 3.2`. Selecionar uma quantidade e depois disparar a geração, por exemplo, tende a representar sequência, não paralelismo.

Não escolham o operador porque ele “deixa o modelo mais completo”. O operador deve representar a relação real entre as subtarefas.

### 6. Reestruturar o GOMS de T01

T01 possui GOAL 0, mas o primeiro goal não está estruturado corretamente para uma tarefa que possui duas maneiras alternativas de ser realizada.

O documento apresenta:

- `GOAL 1.A (SUBGOAL1): Arrastar arquivo`
- `GOAL 1.B (SUBGOAL2): Selecionar arquivo no explorador`

Entretanto, essas duas alternativas são justamente **dois métodos para atingir o mesmo GOAL “Fazer upload de prova”**.

A estrutura conceitual esperada deveria permitir enxergar:

`GOAL 0`
→ `GOAL 1`
→ `METHOD 1.A`
→ `SELECTION RULE`
→ operadores
→ `METHOD 1.B`
→ `SELECTION RULE`
→ operadores

O atual T01 chama de GOAL aquilo que deveria ser método.

Além disso, `GOAL 1.C - Enviar arquivo` aparece como outro subgoal depois das duas alternativas. A equipe deve decidir se “enviar” é um goal comum que ocorre depois de qualquer método de seleção ou se faz parte dos próprios métodos. O importante é que a hierarquia fique inequívoca.

### 7. Revisar o GOMS de T01 no GOAL 3

No GOAL 3, a equipe define:

- Method 3.A - leitura visual do dashboard;
- Method 3.B - leitura do detalhamento das métricas.

Mas não está claro que esses sejam métodos alternativos para atingir a mesma meta.

Se o professor pode e deve utilizar **ambas as formas de leitura**, elas são subgoals ou etapas complementares, e não dois métodos mutuamente selecionados.

Além disso, apenas o Method 3.A possui regra de seleção explícita. O Method 3.B não possui uma regra equivalente.

A equipe precisa decidir: são duas maneiras alternativas de compreender a informação ou são duas etapas/complementos da mesma tarefa? O GOMS deve representar essa decisão corretamente.

### 8. Organizar todos os GOMS como texto hierárquico indentado

O GOMS não deve ser tratado como diagrama, mas também não deve ficar espalhado em títulos independentes que escondem a hierarquia.

T01 e T02 usam várias seções `### Goal`, o que dificulta enxergar claramente que G1, G2 e G3 pertencem a GOAL 0.

T03 contém uma versão indentada no início, mas logo depois repete todo o modelo em outra estrutura. Há ainda texto residual do template:

- `Method M1`
- `O`
- `Method M2: {{...}}`
- `Selection Rule SR1: ...`

A versão final deve existir **uma única vez**, limpa, indentada e organizada.

O leitor precisa enxergar a árvore conceitual do GOMS apenas lendo o texto.

### 9. Garantir verificação interna ao final dos conjuntos de operadores

Um conjunto de operadores não deve terminar apenas com uma ação externa. O último passo deve permitir ao usuário perceber ou verificar que o objetivo foi alcançado.

T02 faz isso melhor. Exemplos:

- examinar resultados filtrados;
- verificar correspondência estrutural;
- decidir se o resumo foi suficiente;
- examinar gráficos e diferenças.

T01 também possui bons exemplos, como verificar que o arquivo foi anexado e verificar a formatação do arquivo exportado.

T03, porém, apresenta vários conjuntos sem essa verificação:

- Method 1.A termina em `Clicar no botão "enviar"`;
- Method 1.B também termina no envio;
- GOAL 2 termina em `Clicar no botão "Gerar novas questões"`;
- Method 3.B termina em `Clicar em "Salvar"`.

É necessário acrescentar uma primitiva interna final: perceber, conferir, examinar ou verificar o resultado da ação antes de considerar aquele método concluído.

### 10. Preservar o que está correto no GOMS de T02 e melhorar apenas a apresentação

Entre os três modelos, T02 é o GOMS mais consistente.

Há GOAL 0, três goals, métodos alternativos com regras de seleção e operadores que normalmente terminam em exame ou decisão.

A correção principal é estrutural: apresentar explicitamente a indentação que liga G1, G2 e G3 ao GOAL 0 e padronizar a nomenclatura `GOAL`, `METHOD`, `SELECTION RULE` e `OP`.

Não é necessário criar métodos artificiais onde existe apenas uma sequência de passos. Se um goal possui apenas uma forma de execução, ele pode ser decomposto em subgoals e operadores sem inventar uma “regra de seleção” inexistente.

### 11. Corrigir contradições no CTT de T01

O CTT de T01 possui boa cobertura de tipos de tarefa e começa corretamente com uma tarefa de usuário externa - `TU1 Preparar a prova` - antes da interação com a plataforma. Também possui processamento do sistema, como `TS1 Gerar dashboard` e `TS2 Gerar arquivo`.

Entretanto, a documentação possui contradições.

Na descrição, T2 é inicialmente chamada de **tarefa interativa**, mas logo depois é descrita como **tarefa abstrata**. No diagrama, T2 está representada como nuvem, portanto é abstrata. O texto deve seguir o diagrama.

Há também uma contradição nas exportações. A legenda usa:

`T4.1 [] T4.2 [] T4.3`

para dizer que os formatos são alternativas de escolha, mas depois também usa:

`T4.1 |=| T4.2 |=| T4.3`

como exemplo de tarefas independentes.

As mesmas tarefas não devem representar simultaneamente “escolha exclusiva” e “independência de ordem” no mesmo nível do modelo. A equipe precisa decidir qual comportamento deseja representar.

### 12. Revisar a classificação de feedback no CTT de T01

Algumas tarefas classificadas como “tarefa do sistema” também incluem apresentação direta de informação ao usuário.

Por exemplo:

- `TS_Erro - Emitir alerta`;
- `TS_Feedback - Validar dados e exibir feedback`.

Uma tarefa do sistema é processamento interno sem interação direta. Quando existe exibição de mensagem, alerta ou feedback ao usuário, há uma parte interativa.

A equipe pode separar o processamento interno da apresentação do resultado ou escolher uma classificação coerente com o que efetivamente está sendo representado.

O importante é não juntar “validar internamente” e “mostrar feedback ao usuário” como se fossem exatamente o mesmo tipo de tarefa.

### 13. Inserir no CTT de T02 uma tarefa externa que motive o uso do sistema

T02 possui tarefas de usuário, tarefas de interação, tarefas de sistema e tarefas abstratas. Também possui processamento do sistema, como aplicar filtros e gerar comparações.

O que está ausente é uma **tarefa externa anterior que explique por que o docente resolveu entrar no sistema**.

O modelo começa diretamente em “Localizar prova no histórico”.

É necessário representar uma ação ou situação do trabalho real do professor que motive essa entrada: por exemplo, uma necessidade de revisar planejamento, comparar avaliações ou investigar um resultado. A equipe deve escolher a situação que efetivamente deriva do cenário e representá-la como tarefa de usuário fora do sistema.

Esse elemento é importante porque o CTT não deve representar apenas “o que acontece dentro da aplicação”; ele deve situar a interação dentro da atividade humana.

### 14. Revisar a coerência entre o CTT de T02 e sua origem

Antes de acrescentar a tarefa externa exigida no item anterior, a equipe precisa resolver a origem de T02.

Se T02 permanecer ligada ao C01, a tarefa externa inicial deve fazer sentido naquele cenário: Maria observa uma situação que a motiva a investigar uma avaliação.

Se a equipe optar por manter uma funcionalidade de histórico e comparação longitudinal, deve primeiro explicar por que essa atividade pertence ao problema e atualizar o cenário/rastreabilidade.

Não criem uma tarefa externa artificial apenas para “passar no requisito do CTT”. Ela precisa existir no trabalho do usuário.

### 15. Revisar identificadores e relações no CTT de T03

O CTT de T03 possui os elementos fundamentais: tarefa externa (`TU1`), tarefas interativas, processamento do sistema, tarefas abstratas e relações temporais.

Porém, a descrição e a legenda apresentam inconsistências de identificadores.

A narrativa menciona TU2/TU3 de formas diferentes, e a legenda apresenta exemplos que nem sempre correspondem exatamente aos identificadores visíveis no diagrama. Também aparece `T5` como exemplo de tarefa abstrata de exportação, embora o diagrama utilize `T4`.

Esses detalhes precisam ser corrigidos porque, em uma modelagem formal, o identificador é parte da semântica do modelo.

### 16. Atualizar a rastreabilidade para apontar apenas para os artefatos atuais

A matriz melhorou em relação às entregas anteriores e já registra T01 e T03 em várias relações.

Entretanto, há referências misturadas entre versões antigas e corrigidas de T01.

R01 aponta para:

`hta_t01_correcao.jpeg` e `ctt_t01_correcao.jpeg`

mas R02, R03 e R04 continuam apontando para:

`hta_t01.jpeg` e `ctt_t01.jpeg`.

Se as versões `_correcao` são as vigentes, a rastreabilidade precisa apontar para elas em todos os registros relacionados.

Além disso, T02 não aparece efetivamente relacionada às necessidades na matriz, apesar de estar declarada como tarefa relevante na Entrega 05.

Por fim, T03 aparece associada ao upload/processamento, mas a matriz não demonstra de onde surgiu a necessidade de **gerar novas questões**.

A rastreabilidade deve explicar a origem da tarefa, e não apenas listar seu arquivo.

### 17. Não declarar o checklist como concluído antes de corrigir o formalismo

O checklist marca como atendidos:

- “GOMS distingue Goals, Operators, Methods e Selection Rules”;
- “CTT usa operadores temporais e tipos de tarefa coerentes”;
- “Tarefas estão ligadas a cenários/personas na rastreabilidade”.

Essas afirmações ainda precisam de ressalvas.

Os componentes do GOMS estão presentes, mas T01 utiliza GOAL no lugar de METHOD em uma parte importante e T03 possui duplicação/estrutura residual.

Os CTTs utilizam a notação, mas T01 contém relações contraditórias para a exportação e T02 não possui a tarefa externa inicial.

A rastreabilidade também ainda não justifica adequadamente T02 e T03.

O checklist deve refletir a situação real do artefato.

## Recomendações de melhoria

### 1. Limpar comentários internos antes da versão final

O arquivo possui muitos comentários HTML de discussão da equipe, lembretes, dúvidas, rascunhos e observações de aula.

Esse material pode ser útil durante o desenvolvimento, mas a versão entregue deve separar o documento final das anotações de trabalho. Atualmente, há trechos que tornam difícil identificar o que é modelo válido e o que era apenas uma hipótese discutida pelo grupo.

### 2. Padronizar terminologia e códigos

Utilizem uma única convenção:

- `GOAL 0`, `GOAL 1`;
- `METHOD 1.A`;
- `SELECTION RULE`;
- `OP. 1.A.1`.

Evitem misturar `G0`, `Goal 0`, `GOAL`, `SUBGOAL`, `M1` e outras variações sem necessidade.

O mesmo vale para CTT: cada identificador deve representar uma única tarefa e ser usado da mesma forma no diagrama, descrição e legenda.

### 3. Evitar soluções de design excessivamente específicas dentro da análise de tarefas

Em alguns pontos, a modelagem já determina:

- dropdown ou toggle;
- determinados tipos de gráfico;
- ícones específicos;
- formatos de exportação;
- modal de edição;
- preview;
- geração automática.

Alguns desses elementos podem surgir como recomendação, mas a análise de tarefas deve primeiro representar o trabalho e as necessidades do usuário.

Quando uma alternativa de interface ainda não foi validada, mantenham-na como recomendação ou hipótese, e não como fato inevitável do fluxo.

### 4. Usar a Entrega 05 para reduzir, e não aumentar, o escopo

A análise de tarefas deveria ajudar a identificar quais atividades realmente precisam estar no protótipo.

No estado atual, T01, T02 e T03 parecem empurrar o projeto para três grandes famílias de funcionalidade: análise de prova, histórico/comparação e geração de novas questões.

Isso amplia significativamente a solução.

A equipe deve priorizar as tarefas sustentadas pelos cenários e pela contribuição do TCC antes de levar funcionalidades para o protótipo.



A equipe já percorreu uma parte importante do caminho: os diagramas existem, são legíveis e demonstram tentativa real de aplicação das três técnicas. Agora é necessário tratar HTA, GOMS e CTT como **modelos formais**, e não como três formas diferentes de desenhar o mesmo fluxo. Cada técnica responde a uma pergunta diferente - decomposição e planos no HTA, metas/métodos/operações no GOMS e relações temporais/tipos de tarefa no CTT. Quando essas diferenças ficam claras, o modelo deixa de ser apenas “mais um desenho” e passa a efetivamente orientar o projeto de interação.
