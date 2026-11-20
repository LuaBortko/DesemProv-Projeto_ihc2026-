# Feedback do Professor > Entrega 14 > Equipe 05

## Avaliação geral

A equipe executou efetivamente uma avaliação de usabilidade por observação e produziu um conjunto de dados consideravelmente mais rico do que apenas um relato genérico de “usuários gostaram da interface”.

Foram observados três participantes finais, quantidade compatível com os três integrantes da equipe. Dois participantes são docentes e um participante foi utilizado como proxy. A equipe também distribuiu a responsabilidade entre Luana, Beatriz e Nuno, apresentou questionários pré e pós-teste individualizados, registrou sucesso, erros, ajudas, tempos, satisfação e observações qualitativas, consolidou os resultados por tarefa e produziu seis achados com recomendações.

Outro avanço importante em relação ao planejamento da Entrega 12 foi a revisão de UT01: agora ela não termina apenas quando o dashboard aparece. O participante também precisa explorar os resultados e explicar o que compreendeu a partir das métricas. Essa mudança é conceitualmente correta e aproxima o teste do verdadeiro objetivo da aplicação.

Entretanto, a entrega possui problemas sérios de **consistência metodológica e tratamento dos dados**. Em vários casos, o moderador ajudou diretamente o participante, mas a tarefa continuou sendo classificada como sucesso total, mesmo quando o próprio critério de sucesso exigia realização “sem auxílio do moderador”. Isso infla a taxa de sucesso apresentada.

Também existem tempos registrados em formato inválido, como `8:92` e `08:87`, e o valor consolidado de UT01 não corresponde aos tempos individuais apresentados. As porcentagens de satisfação também não estão claramente ligadas a uma escala registrada por tarefa. Além disso, os identificadores dos participantes nos questionários pré e pós-teste estão inconsistentes, especialmente em U03.

A conclusão geral da equipe - de que os dados oferecem indícios úteis e não permitem generalização ampla - é correta. Porém, antes de considerar as metas atingidas ou parcialmente atingidas, é necessário corrigir os dados quantitativos e garantir que cada número apresentado possa ser rastreado até o instrumento que o produziu.

## Pontos positivos

- A quantidade de participantes finais atende ao enunciado: três participantes para três integrantes.
- U01 e U03 são docentes e possuem relação direta com o público prioritário da aplicação.
- O uso de U02 como participante proxy foi declarado e a limitação aparece na conclusão.
- A equipe não apresenta U02 como equivalente a um docente sem qualquer ressalva.
- O teste piloto foi registrado.
- Existe um fluxograma do processo completo de avaliação.
- Há termo de consentimento, questionários pré e pós-teste e roteiro de teste.
- O protocolo inclui a orientação de que o produto está sendo avaliado, e não a pessoa.
- O protocolo prevê voluntariedade e interrupção da participação.
- O uso de think aloud está previsto.
- Há definição de anonimização por IDs.
- UT01 e UT02 são contextualizadas como situações de trabalho docente, e não como listas de comandos do tipo “clique aqui”.
- UT01 foi melhorada em relação ao planejamento anterior e agora exige interpretação de métricas.
- Os resultados são apresentados separadamente por participante e tarefa.
- As intervenções dos moderadores foram registradas, em vez de serem escondidas.
- U01 produziu observações úteis sobre nomenclaturas, rolagem, cores, legendas, degradês e informações escondidas em hover.
- U02 identificou dificuldade concreta com o gráfico de correlação.
- U03 identificou dificuldades importantes na entrada de dados, compreensão do estado da interface e entendimento de métricas reais.
- A consolidação qualitativa distingue problemas de interpretação, entrada, navegação, destaque visual e estado de processamento.
- A comparação com a avaliação heurística demonstra corretamente que os dois métodos podem revelar problemas diferentes.
- A conclusão reconhece a limitação da amostra e o fato de apenas dois participantes pertencerem diretamente ao público-alvo.

## Correções prioritárias

