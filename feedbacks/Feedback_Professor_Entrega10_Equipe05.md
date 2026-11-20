# Feedback do Professor > Entrega 10 > Equipe 05

## Avaliação geral

A equipe atende à responsabilidade quantitativa da Entrega 10. Existem três integrantes identificados e foram apresentados três diagramas MoLIC distintos, cada um com autoria explícita:

M01 foi elaborado por Luana Bortko Rodrigues; M02, por Beatriz Manaia Lourenço Berto; e M03, por Nuno Martins Guilhermino da Silva.

Portanto, nesta entrega não há aluno sem diagrama e não há situação de um único diagrama compartilhado que justificaria divisão da nota pelo número de integrantes.

Visualmente, os três diagramas procuram seguir a notação ensinada na disciplina. A equipe utiliza cenas com título e diálogos/signos, acessos ubíquos em cinza, caixas pretas para processamento, falas de transição identificadas com `u:` ou `d:`, caminhos tracejados para alternativas/rupturas e registros de `gco` e `gcc`. Isso é importante porque os diagramas não foram produzidos simplesmente como fluxogramas de telas.

Entretanto, ainda existem problemas conceituais e de rastreabilidade que precisam ser corrigidos. O mais grave está em M03: o documento declara que o diagrama modela `O03`, porém `O03` na Entrega 09 é “analisar duas provas para verificar se não há discrepâncias de exigência”. O diagrama M03, na realidade, modela consulta de métricas, filtros e exportação. Além disso, há uma transição que sai de uma caixa preta rotulada como `u: Habilitar filtros`, o que contraria diretamente a notação: uma caixa preta representa processamento interno e suas saídas devem ser falas do preposto/sistema, portanto `d:`.

Também há um problema de continuidade entre Entregas 09 e 10. O cenário CI03 da Entrega 09 descrevia uma conversa específica de comparação entre duas versões de avaliação. Na consolidação da Entrega 10, porém, a equipe afirma que a comparação automática não faz parte do escopo e que basta repetir o fluxo de análise. Essa mudança pode ser válida, mas precisa ser assumida como mudança de escopo, justificada e refletida na Entrega 09 e na rastreabilidade. Hoje os artefatos contam histórias diferentes.

M01 e M02 estão conceitualmente mais próximos da notação solicitada, embora ainda existam pontos de melhoria na identificação dos signos dentro das cenas e na ligação explícita com o Design Centrado na Comunicação da Entrega 09.

## Pontos positivos

A quantidade de diagramas exigida foi atendida e a autoria está identificada individualmente.

Os arquivos dos três diagramas estão armazenados em `assets/10_molic/` e puderam ser analisados diretamente no repositório.

Os três diagramas utilizam a linguagem visual característica da MoLIC trabalhada em aula, com cenas, acessos ubíquos, processamento interno, falas de transição e caminhos alternativos.

M01 modela de forma compreensível o preenchimento dos dados necessários à análise, incluindo duração, dificuldade das questões, velocidade de leitura e métricas reais.

M01 possui um tratamento explícito para duração superior ao limite e permite retorno à cena de preenchimento.

M02 apresenta um fluxo principal claro para envio e validação da prova.

M02 inclui cancelamento, arquivo inválido, ausência de questões, tamanho de arquivo e erro de servidor como alternativas/rupturas, evitando um diagrama limitado ao happy path.

M02 utiliza corretamente a caixa preta como processamento do arquivo e apresenta saídas do processamento com `d:`.

M03 representa consulta das métricas, filtragem e exportação, além de tentar modelar indisponibilidade de informação.

Os três diagramas utilizam acesso ubíquo, dispensando a necessidade de uma abertura exclusivamente por ponto inicial preto.

A leitura textual dos diagramas procura explicar caminho principal e alternativas, o que ajuda a verificar a intenção da modelagem.

## Correções prioritárias

### 1. Corrigir imediatamente o objetivo declarado de M03

M03 está identificado como:

`Objetivo(s): O03`

Entretanto, na Entrega 09, `O03` significa analisar duas provas para verificar se existem discrepâncias de exigência.

O diagrama M03 não modela isso.

Ele modela principalmente:

consultar as métricas da prova, filtrar informações, compreender resultados e exportar resultados.

