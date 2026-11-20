# Feedback do Professor > Entrega 12 > Equipe 05

## Avaliação geral

A equipe apresentou um planejamento consideravelmente desenvolvido para a avaliação da interface. As seis etapas do DECIDE foram preenchidas, os dois métodos obrigatórios estão previstos (avaliação heurística por inspeção e observação/teste com usuários), existe definição de público, ambiente, equipamentos, piloto, questões éticas, tarefas, instrumentos e um plano de análise que procura antecipar como sucesso, erro, ajuda, tempo, satisfação e dados qualitativos serão tratados.

Também é positivo que os instrumentos não tenham ficado apenas citados no texto. O repositório contém termo de consentimento, roteiro de teste, planilha de observação, formulário heurístico e questionários pré e pós-teste. Isso torna o planejamento mais próximo de algo que outra equipe poderia realmente executar.

Entretanto, o plano ainda precisa de revisão metodológica importante antes de ser considerado pronto para execução. O problema central está na relação entre **objetivo → pergunta → método → evidência → critério**. Em várias perguntas, a equipe atribui à avaliação heurística medidas que somente podem ser produzidas por observação de usuários, como taxa de conclusão, tempo de execução, quantidade de pedidos de ajuda e satisfação. A avaliação heurística pode prever problemas potenciais de usabilidade; ela não produz, sozinha, desempenho real de usuários.

Outro problema importante está nas tarefas UT01 e UT02. As duas tarefas terminam essencialmente quando o participante envia a prova, preenche parâmetros e “gera a análise”. Porém, boa parte das perguntas de avaliação pretende investigar se o professor **compreende as métricas, interpreta os resultados e consegue usar essas informações para analisar a prova**. No planejamento atual, o participante pode cumprir o critério de sucesso sem demonstrar que compreendeu o principal resultado da aplicação.

Também há inconsistências entre o plano, os instrumentos e o tratamento ético. O texto prevê gravação de falas/comportamentos e uso de áudio/vídeo para medição, enquanto o termo de consentimento marca apenas gravação de tela e nega gravação de áudio e vídeo. O protocolo de *think aloud* depende de registro das verbalizações, portanto essa divergência precisa ser resolvida antes da coleta.

A entrega está próxima de um planejamento executável, mas ainda precisa separar melhor o que será aprendido com inspeção e o que será aprendido com usuários reais, além de garantir que as tarefas realmente testem a parte mais importante da interface: interpretação dos resultados.

## Pontos positivos

- As seis etapas do DECIDE foram preenchidas e contextualizadas para o projeto.
- A equipe incluiu os dois métodos previstos para as próximas avaliações: inspeção heurística e observação/teste com usuários.
- O planejamento procura diferenciar a avaliação da interface da avaliação científica do TCC.
- O público do teste foi definido como docentes que elaboram e aplicam avaliações de múltipla escolha.
- Há critérios de inclusão e exclusão para participantes.
- O ambiente de teste foi definido como presencial, em sala reservada.
- A equipe prevê teste piloto antes das sessões finais.
- Há divisão de responsabilidades entre facilitador, observador e responsável por análise/cronometragem.
- O planejamento prevê riscos técnicos, como falha de conexão e instabilidade do protótipo.
- Os aspectos éticos contemplam voluntariedade, consentimento, anonimização e proteção de dados de terceiros.
- Existe preocupação explícita em comunicar ao participante que o produto está sendo avaliado, e não sua competência profissional.
- O plano prevê evitar o uso de provas contendo dados sensíveis de alunos.
- O roteiro de teste usa cenários relativamente neutros e não instrui diretamente onde clicar.
- A equipe define previamente sucesso total, sucesso parcial e falha.
- Erro, dúvida, ajuda e abandono possuem definições operacionais.
- O tempo de execução possui ponto de início e ponto de término definidos.
- Foi planejada escala pós-tarefa do tipo SEQ.
- Há proposta de codificação qualitativa para problemas de interface, problemas de signo/conceito e sugestões/comentários.
- O formulário de avaliação heurística contém as dez heurísticas de Nielsen.
- A equipe prevê classificação de severidade e comparação dos resultados com metas de usabilidade.
- O questionário pré-teste coleta experiência docente, uso de avaliações e familiaridade com tecnologia, informações pertinentes ao perfil desta aplicação.
- O questionário pós-teste inclui questões de facilidade, clareza, compreensão dos signos e utilidade percebida.