### 1. Recalcular as taxas de sucesso considerando o próprio critério definido pela equipe

Este é o problema mais importante da entrega.

UT01 define como critério de sucesso:

> o participante consegue realizar a tarefa e interpretar as métricas “sem auxílio do moderador”.

UT02 também define conclusão:

> “sem auxílio do moderador”.

Porém, os registros individuais mostram:

- U01 / UT01: três ajudas → corretamente marcado como parcial;
- U02 / UT01: houve intervenção para relembrar o fluxo e garantir o preenchimento correto → foi marcado como total;
- U03 / UT01: houve três intervenções/ajudas → foi marcado como total;
- U01 / UT02: zero ajuda → total;
- U02 / UT02: houve intervenção e foi marcado como parcial;
- U03 / UT02: houve uma ajuda para explicar a seção de número de acertos → foi marcado como total.

Isso não é consistente.

Se “sem auxílio” faz parte do critério, U02/UT01, U03/UT01 e U03/UT02 não podem permanecer como sucesso total.

Com os registros atuais, a taxa de sucesso total tende a ser significativamente menor do que os 67% informados.

A equipe precisa reaplicar a mesma regra de classificação para os três participantes.

### 2. Não tratar intervenção do moderador como parte normal do “fluxo desejado”

No registro de U02 aparece:

> “logo foi corrigida pela desenvolvedora para não comprometer o fluxo desejado de teste”

e:

> “foi necessário intervir para relembrar a tarefa específica e garantir o fluxo correto de uso”.

Esse tipo de intervenção é justamente um dado do teste.

Se o participante compreende o cenário de maneira diferente do esperado, isso pode indicar:

- tarefa mal formulada;
- diferença de modelo mental;
- interface que permite interpretações alternativas;
- necessidade de esclarecer o protocolo.

O moderador não deve corrigir o participante para garantir o comportamento que a equipe desejava observar.

Quando a intervenção for inevitável, registrem-na como ajuda e considerem seu efeito na classificação da tarefa.

### 3. Corrigir os tempos inválidos de U02

U02 / UT02 apresenta:

> `8:92 (completo)` e `08:87 (apenas teste da aplicação)`.

Esses tempos não são válidos no formato `mm:ss`.

Portanto, não é possível reproduzir o cálculo do tempo consolidado enquanto esse registro não for corrigido.

Confiram a gravação ou o registro original e substituam pelos valores corretos.

### 4. O tempo consolidado de UT01 não corresponde aos tempos registrados

Os tempos completos apresentados para UT01 são:

- U01: 17:38;
- U02: 08:21;
- U03: 13:00.

A consolidação informa:

> `12:26`.

Esse valor não corresponde nem à média nem à mediana dos três tempos apresentados.

A média está próxima de 13 minutos e a mediana é 13:00.

A equipe precisa dizer explicitamente o que significa “tempo típico”:

- média?
- mediana?
- outro cálculo?

Depois, recalcular utilizando o mesmo método para UT01 e UT02.

### 5. UT02 também não pode ter tempo consolidado validado enquanto U02 estiver com tempo inválido

A entrega informa:

> UT02 - tempo típico 13:52.

Mas um dos três registros individuais está em formato inválido.

Assim, esse valor não é auditável.

Não apresentem uma métrica consolidada quando um dos dados de origem não pode ser interpretado.

### 6. A satisfação por tarefa não está rastreável ao instrumento

Os resultados individuais apresentam percentuais como:

- 80%;
- 90%;
- 100%.

Entretanto, o planejamento da Entrega 12 previa uma escala SEQ de 1 a 7 após cada tarefa.

Os questionários pós-teste armazenados no repositório utilizam predominantemente escalas de 1 a 5 e são aplicados depois das tarefas, não registrando claramente uma satisfação separada para UT01 e UT02.

Não está explicado de onde surgiram 80%, 90% e 100% para cada tarefa.

A equipe precisa documentar:

- qual pergunta foi aplicada após UT01;
- qual pergunta foi aplicada após UT02;
- qual escala foi utilizada;
- como a resposta foi convertida para percentual.