Na própria Entrega 09 existem objetivos específicos associados a essas atividades, especialmente os objetivos relacionados a consultar métricas, explorar resultados e compreender resultados.

Portanto, a equipe precisa corrigir a identificação do objetivo de M03 e revisar todas as referências posteriores.

Esse não é um pequeno erro de numeração. O identificador é o mecanismo que permite saber qual objetivo originou a conversa. Se `O03` aponta para comparação de duas provas e o diagrama mostra filtros de uma única prova, a rastreabilidade deixa de ser confiável.

### 2. M03 possui uma saída de processamento interno com `u:`, o que está incorreto

No diagrama M03, depois de `u: Enviar filtros`, há uma caixa preta de processamento.

Uma das transições que sai dessa caixa está rotulada:

`u: Habilitar filtros`

Isso não pode ocorrer dessa forma.

A caixa preta representa processamento interno do sistema. Quando ela determina o rumo da conversa, a saída deve ser uma fala do sistema/preposto, identificada com `d:`.

Se “habilitar filtros” for uma ação do usuário, essa ação deve sair de uma cena em que o usuário esteja conversando com o sistema, e não da caixa preta.

Se for o sistema que habilita os filtros depois do processamento, a transição deve comunicar isso com `d:`.

Esse ponto precisa ser corrigido no próprio diagrama, pois é uma regra estrutural da notação.

### 3. O fechamento `gcc` de M03 está associado ao momento errado da conversa

O objetivo declarado no próprio diagrama é:

`gco: Consultar as métricas/análise da prova`

Entretanto, o `gcc` aparece associado à região de exportação.

Isso faz parecer que o objetivo “consultar métricas/análise” só é concluído quando o usuário escolhe um formato de exportação.

Essa relação não faz sentido com o próprio caminho principal descrito pela equipe. O texto afirma que o usuário pode consultar as métricas “sem a necessidade de aplicar filtros”. Da mesma forma, exportar também deveria ser uma possibilidade instrumental e opcional, não uma condição obrigatória para concluir a consulta.

A equipe precisa decidir qual é exatamente a garantia de sucesso do objetivo e posicionar o `gcc` no momento em que esse objetivo realmente foi satisfeito.

Se exportação constituir outro objetivo, ela deve ser tratada como mudança de objetivo/conversa, e não como requisito para concluir a consulta.

### 4. A transição `u: explorar resultados` de M03 leva para “Exportar arquivo”

No diagrama M03, a transição que parte da cena “Consultar métricas da prova” em direção à cena “Exportar arquivo” está indicada como:

`u: explorar resultados`

Essa fala não corresponde ao destino.

Explorar resultados e exportar resultados são intenções diferentes.

Se o usuário está explorando resultados, a conversa deveria permanecer no espaço de consulta, detalhamento, filtros ou interpretação.

Se o usuário deseja exportar, a fala de transição precisa comunicar essa intenção.

Em MoLIC, uma seta não serve apenas para conectar duas caixas. A fala de transição deve explicar por que a conversa mudou de tópico.

### 5. A equipe precisa resolver a contradição sobre CI03 e comparação de duas provas

Na Entrega 09, CI03 foi criado especificamente para comparar duas versões de uma avaliação.

A conversa previa:

envio da Versão A; envio da Versão B; consulta dos dois relatórios; comparação das métricas; decisão de ajustes; reanálise da versão modificada.

Na Entrega 10, a consolidação afirma que:

“a comparação não é realizada automaticamente pelo sistema”

e que a solução é manter a modelagem atual, repetindo o fluxo para cada prova.

Essa decisão altera significativamente a solução concebida na Entrega 09.

Isso pode acontecer em um processo iterativo, mas não pode acontecer silenciosamente.

A equipe precisa escolher uma direção:

ou CI03 continua fazendo parte do escopo e então um MoLIC precisa representar adequadamente a conversa de comparação;

ou a comparação deixa de fazer parte do escopo e então CI03, O03 e a rastreabilidade precisam ser revisados, com justificativa da mudança.

Atualmente, a Entrega 09 promete uma conversa que a Entrega 10 não modela.

### 6. A consolidação superestima a cobertura de O01, O02 e O03

Na consolidação, a equipe afirma que O01, O02 e O03 são cobertos conjuntamente por M01, M02 e M03.

Isso precisa ser revisto.