## Correções prioritárias

### 1. Separar claramente o que a avaliação heurística mede e o que o teste com usuários mede

Este é o principal problema metodológico da entrega.

A avaliação heurística é uma **inspeção**. O avaliador examina a interface e identifica violações potenciais das heurísticas.

O teste com usuários é uma **observação de experiências reais de uso**. É nele que podem ser medidos:

- sucesso ou falha na tarefa;
- tempo de execução;
- erros cometidos;
- pedidos de ajuda;
- hesitações;
- satisfação;
- compreensão demonstrada pelo participante.

Na tabela de perguntas, várias linhas misturam essas duas naturezas.

Em QA01, por exemplo, a métrica inclui taxa de conclusão, erros, solicitações de ajuda e abandono e o método é “heurística, observação”. A avaliação heurística não produz taxa de conclusão real nem abandono de usuários.

QA07 pretende medir eficiência, tempo e erros, mas novamente inclui heurística.

QA08 investiga insatisfação e utiliza como critério 75% de satisfação, mas também inclui heurística. Um avaliador pode prever que algo cause insatisfação, mas não pode medir satisfação de usuários reais por inspeção.

QA12 utiliza somente “heurística”, mas as evidências propostas são hesitações, pedidos de ajuda e erros de navegação - evidências que dependem de observar uma pessoa usando a interface.

A equipe precisa revisar cada pergunta e decidir:

- a pergunta é respondida por inspeção?
- por observação?
- ou pelos dois métodos de maneira complementar, mas com evidências diferentes?

Se os dois métodos forem utilizados para uma mesma pergunta, registrem separadamente o que cada um produzirá.

### 2. Justificar a escolha dos dois métodos pela sua complementaridade, e não apenas pela obrigatoriedade

Na etapa `C - Choose`, a justificativa atual é:

> “Serão utilizados os métodos de inspeção heurística e observação de usuários devido a sua obrigatoriedade pelo professor da disciplina.”

Isso explica por que os métodos estão na entrega, mas não demonstra compreensão de por que eles fazem sentido para o projeto.

A justificativa deveria reconhecer que os métodos respondem a tipos diferentes de pergunta.

A inspeção heurística permite examinar sistematicamente um conjunto amplo de telas e estados e prever problemas de usabilidade.

A observação permite descobrir problemas reais, caminhos inesperados, interpretações, erros, dúvidas e estratégias que a equipe não consegue antecipar apenas inspecionando a própria interface.

É exatamente a combinação dos dois resultados que torna o planejamento mais robusto.

### 3. “Analisar a apropriação da tecnologia” é um objetivo maior do que o estudo planejado consegue responder

Na etapa `D - Determine the goals`, a equipe registra dois objetivos:

- identificar problemas de interação/interface;
- analisar a apropriação da tecnologia.

O primeiro está adequado.

O segundo não está coerente com uma sessão presencial de aproximadamente 30 minutos realizada em laboratório.

Apropriação envolve compreender como uma tecnologia passa a ser incorporada às práticas do usuário ao longo do uso. Uma sessão curta pode investigar:

- facilidade de uso;
- compreensão;
- aceitação inicial;
- percepção de utilidade;
- intenção declarada de uso.

Mas isso não equivale a demonstrar apropriação real da tecnologia.

A equipe deve reduzir esse objetivo ao que o método e o contexto conseguem efetivamente observar.

### 4. Relacionar explicitamente os objetivos da avaliação às metas MU01–MU05 da Entrega 08

O DECIDE começa pela definição dos objetivos.

O próprio modelo solicita relação com as metas de usabilidade anteriores.

A equipe só realiza essa ligação de maneira mais clara no final do plano, quando compara resultados com MU01, MU03, MU04 e MU05.

Essa ligação deveria aparecer desde o início.

Além disso, MU02 - facilidade de memorização - desapareceu do planejamento.