Sem isso, os 90% e 93,3% consolidados não são reproduzíveis.

### 7. O questionário pós-teste de U03 possui uma opção fora da escala definida

No questionário pós-teste de U03, a pergunta sobre clareza possui escala de 1 a 5.

Porém, foi acrescentada uma sexta opção:

> `6 - Faltou um pouco de clareza`

Isso invalida a comparabilidade daquela pergunta com os demais participantes.

“Faltou um pouco de clareza” também não representa um valor maior do que “5 - Muito Clara”; semanticamente, seria uma avaliação inferior.

Nunca alterem a escala depois de iniciada a coleta para acomodar uma resposta.

Quando o participante quiser qualificar a resposta, mantenham o valor da escala e registrem o comentário na questão aberta.

### 8. Corrigir os identificadores dos participantes nos instrumentos

Existe uma inconsistência séria de rastreabilidade.

O documento principal usa U01, U02 e U03.

Mas os questionários registram códigos diferentes:

- `questionario_preU01.md` usa `P[02]`;
- `questionario_posU01.md` usa `P:02`;
- `questionario_preU02.md` usa `P01`;
- `questionario_posU02.md` usa `P01`;
- `questionario_preU03.md` usa `P03`;
- `questionario_posU03.md` usa `P01`.

Assim, o pós-teste de U03 aparece com o mesmo código de outro participante.

Além disso, `P01`, `P02` e `P03` já foram utilizados no projeto para identificar personas. Não devem ser reaproveitados para participantes reais.

Padronizem:

- U01;
- U02;
- U03.

Utilizem esses códigos em todos os instrumentos e mantenham a relação com o perfil real separadamente.

### 9. Não chamar U01/U02/U03 de P01/P02/P03

Na seção de participantes aparece:

- U01 - P01;
- U02 - P02;
- U03 - P03.

Isso dá a impressão de que cada participante real “é” uma das personas.

Uma persona é um arquétipo de projeto, não um participante individual.

U02 torna essa inconsistência ainda mais evidente: ele é um colega de turma com conhecimento de IHC, não a persona P02.

Descrevam o perfil de cada participante diretamente, por exemplo:

- docente de Ciência da Computação;
- participante proxy, estudante de Computação com experiência em IHC;
- docente de Administração.

Depois indiquem, quando pertinente, qual persona aquele perfil se aproxima.

### 10. O participante proxy não deve ter o mesmo peso interpretativo dos docentes para conclusões sobre uso pedagógico

A equipe faz bem em reconhecer na conclusão que apenas dois dos três participantes pertencem diretamente ao público-alvo.

Porém, na consolidação quantitativa, os três entram com exatamente o mesmo peso.

Para métricas de interação básica isso pode ser aceitável como dado exploratório.

Para conclusões como:

- utilidade pedagógica;
- intenção de uso em rotina docente;
- adequação da linguagem ao professor;
- compreensão do contexto de avaliação,

o resultado do participante proxy deve ser tratado separadamente ou, no mínimo, com ressalva.

Conhecimento prévio de IHC pode inclusive tornar U02 mais sensível a determinados aspectos da interface e menos representativo do professor típico.

### 11. O checklist afirma que “moderadores não ensinaram o caminho”, mas os registros mostram o contrário

O checklist marca:

> “Moderadores não ensinaram o caminho durante a tarefa.”

Porém, os próprios resultados registram:

- ajuda para escolher arquivo;
- explicação de que dados deveriam ser preenchidos;
- explicação de onde digitar duração;
- esclarecimento sobre métricas reais;
- intervenção para “garantir o fluxo correto”.

Não há problema em ter ocorrido ajuda, desde que ela seja registrada. Isso é inclusive um dado importante de usabilidade.

O problema é marcar o checklist como se nenhuma intervenção tivesse acontecido.

A equipe deve corrigir o checklist e explicar que houve intervenções controladas quando necessárias, contabilizadas como ajuda e consideradas na classificação de sucesso.