M01, M02 e M03 dividem um fluxo de:

enviar prova → informar dados → consultar métricas.

Esse conjunto pode apoiar diferentes cenários, mas isso não significa automaticamente que todos os objetivos finais foram modelados.

O03, em particular, é comparação entre duas provas e não está representado no conjunto atual.

Além disso, O01 e O02 possuem motivações diferentes:

O01 trata da análise antes da aplicação;

O02 trata da análise depois de um desempenho abaixo do esperado.

Se o mesmo fluxo serve aos dois objetivos, a equipe deve mostrar onde as conversas diferem, especialmente no uso de dados reais de desempenho, na interpretação dos resultados e na conclusão do objetivo.

Não basta escrever “M01, M02, M03” em todas as linhas da consolidação.

### 7. M01 está associado a CI01, mas sua conversa corresponde muito mais claramente a CI02

M01 é “Informar dados necessários para a análise”.

Na Entrega 09, o Design Centrado na Comunicação de CI02 possui explicitamente o subtópico:

“Informar dados da avaliação para iniciar a análise”.

Já CI01, na sua tabela de Design Centrado na Comunicação, concentra-se em:

enviar e validar avaliação; tratar problemas no upload; compreender métricas; explorar resultados; filtrar análises; interpretar pontos de atenção.

Portanto, a origem declarada de M01 como CI01 precisa ser justificada ou corrigida.

A relação com o cenário não deve ser escolhida apenas porque todos utilizam T01. O MoLIC precisa derivar das conversas definidas anteriormente.

### 8. Revisar a utilização dos signos dentro das cenas de M01

M01 apresenta bons exemplos de signos dentro das cenas, como duração, tempo de leitura, dificuldade e métricas reais.

Entretanto, a cena tracejada de erro contém apenas:

“Erro5: Duração máxima de 6h excedida”

sem estruturar esse conteúdo com a mesma lógica de signo do preposto utilizada nas demais cenas.

A mensagem de erro é informação comunicada pelo sistema e deve aparecer claramente como signo/fala do preposto.

Além disso, “Informação dos inputs” contém apenas uma explicação genérica sobre “importância do input”. O modelo deveria indicar que conceito está sendo explicado: duração, dificuldade, velocidade de leitura, métricas reais etc.

A equipe deve preservar o vínculo com o esquema conceitual de signos da Entrega 09.

### 9. M02 usa a notação de modo razoável, mas precisa melhorar os signos da cena de erro

M02 possui um bom fluxo de ruptura e recuperação.

Porém, a cena tracejada de erro contém uma lista interna:

Erro1, Erro2, Erro3 e Erro4.

Isso funciona como anotação para os projetistas, mas a MoLIC precisa representar o que o preposto efetivamente comunica ao usuário.

“server error”, por exemplo, é uma formulação orientada à implementação.

A mensagem deve usar linguagem adequada ao professor e permitir que ele compreenda:

o que aconteceu; o que foi afetado; e qual ação é possível para continuar.

O próprio material da equipe já está tentando fazer isso na descrição textual. Falta refletir melhor essa comunicação no diagrama.

### 10. Corrigir a inconsistência do erro de “arquivo excede tamanho” na explicação de M02

Na seção textual de alternativas de M02, a situação “Arquivo excede o tamanho permitido” é descrita como sendo percebida pelo usuário através de:

“mensagem informando que ocorreu um erro interno e que não foi possível concluir o processamento”.

Isso não corresponde ao problema.

Se o arquivo excedeu o tamanho permitido, a comunicação deveria explicar especificamente essa condição.

Erro de validação de entrada e erro interno de servidor são rupturas distintas e devem produzir mensagens e recuperações distintas.

### 11. Em M03, “Filtros desabilitados” e “nenhuma análise selecionada” estão sendo tratados como se fossem o mesmo problema

O texto da entrega descreve um caminho alternativo em que o usuário:

“desmarca todas as análises”.

O diagrama, entretanto, utiliza:

`d: Filtros desabilitados`.

Essas situações são diferentes.

“Nenhum filtro selecionado” significa que o usuário realizou uma seleção vazia.

“Filtros desabilitados” significa que o sistema não permite utilizar os filtros naquele estado.

A equipe precisa definir qual ruptura realmente está modelando e usar a mesma terminologia no diagrama, na leitura textual e no esquema de signos.