Se a equipe decidiu não avaliar memorização porque exigiria uma segunda sessão após determinado intervalo, isso é perfeitamente defensável. O problema é simplesmente deixar a meta desaparecer.

A equipe deve registrar explicitamente:

- quais metas serão avaliadas;
- quais não serão;
- por que alguma meta ficará fora do escopo desta avaliação.

### 5. As perguntas de avaliação estão numerosas e algumas ainda são genéricas demais

A seção possui quinze perguntas.

Quantidade não é qualidade.

Várias perguntas foram claramente inspiradas pelas questões gerais apresentadas na teoria, mas ainda precisam ser transformadas em perguntas específicas para o DesemProv.

Por exemplo:

> “A tecnologia disponível pode oferecer maneiras mais interessantes ou eficientes de os usuários atingirem seus objetivos?”

é uma pergunta válida em uma discussão geral de avaliação de IHC, mas muito ampla para orientar este protocolo específico.

Da mesma forma:

> “Quais objetivos dos usuários podem ser alcançados através do sistema e quais não podem ser alcançados?”

pode produzir respostas vagas se a avaliação possui apenas duas tarefas muito semelhantes.

Sugiro reduzir e consolidar as perguntas em torno de questões realmente decisivas para esta interface, como:

- o docente consegue submeter corretamente uma prova?
- entende os parâmetros solicitados?
- percebe o estado de processamento?
- compreende as métricas apresentadas?
- consegue identificar um ponto da prova que merece atenção?
- entende as limitações do que os resultados permitem concluir?
- recupera-se dos principais estados de erro?

Não precisam copiar essas perguntas; usem-nas apenas como referência para tornar o conjunto mais específico.

### 6. UT01 e UT02 praticamente testam o mesmo fluxo

As duas tarefas possuem contextos diferentes:

- UT01 ocorre antes da aplicação da prova;
- UT02 ocorre depois de um desempenho fora do esperado.

Porém, os critérios de sucesso são praticamente idênticos:

> concluir upload, preencher informações e gerar a análise.

Assim, a diferença de contexto não produz diferença observável na tarefa.

Se UT02 pretende representar análise posterior à aplicação, ela deveria explorar os elementos específicos que tornam esse cenário diferente - por exemplo, o uso de dados reais de desempenho, quando disponíveis, e a interpretação desses resultados.

Caso contrário, vocês terão duas execuções do mesmo fluxo com narrativas diferentes.

### 7. As tarefas não verificam adequadamente a compreensão dos resultados

Este é um dos pontos mais importantes desta entrega.

QA02 pergunta se o usuário consegue analisar as métricas.

QA03 pergunta se as métricas auxiliam na compreensão da avaliação.

QA11 investiga se os elementos são compreendidos.

QA13 investiga se informações são localizadas.

Entretanto, UT01 e UT02 terminam quando o participante:

> “gera a análise”.

O participante pode atingir o critério de sucesso sem interpretar um único gráfico.

A avaliação precisa incluir pelo menos um resultado observável relacionado à interpretação.

O participante deve demonstrar que consegue usar a tela de resultados para responder a uma necessidade do cenário, e não apenas chegar ao dashboard.

Isso é especialmente importante porque a Entrega 11 mostrou que a página de resultados é a parte mais densa e conceitualmente crítica da interface.

### 8. O planejamento precisa decidir se avaliará também os estados de erro e recuperação

A interface da Entrega 11 possui diversos estados de erro:

- formato de arquivo inválido;
- arquivo grande;
- falha no processamento;
- duração inválida;
- métrica indisponível;
- ausência de acertos por questão.

A inspeção heurística pode avaliar todos esses estados.

No teste com usuários, não é necessário provocar artificialmente todos os erros. Porém, se recuperação de erros for uma questão importante - e QA05/QA15 indicam que é - o planejamento deve definir se algum estado será deliberadamente incluído na tarefa ou se apenas erros espontâneos serão observados.

Hoje essa decisão não está clara.

### 9. A quantidade de participantes do teste não deve permanecer como “1 a 3”

O grupo possui três integrantes e o planejamento da etapa de observação precisa ser suficientemente definido antes da execução.