### 12. O fluxograma menciona UT03, mas a avaliação possui apenas duas tarefas

No fluxograma aparece:

> “Orientar e acompanhar as tarefas UT01, UT02 e UT03”.

A Entrega 14 possui apenas UT01 e UT02.

Corrijam o artefato para evitar a impressão de que uma terceira tarefa foi executada e não documentada.

### 13. A tarefa UT01 do documento principal ainda orienta demais a sequência de interação

A tarefa principal diz explicitamente:

> “enviar o arquivo da prova, preencher os parâmetros solicitados e realizar a análise”.

Isso antecipa etapas do fluxo.

O roteiro de teste armazenado em `instrumentos/roteiro_teste_usabilidade.md` possui uma formulação melhor:

> “Você quer saber algumas métricas sobre o formato dessa prova... Use o sistema para obter essas informações.”

Essa segunda formulação expressa mais claramente **o que o usuário quer alcançar**, sem listar toda a sequência de ações.

Utilizem a formulação mais neutra como instrução oficial da tarefa.

### 14. UT02 ainda precisa explorar melhor o que a diferencia de UT01

UT02 representa uma situação pós-aplicação.

O diferencial conceitual deveria ser justamente a existência de dados reais do desempenho dos alunos.

Na prática, U03 relatou dificuldade em entender que o número de acertos por questão deveria ser preenchido manualmente.

Esse é um achado importante e mostra que a tarefa possui potencial para avaliar o cenário pós-aplicação.

Porém, o critério de sucesso de UT02 não exige explicitamente:

- inserir os dados reais;
- localizar a análise correspondente;
- interpretar o resultado à luz desses dados.

A tarefa precisa ser mais coerente com o objetivo O02 e com a diferença entre análise preventiva e análise posterior.

### 15. A consolidação de “taxa de sucesso” está semanticamente confusa

A tabela apresenta:

> `67% (2 totais e um parcial)`.

Se existem dois sucessos totais e um parcial, então:

- taxa de sucesso total = 67%;
- taxa de conclusão total ou parcial = 100%.

São métricas diferentes.

A equipe precisa deixar explícito qual delas está reportando.

Isso se torna ainda mais importante depois de corrigir as classificações das tarefas que receberam ajuda.

### 16. A equipe precisa separar tempo “da aplicação” de tempo “completo” de forma metodologicamente clara

Os registros possuem dois tempos:

- “apenas teste da aplicação”;
- “completo”.

Isso pode ser útil, mas falta uma definição.

O que entra no tempo completo?

- leitura da tarefa?
- explicações do moderador?
- preenchimento do questionário?
- think aloud?
- interrupções?
- comentários posteriores?

A meta MU03 deveria utilizar sempre a mesma definição de início e fim para todos.

O planejamento anterior já definia pontos de início e término. A Entrega 14 precisa aplicar exatamente aquela convenção.

### 17. A conclusão afirma cumprimento da meta de 15 minutos com base em uma métrica ainda inconsistente

A conclusão diz que os tempos ficaram abaixo dos 15 minutos planejados.

Porém:

- o tempo consolidado de UT01 não confere com os registros;
- um tempo de U02/UT02 é inválido;
- não está claro se a meta se aplica ao tempo “completo” ou ao tempo de uso da aplicação.

Portanto, ainda não é possível afirmar com segurança que MU03 foi atendida.

Corrijam os registros e o método de cálculo primeiro; depois comparem com a meta.

### 18. MU01 também não foi atingida se considerarmos o critério original de 90%

A Entrega 08 definiu MU01 como taxa de sucesso de pelo menos 90%.

A própria consolidação atual apresenta 67%.

Mesmo antes de revisar as classificações, isso já está abaixo da meta.

Depois de considerar adequadamente as ajudas, a taxa de sucesso total pode cair ainda mais.

Portanto, não tratem a avaliação apenas como “parcialmente atendida” de forma genérica. Digam especificamente:

- MU01 - não atingida;
- MU03 - precisa ser recalculada;
- MU04 - interpretar a partir dos erros/ajudas observados;
- MU05 - precisa ter cálculo rastreável;
- MU02 - não foi efetivamente avaliada por ausência de reaplicação após intervalo.

### 19. MU02 não foi avaliada

A Entrega 14 continua listando MU02 - facilidade de memorização - entre as metas relacionadas.

Mas os participantes realizaram as tarefas na mesma sessão.

Repetir uma tarefa minutos depois mede aprendizagem imediata e familiarização, não necessariamente memorização ao longo do tempo.

Se não houve uma segunda sessão após intervalo previamente definido, MU02 deve ser declarada como **não avaliada nesta rodada**.

Isso já havia sido apontado no planejamento e precisa aparecer explicitamente na conclusão.

### 20. A interpretação de “boa aceitação” deve ser mais cuidadosa

A conclusão utiliza satisfação de 90% e 93,3% para indicar boa aceitação.

Além de o cálculo de satisfação ainda não estar documentado, “aceitação” é um conceito mais amplo do que satisfação imediata durante uma sessão.

Os questionários pós-teste mostram interesse e intenção declarada de uso, o que é positivo.

Mas a formulação mais rigorosa seria:

- percepção inicial positiva;
- satisfação declarada;
- utilidade percebida;
- intenção de uso.

Não confundam isso com adoção ou apropriação real da tecnologia.

### 21. Há um achado importante que deveria ser explicitado: informação essencial escondida em hover

U01 não percebeu dados disponíveis apenas ao passar o mouse sobre o gráfico.

Esse é um achado de usabilidade importante.

Informação necessária à interpretação não deve depender exclusivamente de uma interação que o usuário pode não descobrir.

Esse problema merece um AU específico ou maior destaque em AU02, pois afeta descoberta, reconhecimento e compreensão das métricas.

### 22. AU05 referencia F01, embora o problema seja dos gráficos/resultados

AU05 trata de:

- cores dos gráficos;
- contraste das legendas;
- diferenciação visual dos resultados.

Na coluna “Artefatos a revisar”, aparece:

> “Gráficos, legendas, F01”.

Na Entrega 11, F01 é upload.

O artefato relacionado é a região de resultados - F04 e estados associados.

Essa inconsistência de IDs já foi apontada nas entregas anteriores e precisa finalmente ser corrigida.

### 23. A comparação com a heurística precisa ser atualizada após a correção da Entrega 13

A Entrega 14 considera como problema heurístico:

> “Inconsistência nas mensagens de erro”.

Na correção da Entrega 13, esse achado foi questionado porque “Entendido” e “Tentar novamente” podem representar recuperações semanticamente diferentes.

Além disso, problemas mais importantes de erro - `Network Error`, BERT/RoBERTa e JSON - estavam pouco considerados.

Portanto, antes de concluir a comparação “heurística × usuários”, revisem a consolidação da Entrega 13 e usem os achados heurísticos corrigidos.

### 24. O termo de consentimento ainda contradiz a descrição da Entrega 14 sobre gravação

Na Entrega 14 vocês registram:

> “A gravação de áudio poderá ser utilizada para registrar comentários e dúvidas verbalizadas”.

Entretanto, o termo de consentimento armazenado marca:

- gravação de tela: sim;
- gravação de áudio: não;
- gravação de vídeo: não.

A inconsistência apontada na Entrega 12 permaneceu.

Se houve gravação de áudio, o consentimento precisava autorizar isso.

Se não houve, a Entrega 14 não deve afirmar que o áudio foi utilizado.

Corrijam o relato para refletir exatamente o procedimento executado.

### 25. O prazo de descarte também está inconsistente entre os documentos

Na Entrega 14, os arquivos de gravação seriam excluídos:

> após a consolidação dos resultados e conclusão da avaliação.

No termo de consentimento, os dados seriam descartados:

> após a conclusão e a defesa do trabalho.

