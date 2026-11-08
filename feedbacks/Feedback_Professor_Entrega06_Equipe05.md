# Feedback do Professor > Entrega 06 > Equipe 05

A equipe entregou uma solução integrada de prototipação e manteve os artefatos visuais dentro do repositório. Em `assets/06_prototipos/` há oito estados do protótipo original e sete imagens correspondentes a ajustes posteriores, totalizando 15 imagens relevantes para esta entrega. Portanto, o requisito essencial de existir material visual do protótipo foi atendido.

As telas representam um fluxo coerente com a tarefa T01 da Entrega 05: selecionar/enviar a prova, informar a duração, lidar com uma condição de erro, habilitar a análise, visualizar métricas, consultar explicações e acessar opções de exportação. A escolha de C02/T01 como recorte também é adequada porque T01 era, entre as tarefas anteriores, a mais bem sustentada pelo problema central do projeto.

A equipe também documentou uma alteração concreta depois da simulação: a entrada de duração foi simplificada, eliminando o dropdown de horas/minutos e reduzindo estados do fluxo. Essa é exatamente a natureza esperada da prototipação em baixa fidelidade: construir, simular, perceber um problema e revisar rapidamente a interação.

Entretanto, a entrega ainda precisa de revisão importante em três pontos. Primeiro, o walkthrough está documentado de forma fraca: sete das oito observações estão registradas como “Nenhuma”, e praticamente todas as linhas recebem a mesma consequência de design, mesmo quando a tela observada não tem relação com o campo de duração. Segundo, a seção 5 apresenta várias linhas em que “Problema”, “Depois” e “Justificativa” não demonstram uma alteração efetivamente derivada de observação. Terceiro, ainda há inconsistências de numeração, referências de imagens e texto residual de discussão interna no documento.

A Entrega 06 tem material suficiente para ser válida, mas o valor pedagógico da atividade está menos na quantidade de telas e mais na demonstração de que a equipe **simulou o fluxo, observou comportamento/dificuldades e alterou a solução em consequência disso**. É justamente esse encadeamento que precisa ficar mais claro.

## Pontos positivos

- O protótipo foi mantido no próprio repositório, dentro de `assets/06_prototipos/`.
- Existem imagens do fluxo original e das versões ajustadas.
- O protótipo permanece em baixa fidelidade e não tenta antecipar acabamento visual de alta fidelidade.
- O escopo foi reduzido para P01/P03, C02 e T01, em vez de tentar prototipar simultaneamente todas as funcionalidades discutidas nas entregas anteriores.
- A escolha de T01 é coerente com o núcleo do projeto: analisar uma avaliação antes de sua aplicação.
- O fluxo possui início, desenvolvimento e estado de resultado.
- A equipe representou um estado de erro relacionado à duração informada, em vez de mostrar apenas o caminho feliz.
- Há uma condição de habilitação do botão “Analisar”, o que demonstra preocupação com o estado da interação.
- O dashboard contém diferentes formas de apresentação das métricas.
- Existe mecanismo de detalhamento/explicação por meio de ícone informativo.
- A equipe representou opções de exportação.
- A simulação gerou pelo menos uma mudança concreta e visível: simplificação da entrada de duração e eliminação do dropdown.
- As imagens ajustadas demonstram que a equipe não tratou o primeiro desenho como versão definitiva.

## Correções prioritárias

### 1. Corrigir a documentação do walkthrough

Este é o ponto mais importante da entrega.

O item 4 deveria demonstrar o ciclo:

**simular → observar → registrar dificuldade/comportamento → decidir mudança**

No documento atual, quase todas as linhas possuem “Observação: Nenhuma”.

Isso não seria necessariamente um problema se a consequência também fosse “nenhuma alteração”. Porém, em praticamente todas as telas aparece como consequência:

> “alterar input baseado no feedback da tela do fluxo3”

Essa mesma consequência é repetida inclusive em telas de dashboard, detalhamento e exportação, que não têm relação direta com o input de duração.

Isso impede compreender o que foi realmente observado em cada etapa.

A equipe deve reescrever o walkthrough tela por tela:

- o que a pessoa tentou fazer;
- o que ela fez;
- se hesitou, perguntou, errou ou realizou sem dificuldade;
- o que foi dito espontaneamente;
- se a ação ocorreu como esperado;
- qual consequência concreta surgiu para aquela tela.

Quando realmente não houver problema, registrem explicitamente que **a interação foi compreendida e nenhuma alteração foi necessária**. Não atribuam a uma tela uma mudança causada por outra.

### 2. Identificar melhor como a simulação foi realizada

A entrega afirma que foi realizada uma simulação com uma pessoa que não participou da elaboração das telas, mas não registra:

- quem era o participante ou ao menos qual seu perfil;
- se era colega, docente ou outro participante;
- quem conduziu a simulação;
- quais instruções foram dadas;
- se o participante recebeu uma tarefa ou apenas percorreu as telas;
- como as observações foram registradas.

Não é necessário identificar nominalmente a pessoa. O importante é deixar o procedimento reproduzível.

A equipe deve acrescentar uma breve descrição do walkthrough antes das observações.

### 3. Não utilizar a própria tela como única “evidência” da observação

Na coluna “Evidência”, todas as linhas apontam novamente para a imagem do protótipo.

A imagem prova que a tela existe, mas não prova o que aconteceu durante a simulação.

A evidência do walkthrough poderia ser, por exemplo:

- anotação feita durante a sessão;
- comentário registrado pelo participante;
- fotografia da execução, quando permitido;
- registro textual da hesitação ou dificuldade;
- anotação do observador;
- marcação no protótipo;
- outro registro produzido durante a simulação.

Se não houver evidência adicional, ao menos o texto deve deixar claro que se trata de **registro de observação**, e não de imagem da tela utilizada.

### 4. Corrigir a seção 5 para mostrar somente alterações reais

Na seção “Alterações após a simulação”, várias linhas declaram “Nenhuma” como problema e “Nenhuma observação de melhoria” como justificativa.

Se não houve problema e não houve mudança, essa linha não representa uma alteração após a simulação.

A seção deve registrar apenas os casos em que ocorreu:

**Antes → problema observado → Depois → justificativa**

O caso da duração é um bom exemplo e deve ser preservado.

Já as telas de dashboard, tooltip e exportação, quando permaneceram iguais, não precisam aparecer como se tivessem sido alteradas.

### 5. Explicar melhor a alteração realizada no campo de duração

A equipe identificou corretamente que o modelo anterior de entrada de duração, com dropdown para hora/minuto, criava complexidade.

A mudança para um campo único simplifica a interface, mas o próprio documento registra uma consequência importante: o usuário pode precisar converter mentalmente horas/minutos.

Esse ponto merece ser tratado com mais cuidado.

A revisão não deve parar em “tiramos o dropdown”. É necessário verificar se o novo formato realmente reduz esforço para o docente ou apenas transfere a complexidade.

Essa questão pode ser retomada em nova simulação ou posteriormente na avaliação da interface.

### 6. Corrigir a numeração das telas e estados

A documentação apresenta inconsistências:

- existem dois estados chamados `P04`;
- a sequência mistura `P04 Warning` e novamente `P04`;
- algumas imagens e descrições de estados não correspondem perfeitamente à numeração;
- P03 referencia novamente `prototipo_fluxo_02.jpeg`, embora sua descrição indique outro estado.

Cada estado precisa possuir um identificador único.

Sugiro revisar toda a sequência P01–P08 e garantir que:

- cada ID corresponda a uma única imagem;
- a legenda descreva aquela imagem;
- referências futuras utilizem sempre o mesmo ID.

### 7. Corrigir a renderização do estado P07

No item P07, o link para o protótipo foi escrito como link Markdown comum:

`[Protótipo tooltip informações](...)`

enquanto os demais utilizam sintaxe de imagem:

`![...](...)`

Isso faz com que P07 não seja renderizado da mesma forma que os demais estados no Markdown.

A equipe deve padronizar a inclusão das imagens.

### 8. Revisar o fluxo PF01 para descrevê-lo como interação, não como hipótese científica

No item 2, PF01 foi descrito como:

> “Analisar se características específicas da prova impactariam o desempenho dos alunos”.

Essa frase representa mais diretamente a questão/contribuição do TCC do que o fluxo de interação da interface.

O fluxo prototipado é mais concreto: o docente submete uma avaliação, informa dados necessários, solicita a análise e interpreta os resultados.

A equipe deve manter a relação com a contribuição científica, mas descrever PF01 como **fluxo de interação do usuário**.

### 9. Evitar afirmar que o protótipo “avalia impacto” se a interface apresenta estimativas ou métricas

A justificativa do fluxo diz que a solução busca avaliar se características como quantidade de palavras, presença de imagens, tempo, formalidade, ordem das questões e distratores “podem influenciar o desempenho”.

É importante manter a precisão do que o TCC efetivamente consegue inferir.

Na interface, a equipe deve deixar claro se está:

- apresentando métricas estruturais;
- apresentando estimativas;
- mostrando relações derivadas do modelo;
- ou efetivamente demonstrando causalidade.

Essa diferença é importante para evitar que o docente interprete os resultados com confiança maior do que a evidência permite.

### 10. Revisar as famílias de interface marcadas como não aplicáveis

A equipe marcou:

- configuração/parametrização: ❌
- acompanhamento de execução: ❌

Entretanto, o próprio protótipo solicita pelo menos um parâmetro — duração da prova — e possui um momento de processamento entre “Analisar” e a apresentação do dashboard.

Isso não significa que a equipe tenha obrigação de criar telas específicas para configuração ou acompanhamento.

O ponto é apenas conceitual: existe parametrização no fluxo, ainda que mínima. A classificação deve refletir o que o protótipo realmente faz.

### 11. Relacionar explicitamente as telas às subtarefas corrigidas de T01

A entrega declara que cobre T01, mas poderia demonstrar melhor a continuidade.

O fluxo possui correspondência clara com partes do HTA/GOMS/CTT:

- seleção do arquivo;
- envio da prova;
- informação de duração;
- análise;
- consulta das métricas;
- detalhamento;
- exportação.

A equipe deve utilizar essa relação para justificar cada estado.

Isso também ajudará a identificar elementos que entraram no protótipo sem necessidade comprovada.

### 12. Atualizar a rastreabilidade com a Entrega 06

A matriz já possui padrões F01–F04 — dashboard, upload, detalhamento e exportação — mas ainda não registra as telas produzidas nesta entrega.

Os campos de telas permanecem como “Pendente” na rastreabilidade entre capacidade, necessidade e artefatos.

Agora já existem artefatos concretos.

A equipe deve atualizar as relações para que seja possível percorrer:

**necessidade → cenário → tarefa → modelo de tarefa → estado/tela do protótipo**

Não é necessário antecipar Figma ou teste final, mas a prototipação em papel já deve aparecer na cadeia de rastreabilidade.

### 13. Corrigir a afirmação de status da entrega

No cabeçalho aparece:

> “Concluída (não teve nenhua sugestão de melhoria no feedback, apenas elogios)”

Esse comentário não deve fazer parte do status do artefato.

O status deve indicar o estágio documental da entrega, não registrar uma interpretação sobre avaliação recebida.

Além disso, a própria versão atual possui várias questões que precisam de revisão, principalmente no walkthrough.

Utilizem algo simples como “concluída”, “revisada” ou equivalente.

### 14. Remover comentários internos e dúvidas residuais do documento final

Permanecem comentários como:

- “designcocneitual”;
- “??????”;
- “ta certo isso??”;
- observações sobre o que deveria ser colocado em assets;
- dúvidas internas sobre como descrever os fluxos.

Esses comentários mostram o processo de elaboração, mas não devem permanecer na versão final destinada à documentação do projeto.

A equipe precisa fazer uma última leitura antes da entrega e remover notas de trabalho.

## Recomendações de melhoria

### 1. Fazer uma segunda simulação rápida depois da alteração do input

Como a principal modificação foi o campo de duração, seria bastante útil repetir especificamente essa parte do fluxo com outra pessoa ou com a mesma pessoa em uma nova rodada.

O objetivo seria verificar se a solução simplificada realmente resolveu a dificuldade.

### 2. Observar também as telas de resultado

O walkthrough aparentemente encontrou dificuldade apenas na entrada de duração.

Entretanto, o dashboard é conceitualmente a parte mais crítica do projeto, porque exige interpretação de métricas.

Em uma próxima avaliação, não se limitem a perguntar se a pessoa “consegue clicar”. Observem:

- o que ela entende de cada métrica;
- qual informação procura primeiro;
- se compreende os gráficos;
- se utiliza o ícone de informação;
- se a explicação realmente ajuda;
- o que conclui a partir dos resultados.

### 3. Não transformar “tooltip” em solução obrigatória antes de avaliar compreensão

O ícone de informação faz sentido como hipótese de design e já apareceu nas entregas anteriores.

Agora que existe um protótipo, é possível testar se o participante:

- percebe o ícone;
- entende para que serve;
- consegue associar a explicação à métrica;
- prefere informação contextual, legenda ou outro formato.

O objetivo não é comprovar que o tooltip estava certo, mas descobrir se ele resolve a dificuldade.

### 4. Manter a baixa fidelidade

A equipe acertou em continuar utilizando desenhos simples.

Não há necessidade de avançar visualmente antes de estabilizar fluxo, conteúdo, estados de erro e interpretação dos resultados.



A equipe produziu o artefato visual mais importante desta etapa e demonstrou capacidade de alterar rapidamente o desenho depois de uma observação. O próximo avanço é melhorar a **qualidade da evidência do walkthrough**. Prototipação em papel não é apenas desenhar telas; é usar essas telas para descobrir onde nossa ideia estava errada. Se a observação diz “Nenhuma” em quase todo o percurso, a pergunta que fica é: o usuário realmente não teve dificuldade ou nós ainda não estamos observando as coisas certas?