Registrar “1 a 3” deixa uma decisão essencial aberta.

Além disso, com apenas um participante não seria possível sequer observar recorrência entre participantes.

Definam previamente a quantidade que será utilizada.

Para esta equipe, a continuação natural do planejamento é trabalhar com os três participantes previstos para a avaliação final, respeitando os critérios de inclusão definidos.

### 10. O critério de 90% de sucesso precisa ser interpretado com cuidado em uma amostra pequena

MU01 estabelece taxa de sucesso de pelo menos 90%.

Com três participantes, a proporção de sucesso varia em saltos de aproximadamente um terço:

- 3/3;
- 2/3;
- 1/3;
- 0/3.

Isso significa que, na prática, “pelo menos 90%” corresponderá a 100% dos três participantes.

Não há problema em manter a meta como referência de projeto, mas a equipe não deve tratar uma amostra tão pequena como estimativa estatística precisa da população.

O relatório deve apresentar os resultados como **indícios obtidos naquele grupo de participantes**, complementados pelas evidências qualitativas.

### 11. O plano da avaliação heurística precisa explicitar a execução individual antes da consolidação

A equipe prevê três avaliadores internos, o que é coerente com o método.

Porém, o ambiente foi descrito como:

> “Presencial/Remoto em reunião síncrona (Google Meet) entre os membros da equipe.”

Isso pode sugerir que a inspeção será realizada em conjunto.

A avaliação heurística deve preservar a inspeção individual antes da consolidação, para evitar que um avaliador influencie os achados dos demais.

O planejamento precisa indicar claramente:

1. cada avaliador percorre individualmente as telas e H1–H10;
2. registra seus achados sem discutir com os demais;
3. somente depois os resultados são consolidados;
4. problemas repetidos são agrupados e a severidade final é discutida.

Esse encadeamento prepara corretamente a Entrega 13.

### 12. O escopo da inspeção heurística precisa listar as telas e estados que serão examinados

O planejamento afirma que haverá avaliação heurística, mas não delimita claramente seu escopo visual.

Na Entrega 11 já existem telas e estados identificados, incluindo:

- upload;
- arquivo selecionado;
- parametrização;
- ajuda;
- resultados;
- filtros;
- exportação;
- diferentes erros.

A inspeção deve informar quais desses estados fazem parte do escopo.

Isso também evita que três avaliadores inspecionem conjuntos diferentes de telas sem perceber.

### 13. Resolver a contradição sobre gravação de áudio

Há uma inconsistência direta entre os documentos.

O plano afirma que serão utilizados:

- microfone;
- câmera;
- OBS Studio ou Google Meet;
- gravação de áudio/vídeo para medir o tempo;
- transcrição das falas do *think aloud*.

O termo de consentimento, porém, marca:

- gravação de tela: **sim**;
- gravação de áudio: **não**;
- gravação de vídeo: **não**.

Essas duas decisões não podem coexistir.

Se o áudio do participante será gravado para análise das verbalizações, isso precisa constar explicitamente no consentimento.

Se o áudio não será gravado, a equipe deve retirar do plano a afirmação de que as falas serão posteriormente transcritas a partir da gravação e definir como o observador fará o registro.

Corrijam isso **antes** de recrutar participantes.

### 14. O protocolo de *think aloud* precisa estar consistente em todos os instrumentos

O termo de consentimento informa que o participante deverá pensar em voz alta.

O roteiro também menciona a técnica.

O plano de análise afirma que as falas e comportamentos gravados serão transcritos.

Portanto, *think aloud* não é apenas uma possibilidade: ele está sendo adotado como parte do método.

Nesse caso, o protocolo precisa deixar claro:

- como a técnica será explicada;
- quando o moderador pode lembrar o participante de continuar verbalizando;
- que o moderador não deve transformar o lembrete em orientação da tarefa;
- como as falas serão registradas.

### 15. A escala de satisfação de 75% continua sem fórmula definida

A Entrega 08 já apresentava a meta MU05 de 75% de satisfação.

Nesta entrega, a equipe avançou ao criar:

- SEQ 1–7 pós-tarefa;
- questionário pós-teste com escalas 1–5 e respostas categóricas.