São períodos diferentes.

O participante precisa receber uma informação única e verdadeira.

Padronizem o critério de descarte.

### 26. O protocolo do moderador está correto no documento principal, mas precisa ser demonstrado pelos registros

O Passo 6 contém os elementos esperados:

- boas-vindas;
- produto, não pessoa;
- consentimento;
- pré-teste;
- instruções;
- observação;
- think aloud;
- pós-tarefa;
- pós-teste;
- encerramento.

Isso está bem estruturado.

O ponto de atenção é que o protocolo real incluiu diversas intervenções.

Nas próximas avaliações, mantenham uma política explícita:

- silêncio e observação como padrão;
- lembrete de think aloud sem orientar ação;
- ajuda apenas quando definida como necessária;
- toda ajuda registrada;
- tarefa reclassificada adequadamente após ajuda.

### 27. A `RASTREABILIDADE.md` ainda não incorpora AU01–AU06

O checklist afirma:

> “Achados geram recomendações e atualização da rastreabilidade.”

Entretanto, a matriz ainda não registra AU01–AU06.

A coluna “Heurística / problema” continua sem incorporar adequadamente os problemas das Entregas 13 e 14.

Esta é a última entrega do ciclo e a rastreabilidade deveria fechar a cadeia:

**necessidade → cenário → tarefa → modelo → interface → avaliação → problema → melhoria.**

Incluam os achados de observação, telas afetadas e decisões de melhoria.

### 28. A rastreabilidade continua utilizando F01–F04 com semântica antiga

A seção de padrões ainda define:

- F01 = dashboard;
- F02 = upload;
- F03 = detalhamento;
- F04 = exportação.

Na Entrega 11, os IDs das telas possuem outro significado.

Isso afeta diretamente AU05, os achados heurísticos e qualquer decisão de melhoria.

Corrijam a convenção antes de encerrar o projeto.

### 29. As hipóteses H05, H07, H10 e H11 continuam “fechadas” sem evidência coerente

A Entrega 14 finalmente produziu dados reais com docentes.

Esse seria um bom momento para atualizar hipóteses relevantes com evidências empíricas.

Por exemplo:

- momento de uso antes/depois da aplicação;
- familiaridade tecnológica;
- entendimento de métricas;
- uso de dados reais.

Entretanto, a `RASTREABILIDADE.md` ainda utiliza justificativas antigas como cenário hipotético ou “não tem” e mantém hipóteses fechadas.

Não desperdicem a evidência obtida nesta entrega.

Atualizem a matriz com o que os participantes realmente demonstraram.

### 30. O checklist precisa refletir o que realmente aconteceu

Alguns itens estão marcados como atendidos de maneira forte demais.

Em especial:

> “Participantes são representativos do público”

Há um proxy.

> “Moderadores não ensinaram o caminho”

Houve múltiplas intervenções.

> “Achados geram recomendações e atualização da rastreabilidade”

A rastreabilidade ainda não possui AU01–AU06.

O checklist deve funcionar como última auditoria do projeto, não como confirmação automática.

## Recomendações de melhoria

### 1. Preserve os dados brutos antes de corrigir a consolidação

Não apaguem os registros originais.

Corrijam:

- IDs;
- tempos;
- classificação de sucesso;
- escala de satisfação;

mantendo histórico de como a versão anterior foi produzida.

### 2. Produzam uma pequena regra de codificação de sucesso

Antes de recalcular, escrevam algo como:

- total = concluiu todos os critérios sem ajuda;
- parcial = concluiu com ajuda ou não atingiu algum critério secundário;
- falha = não atingiu o objetivo principal.

Depois apliquem exatamente a mesma regra aos seis casos.

### 3. Separem resultados dos docentes e do proxy quando discutirem utilidade pedagógica

Podem manter os três participantes na análise exploratória de interação.

Mas, ao falar de rotina docente e valor pedagógico, deem destaque aos resultados dos dois professores.

### 4. Transformem os achados em decisões verificáveis