### 12. M03 ainda expõe BERT/RoBERTa como parte da conversa com o professor

A cena principal de M03 inclui explicitamente:

`BERT/RoBERTa`

ao explicar métricas indisponíveis.

Esse problema já aparecia no esquema de signos da Entrega 09.

O professor usuário não precisa necessariamente conhecer qual modelo interno de processamento falhou.

A conversa deve ser orientada ao efeito sobre a tarefa, por exemplo:

determinada métrica não pôde ser calculada; parte da análise está temporariamente indisponível; ou o processamento textual não foi concluído.

Detalhe técnico interno só deve aparecer se existir evidência de que ele é relevante para a decisão do usuário.

### 13. Os três diagramas aproximam-se visualmente da notação ensinada, mas a equipe ainda precisa cuidar da semântica, não apenas da aparência

Este é um ponto importante.

Os diagramas utilizam corretamente vários elementos gráficos da linguagem:

cenas; caixas de processamento; acesso ubíquo cinza; transições; caminhos tracejados.

Isso é positivo.

Entretanto, um MoLIC não fica correto apenas porque “parece um MoLIC”.

A semântica dos elementos também precisa estar correta:

uma caixa preta não produz `u:`; um `gcc` precisa indicar conclusão real do objetivo; uma fala de transição precisa explicar a mudança de tópico; uma cena precisa representar uma conversa; e objetivos precisam permanecer coerentes com a Entrega 09.

A equipe está relativamente perto da forma correta, mas precisa revisar a lógica interna dos diagramas.

### 14. Revisar a rastreabilidade de M01, M02 e M03

A `RASTREABILIDADE.md` já passou a mencionar os MoLICs, o que é um avanço.

Entretanto, ela associa CI01, CI02 e CI03 a M01/M02/M03 de maneira muito ampla.

Por exemplo, R01 associa os três cenários a M03.

R02 associa os três cenários a M01 e M02.

Isso sugere uma cobertura que os diagramas não demonstram integralmente.

Se CI03 permanecer no projeto, deve existir rastreabilidade específica para a comparação.

Se CI03 for retirado, as relações precisam ser atualizadas.

A rastreabilidade precisa descrever o que realmente está representado, e não o que se gostaria que os diagramas cobrissem.

### 15. Resolver definitivamente a numeração O09/O10

Na Entrega 09 havia inconsistência entre `O09`, `O10` e `O010`.

Na Entrega 10, a consolidação utiliza O09 e O10.

Antes de avançar, a equipe precisa consolidar uma única convenção e atualizar todos os documentos.

Esse tipo de erro parece pequeno, mas passa a ser especialmente problemático agora, porque o Figma e as avaliações deverão apontar de volta para esses objetivos.

### 16. O caminho de ajuda de M01 pode permanecer como alternativa, mas precisa ser semanticamente justificado

M01 utiliza linhas tracejadas para acessar e fechar “Informação dos inputs”.

Como linhas tracejadas podem representar caminhos alternativos e rupturas, isso é aceitável se a equipe estiver modelando a ajuda como conversa alternativa.

O importante é deixar claro que ela não é uma “cena de erro”.

A ajuda deve ser tratada como uma mudança de tópico instrumental para apoiar a atividade corrente.

### 17. Revisar os checklists marcados integralmente como atendidos

M01 e M03 marcam praticamente todos os itens como concluídos.

Entretanto, a análise mostra problemas objetivos:

M03 possui saída de processamento com `u:`; o `gcc` está mal posicionado; o objetivo O03 não corresponde ao conteúdo; e a cobertura de CI03 não está demonstrada.

O checklist deve ser utilizado como autoverificação real.

Marcar todos os itens como atendidos não substitui conferir a semântica do diagrama.

## Recomendações de melhoria

### 1. Fazer uma revisão “seta por seta”

Antes de considerar cada diagrama concluído, a equipe deve percorrer todas as transições perguntando:

Quem motivou esta mudança de tópico?

Se foi o usuário, a fala deve ser `u:`.

Se foi uma decisão ou comunicação automática do sistema, deve ser `d:`.

Essa revisão simples identificaria imediatamente o problema de `u: Habilitar filtros` saindo da caixa preta de M03.

### 2. Fazer uma revisão “cena por cena”