Entretanto, ainda não está definido **como 75% será calculado**.

Será:

- percentual do máximo possível?
- percentual de respostas “fácil/muito fácil”?
- média convertida para uma escala de 0–100?
- combinação de várias perguntas?
- apenas uma questão específica?

Antes da coleta, essa fórmula precisa estar definida. Caso contrário, a equipe poderá escolher depois o cálculo que produz o resultado mais conveniente.

### 16. O instrumento SEQ está definido no plano, mas não está materializado com a mesma clareza dos demais instrumentos

O plano afirma que, após cada tarefa, será aplicada a pergunta:

> “Quão fácil ou difícil foi realizar esta tarefa?”

em escala de 1 a 7.

A planilha de observação possui uma coluna “Satisfação”, portanto é possível registrar a resposta.

Mesmo assim, seria melhor deixar explícito no roteiro/planilha:

- a pergunta exata;
- os extremos da escala;
- o sentido da pontuação.

Isso evita que diferentes moderadores utilizem formulações diferentes.

### 17. O questionário pós-teste mistura facilidade, clareza, relevância pedagógica e intenção de uso

Isso não é necessariamente um problema, pois são informações úteis.

O problema aparece quando todos esses itens são tratados como se medissem a mesma coisa chamada “satisfação”.

“Utilizaria o DesemProv na sua rotina?” mede intenção declarada de uso.

“As métricas são relevantes?” mede utilidade percebida.

“Quão fácil foi operar?” mede facilidade percebida.

“Clareza das instruções” mede compreensão.

A equipe deve preservar esses dados separadamente ou justificar qualquer índice composto.

### 18. A avaliação deve distinguir usabilidade da validade científica das métricas

O próprio modelo da entrega exige essa distinção.

O plano afirma que a avaliação investiga interação/protótipo, o que é correto.

Porém, algumas perguntas e o questionário pós-teste podem levar o participante a julgar se as métricas “realmente” melhoram a prova.

A avaliação com docentes pode investigar:

- se entendem as métricas;
- se consideram as informações úteis;
- como utilizariam o resultado;
- se a apresentação apoia uma decisão.

Ela não deve ser usada como evidência de que o modelo científico do TCC está correto ou de que determinada característica realmente causa desempenho.

Mantenham essa separação explícita durante a moderação e no relatório.

### 19. O plano de análise precisa separar a consolidação da avaliação heurística da consolidação do teste com usuários

A seção final mistura ambos em um único tratamento de problemas.

Os dois métodos produzem resultados diferentes.

Na heurística:

- cada avaliador registra violações;
- os achados são consolidados;
- duplicidades são agrupadas;
- severidade é discutida;
- cada problema permanece ligado à heurística violada.

Na observação:

- os dados são consolidados por participante e por tarefa;
- podem ser calculados sucesso, tempo, erros e ajuda;
- comportamentos e falas são interpretados;
- recorrências são identificadas.

Depois disso, os dois conjuntos podem ser comparados.

Essa separação é importante inclusive pedagogicamente, porque permitirá verificar quais problemas os avaliadores previram e quais apareceram apenas com usuários reais.

### 20. A classificação de severidade de Nielsen deve ser aplicada com cuidado aos achados da observação

É possível utilizar uma escala de prioridade também para problemas encontrados com usuários.

Porém, a escala de severidade da avaliação heurística possui uma lógica própria e será usada formalmente na Entrega 13.

No teste de usuários, o impacto pode ser interpretado utilizando:

- frequência;
- gravidade da consequência;
- capacidade de recuperação;
- bloqueio da tarefa.

Se a mesma escala 0–4 for reutilizada, a equipe deve explicar que está adotando essa escala também como mecanismo de priorização dos achados empíricos, e não confundir isso com uma “violação heurística” encontrada pelo usuário.

### 21. A descrição “dados simulados serão declarados” precisa indicar exatamente o que pode estar simulado

O plano registra que a versão é parcial e que limitações funcionais ou dados simulados serão declarados.

Essa é uma boa prática, mas ainda genérica.

Antes da execução, indiquem exatamente:

- quais funcionalidades são reais;
- quais resultados são simulados, se houver;
- quais estados não estão integrados;
- o que será dito ao participante.

O teste deve avaliar a interação sem induzir o usuário a acreditar que um processamento científico está funcionando quando ele está apenas sendo simulado.

### 22. A rastreabilidade ainda possui inconsistências que afetam o planejamento da avaliação

A `RASTREABILIDADE.md` continua utilizando IDs F01–F04 com significados diferentes dos adotados na Entrega 11.

Além disso, nas linhas R01–R04, `UT01 e UT02` aparecem sob a coluna “Heurística/problema”, deslocando semanticamente as colunas seguintes.

Isso precisa ser corrigido agora.

A Entrega 12 é justamente o momento em que a cadeia deveria estar clara:

**necessidade → tarefa → MoLIC → tela → pergunta de avaliação → problema heurístico/tarefa de usuário → melhoria.**

Se os IDs e colunas estiverem inconsistentes, os resultados das Entregas 13 e 14 serão difíceis de relacionar ao projeto.

### 23. H04–H11 continuam aparecendo como “fechadas” sem evidência suficiente

A rastreabilidade mantém várias hipóteses como fechadas mesmo quando a evidência apresentada é:

- persona hipotética;
- cenário hipotético;
- entendimento da própria equipe;
- concorrentes;
- ausência de dado.

Isso é particularmente estranho agora, porque a Entrega 12 está preparando exatamente a etapa que deveria gerar parte das evidências empíricas necessárias.

Não utilizem o planejamento de avaliação como se ele já tivesse validado as hipóteses.

Quando a evidência ainda não foi coletada, mantenham a hipótese aberta.

### 24. A tarefa UT02 ainda mantém o problema de escopo de O02 sem testar o que realmente diferencia esse cenário

UT02 diz que a prova já foi aplicada e que o desempenho ficou fora do esperado.

Esse cenário deveria permitir observar se o docente consegue utilizar informações de desempenho real - quando disponíveis - junto às métricas estruturais.

Porém, o critério de sucesso é o mesmo de UT01.

Se o objetivo O02 continuar no escopo, a avaliação precisa refletir a diferença entre:

- análise preventiva;
- análise posterior à aplicação.

Caso contrário, O01 e O02 estão sendo tratados como duas narrativas para o mesmo teste.

### 25. Revisar o checklist antes de manter o status “Concluída”

O checklist marca todos os itens como atendidos.

Porém, ainda existem questões objetivas abertas:

- pergunta/método/evidência nem sempre correspondem;
- MU02 não está tratada;
- a quantidade de participantes continua indefinida;
- há contradição sobre gravação de áudio;
- a fórmula dos 75% de satisfação não está definida;
- as tarefas não testam adequadamente a interpretação dos resultados;
- o escopo da inspeção heurística não está delimitado por telas/estados.

Portanto, o status “Concluída” é prematuro.

O checklist deve ser refeito depois dessas decisões.

## Recomendações de melhoria

### 1. Criar duas subseções operacionais dentro do mesmo DECIDE

O DECIDE pode continuar sendo um planejamento único da equipe, mas, depois das decisões gerais, seria útil deixar muito explícitos dois planos de execução:

**Plano A - Avaliação heurística**

- avaliadores;
- telas/estados;
- execução individual;
- H1–H10;
- registro de evidências;
- severidade;
- consolidação.

**Plano B - Teste com usuários**

- participantes;
- tarefas;
- roteiro;
- métricas;
- think aloud;
- satisfação;
- consentimento;
- análise.

Isso reduz bastante a mistura atual entre os dois métodos.

### 2. Reduzir as perguntas de avaliação às que realmente serão respondidas

Quinze perguntas podem tornar a sessão e a análise dispersas.

Priorizem as perguntas que podem realmente mudar decisões de design.

Se uma pergunta não está ligada a uma tarefa, tela, métrica ou decisão de projeto, provavelmente não precisa ser central nesta avaliação.

### 3. Planejar explicitamente a avaliação da tela de resultados

A aplicação existe para entregar uma análise ao professor.

Portanto, a avaliação não pode terminar no momento em que o dashboard aparece.