Para cada AU, registrem:

- o que será alterado;
- em qual tela;
- qual versão contém a correção;
- como verificarão se a mudança resolveu o problema.

Isso fecha adequadamente o ciclo de engenharia de usabilidade.

## Pontos que devem alimentar o fechamento do projeto

- **MU01:** recalcular após corrigir sucesso total/parcial.
- **MU02:** declarar não avaliada, salvo se houver uma sessão posterior com intervalo.
- **MU03:** recalcular tempos após corrigir registros inválidos e definir média/mediana.
- **MU04:** consolidar erros, ajudas e capacidade de recuperação com a mesma regra para todos.
- **MU05:** documentar fórmula e instrumento usados para gerar a satisfação.
- **Interface:** tornar informações necessárias visíveis sem depender exclusivamente de hover.
- **Interface:** melhorar explicações do gráfico de correlação.
- **Interface:** explicitar estados de processamento e análises indisponíveis.
- **Interface:** esclarecer campos obrigatórios e dados reais inseridos manualmente.
- **Interface:** revisar nomenclaturas como “Mediana da caracteres”.
- **Interface:** revisar cores, contraste de legendas e organização da página.
- **Rastreabilidade:** incluir AU01–AU06 e as decisões tomadas.
- **Ética:** harmonizar consentimento, gravação e período de descarte.
- **Relatório final:** separar claramente evidência obtida com docentes de evidência obtida com participante proxy.

## Síntese das ações recomendadas

1. **Reclassificar todos os seis resultados de tarefa usando a regra “sucesso total = sem auxílio”, já definida pela própria equipe.**
2. **Recalcular as taxas de sucesso após essa correção.**
3. **Corrigir os tempos inválidos de U02 e recalcular os tempos consolidados.**
4. **Definir se “tempo típico” significa média ou mediana e aplicar a mesma regra.**
5. **Documentar a origem e o cálculo das porcentagens de satisfação.**
6. **Corrigir a escala alterada no pós-teste de U03.**
7. **Padronizar os participantes como U01, U02 e U03 em todos os instrumentos.**
8. **Não reutilizar P01/P02/P03, que já identificam personas.**
9. **Tratar U02 explicitamente como proxy também na análise quantitativa/qualitativa.**
10. **Corrigir o checklist que afirma ausência de ajuda do moderador.**
11. **Corrigir o fluxograma que menciona UT03.**
12. **Usar no documento principal as tarefas mais neutras do roteiro de teste.**
13. **Tornar UT02 realmente específica para o cenário pós-aplicação.**
14. **Declarar MU02 como não avaliada, caso não tenha havido reaplicação após intervalo.**
15. **Não afirmar atendimento de MU03 até corrigir os tempos.**
16. **Dar maior destaque ao problema de informações essenciais escondidas em hover.**
17. **Corrigir AU05 para apontar às telas de resultados, e não F01/upload.**
18. **Revisar a comparação com a heurística usando a consolidação corrigida da Entrega 13.**
19. **Resolver a contradição entre relato de gravação de áudio e o termo de consentimento.**
20. **Padronizar o período de descarte dos dados.**
21. **Atualizar a `RASTREABILIDADE.md` com AU01–AU06, telas afetadas e melhorias.**
22. **Revisar as hipóteses usando as evidências reais obtidas com os docentes.**
23. **Refazer o checklist após as correções.**

A equipe conseguiu chegar ao ponto mais importante de todo o ciclo: colocou pessoas reais diante da aplicação e encontrou problemas que não apareceram apenas olhando para as telas. Isso é exatamente o valor de um teste de usabilidade. Agora vem a parte menos “bonita”, mas cientificamente indispensável: respeitar os próprios dados. Se o participante precisou de três ajudas, isso não diminui o trabalho de vocês - pelo contrário, é um achado valioso. O que enfraquece a avaliação é chamar esse caso de “sucesso total” apenas para melhorar a porcentagem. O teste fica melhor quando o dado desconfortável continua sendo dado. 🙂