Para cada cena, verifiquem:

qual é o tópico da conversa; quais signos o usuário fornece; quais signos o sistema apresenta; quais falas permitem sair daquela cena.

Se a caixa contém apenas o nome de uma tela, ela ainda não está suficientemente modelada como conversa.

### 3. Fazer uma revisão “objetivo por objetivo”

Comecem pelo `gco`.

Depois perguntem:

em que momento o usuário pode dizer “consegui o que eu queria”?

Esse é o ponto candidato ao `gcc`.

Não utilizem exportação como fechamento de uma consulta se exportar é opcional.

### 4. Usar a Entrega 09 como fonte real, não apenas como referência nominal

Cada MoLIC deveria conseguir apontar para:

um cenário de interação; um tópico do Design Centrado na Comunicação; os signos utilizados naquela conversa; o objetivo correspondente.

Se essa ligação não puder ser demonstrada, provavelmente existe inconsistência entre as entregas.

### 5. Evitar linguagem interna de desenvolvimento nas rupturas

“Server error”, “BERT” e “RoBERTa” podem ser úteis para logs técnicos, mas não devem automaticamente se transformar na fala do preposto para o professor.

A conversa da interface deve explicar a situação no vocabulário necessário para a tarefa.

## Pontos que devem alimentar as próximas entregas

Antes de materializar os fluxos no Figma, a equipe precisa corrigir a semântica de M03 e resolver o escopo de CI03.

O Figma não deve simplesmente reproduzir os problemas atuais do MoLIC.

A equipe deve preservar no protótipo os estados já identificados de upload, validação, processamento, erro e recuperação.

As telas de métricas devem derivar de cenas e signos corrigidos, principalmente no que diz respeito a filtros, explicações e exportação.

Se a comparação entre duas provas permanecer no escopo, o protótipo precisará materializar uma conversa que hoje não está adequadamente modelada no MoLIC.

Se a comparação for retirada do escopo, essa decisão deverá ser registrada antes de avaliar o protótipo.

As futuras avaliações devem testar as rupturas representadas no MoLIC, principalmente arquivo inválido, ausência de questões, erro de processamento, duração inválida e estados de filtragem.

A rastreabilidade deve ser corrigida antes das próximas entregas para que MoLIC, Figma e testes apontem para os mesmos objetivos.

## Síntese das ações recomendadas

1. Corrigir M03 para apontar para o objetivo realmente modelado, e não para O03.
2. Corrigir `u: Habilitar filtros` saindo da caixa preta; saída de processamento deve ser `d:`.
3. Reposicionar o `gcc` de M03 no momento em que o objetivo de consulta efetivamente é concluído.
4. Corrigir `u: explorar resultados` levando para a cena de exportação.
5. Decidir formalmente se CI03/comparação de duas provas permanece no escopo.
6. Se CI03 permanecer, criar/modelar a conversa de comparação; se sair, atualizar Entrega 09 e rastreabilidade.
7. Revisar a origem de M01, pois “Informar dados da avaliação” está explicitamente associado a CI02 na Entrega 09.
8. Melhorar a representação dos signos nas cenas de erro de M01 e M02.
9. Diferenciar claramente “nenhum filtro selecionado” de “filtros desabilitados” em M03.
10. Evitar BERT/RoBERTa e “server error” como linguagem voltada ao professor.
11. Rever a consolidação de cobertura de O01, O02 e O03.
12. Corrigir e estabilizar O09/O10 em todas as entregas.
13. Atualizar a rastreabilidade para refletir a cobertura real dos diagramas.
14. Reexecutar os checklists depois das correções, em vez de manter itens marcados que o próprio diagrama contradiz.

A equipe já deu um passo importante: os diagramas têm aparência de MoLIC e incorporam boa parte dos elementos gráficos trabalhados em aula. Agora é preciso garantir que eles também **pensem como MoLIC**. A caixa preta não pode falar como usuário, o `gcc` não pode aparecer só porque “faltava colocar um gcc” e um objetivo não pode mudar de significado entre duas entregas. A notação existe justamente para tornar explícita a conversa. Quando cada seta consegue responder claramente “quem falou o quê, por que o tópico mudou e qual objetivo está sendo perseguido?”, o diagrama deixa de ser apenas um desenho bem organizado e passa a ser um modelo de interação.