A parte mais importante é verificar se o docente consegue transformar os resultados apresentados em compreensão e decisão.

### 4. Comparar depois os achados dos dois métodos

Uma boa síntese das Entregas 13 e 14 poderá responder:

- quais problemas foram previstos pela heurística e também apareceram com usuários;
- quais problemas foram previstos pelos avaliadores, mas não apareceram nos testes;
- quais problemas só foram descobertos pelos usuários;
- quais pontos positivos foram percebidos em ambos.

Isso demonstrará claramente o valor da combinação de inspeção e observação.

## Pontos que devem alimentar as próximas entregas

- **Entrega 13:** cada integrante deve realizar a inspeção de forma independente antes da consolidação.
- **Entrega 13:** definir previamente todo o conjunto de telas e estados que será inspecionado.
- **Entrega 13:** manter violações ligadas às heurísticas correspondentes e evitar misturar resultados de usuários nessa etapa.
- **Entrega 14:** utilizar exatamente a quantidade final de participantes definida neste planejamento, e não uma faixa aberta.
- **Entrega 14:** registrar sucesso, erro, ajuda, tempo e satisfação por tarefa.
- **Entrega 14:** incluir pelo menos uma atividade que exija interpretação dos resultados apresentados.
- **Entrega 14:** distinguir claramente análise preventiva e análise pós-aplicação, se O01 e O02 permanecerem como objetivos distintos.
- **Ética:** resolver antes da coleta se haverá gravação de áudio e atualizar o consentimento.
- **Instrumentos:** formalizar a pergunta SEQ 1–7 no roteiro/planilha.
- **Metas:** definir matematicamente como MU05 será calculada.
- **MU02:** decidir se memorização será excluída desta avaliação ou se haverá uma segunda sessão.
- **Rastreabilidade:** corrigir imediatamente IDs de telas, colunas deslocadas e hipóteses indevidamente fechadas.
- **Resultados:** tratar a amostra pequena como evidência exploratória para melhoria da interface, não como estimativa estatística da população de docentes.

## Síntese das ações recomendadas

1. **Revisar todas as QA01–QA15 separando evidências produzidas pela heurística das evidências produzidas por usuários.**
2. **Justificar teoricamente a complementaridade entre avaliação heurística e teste com usuários.**
3. **Retirar ou redefinir o objetivo amplo de “apropriação da tecnologia”.**
4. **Relacionar explicitamente o DECIDE às metas MU01–MU05 e decidir o destino de MU02.**
5. **Reduzir e tornar mais específicas as perguntas de avaliação.**
6. **Modificar UT01/UT02 para avaliar também a interpretação dos resultados, não apenas a geração da análise.**
7. **Diferenciar de forma real UT01 e UT02, caso os dois objetivos permaneçam no escopo.**
8. **Fixar a quantidade final de participantes do teste.**
9. **Garantir inspeção heurística individual antes da consolidação.**
10. **Listar previamente as telas/estados que serão inspecionados.**
11. **Resolver a contradição sobre gravação de áudio e atualizar o TCLE/roteiro.**
12. **Definir a fórmula de cálculo da meta de 75% de satisfação.**
13. **Separar a análise dos resultados heurísticos da análise dos resultados observacionais.**
14. **Documentar exatamente quais dados/processamentos estarão simulados durante o teste.**
15. **Corrigir a rastreabilidade antes das Entregas 13 e 14.**
16. **Reabrir hipóteses que continuam sem evidência empírica suficiente.**
17. **Refazer o checklist somente depois dessas decisões.**

A equipe fez um trabalho importante ao preparar instrumentos e antecipar como os dados serão registrados. Agora o planejamento precisa ganhar precisão metodológica. A regra simples é: **a heurística prevê; o usuário revela**. Se quero saber quanto tempo uma pessoa levou, quantas vezes pediu ajuda ou se ficou satisfeita, preciso observá-la. Se quero saber se uma tela viola consistência, prevenção de erros ou visibilidade do estado, posso inspecioná-la. Quando cada pergunta sabe exatamente de onde virá sua resposta, o DECIDE deixa de ser uma sigla preenchida e passa a ser, de fato, um plano de avaliação.
