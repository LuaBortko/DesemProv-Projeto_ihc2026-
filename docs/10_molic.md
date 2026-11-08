
# Entrega 10 — MoLIC

**Data:** 02/11/2026 <br>
**Status:**  🟨 Em andamento <br> 
**Responsabilidade:** 1 solução completa por integrante<br> 

## Objetivo da atividade
<!-- 
Conversas alternativas em direcao ao mesmo objetivo 
Ex: goms, de acordo com regra de selecao tem maneiras diferencas, conv alternativas em direcao a um obj 

Nos signos definimos recuperacao de rupturas, dado essa modelagem do esquema conceitual de signos planejamos mecanismos p user se recuepra de problemas 


IMPORTANTE: pre cond: xxx acima do u:, condicao necessaria pra fala de transicao ocorrer, ex analisar  so é possivel se preencher campo de input obrigatorio


IMPORTANTE: NA MODELAGEM FAZEMOS CENA DETALHADA: cena composta pelo nome do topico e dialogos q ocorrem (dialog obaseado na lista de signo q compoe o dialog

PROCESSO APOS CLICAR E MANALISAR 

IMPORTANTE: TRACEJADO para upload invalodo de pdf, tempo maior q o amx inserido…(acho)

cena comecando, carregei diretro a cena inicial 

MAPEAR INICIO E FIM DA META
,saida de caixa preta eh sempre d e oq sai da cena eh usuario 



IMPORTANTE: Gco: obj quand oentra eh ver a lsita de documentos MTO IMPROTANTE TER GCO, pde taem hta, goms...

IMPORTANTE: ACABO MODELAGEM OLHAS E TD SETA TEM FALA DE TREANSICAO (u: ou d:? Toda seta tem q ter, a uncia q n tem u: ou d: é a q sai p difurcaao (-----_ pq tem depois , pode n usa --- e puxa as 2 setas da caixa  

IMPORTANTE: Se sai da cena 90% das vezes eh u: 
Se entra no processamento (entra na caixa preta é u:, ta saind oda caixa preta é d:) 

 -->
Modelar a interação como uma **conversa entre usuário e preposto do designer**, oferecendo visão global dos caminhos que permitem ao usuário atingir seus objetivos — incluindo alternativas e rupturas relevantes. MoLIC não deve ser reduzida a um fluxograma de telas.

<!--
Comeco a faze molic consumindo mapa de objetivos. 

OBJETIVOS NUM GERAL (O01: Analisar a estrturua de uma prova antes de aplicá-la, O02: Analisar avaliação após um desempenho baixo na aplicação, O03: Comparar duas versÕes de uma avaliação para identificar possíveis diferenças injustas) É SEMPRE ANALISAR PROVA ENTAO VAMOS DIVIDIR AS TAREFAS PRA CADA UM MODELAR UMA:


O04: enviar a avaliação em PDF (é uma cena, cena pode ser uma tela, ex menu de navegacao pode ser 1 cena e pop up de avisa upload invalido pode ser outra (navegacao como cena ubiqua), 

tópico (nome da cena): só pro projetista entende oq ocorre


PRIMEIRA FUNCIONALIDADE DO MOLIC: 
Falas dde transicao: mmudanca de topico em determinado omento dainteracaosao cenas, estados do sistema, mudanca de estado sao cenas 
u: fala d etransicao do usuario ( acao q user faz q motiva a ir p outra cena, estado )

D+u-> user ta entrando input mas sistema ta ajudando user,  

D+u, faco sistema que deixo user digita estado ex: nao deixa a pessoa digitar o estado, estado fornece um dropdown pra escolher 


-->


> Use a **notação MoLIC ensinada na disciplina**. Este template foca critérios de qualidade e não substitui a legenda/notação apresentada em aula.

## Atenção a TCCs sem interface original

O MoLIC não modela o algoritmo por dentro. Ele modela a **conversa de interação necessária para que uma pessoa use a contribuição**.

Exemplos de conversas:

- usuário escolhe dados/parâmetros → sistema valida → usuário inicia análise → sistema comunica processamento → usuário interpreta resultado;
- usuário consulta histórico → refina filtros → abre execução → compara com outra;
- administrador seleciona perfil → altera permissão → sistema comunica consequências → administrador confirma/cancela;
- analista recebe alerta → examina evidências → classifica ocorrência → registra decisão.

Modele também rupturas plausíveis: entrada inválida, falha de processamento, ausência de resultado, permissão insuficiente, filtro sem resultados, conflito de alteração, cancelamento ou necessidade de recuperação.

## M01 — Informar dados necessários para a análise

**Autor(a):** Luana Bortko Rodrigues RA:24.123.006-9 <br>
**Cenário de interação de origem:** CI01 <br>
**Objetivo(s):** O05(Informar os dados necessários para a análise<br>
**Tarefa(s) relacionada(s):** T01 - Analisar a prova<br>
**Signos relevantes:** muitos<br>

### Diagrama

![MoLIC M01](../assets/10_molic/molic_m01.svg)

**Fonte editável:** [link editável](https://canva.link/tbgn4mxijuochce)

### Leitura do diagrama

Explique em texto o caminho principal e pelo menos os caminhos alternativos/rupturas mais importantes.

#### Caminho principal

Pré-condição (precond): {Arquivo de prova em PDF carregado e validado} <br>
Objetivo (gco): Informar dados da prova <br>
Garantia de Sucesso (gcc): Informar dados da prova <br>
1. Abertura do objetivo: Após a validação do upload na mesma página, o sistema habilita e exibe a cena *Informar dados da prova* logo abaixo da caixa de envio, disponibilizando os parâmetros para configuração.
2. Exibição dos parâmetros padrão: O sistema apresenta a cena do formulário de configuração com a opção Análise Completa selecionada por padrão, além dos campos para a duração da prova, opção de tempo de leitura padrão (1100 char/min), dificuldade (marcado como "Não") e métricas reais (marcado como "Não").
3. Preenchimento da duração: O docente insere a duração total estimada da prova (em horas e minutos) dentro do limite permitido de até 6 horas. 
4. Acionamento da análise: O docente clica para submeter os parâmetros configurados. 
5. Processamento do sistema: O sistema entra no nó de processamento interno, executando a extração de características estruturais e estatísticas. 
6. Validação e conclusão: O sistema conclui o processamento com sucesso, e direcionando a conversa para a visualização das analises.

#### Caminho alternativo 1 (Personalização dos parâmetros de análise)

Dado que a prova foi validada (precond: {prova validada}), o docente interage com as opções de expansão na cena Informar dados da prova: 
- Ao selecionar Tempo de leitura: Personalizado, a interface exibe o campo para digitação daVelocidade de leitura (caracteres/minuto), cujo preenchimento numérico é obrigatório para liberar a submissão. 
- Ao marcar Dificuldade das questões: Sim, o sistema expande seletores individuais para cada uma das questões detectadas na prova, exigindo a atribuição de um nível (Fácil, Médio ou Difícil) para todas as questões. 
- Ao marcar Métricas reais dos estudantes: Sim, a interface exibe o campo para a quantidade total de estudantes e gera caixas individuais para o preenchimento de acertos por questão. Após ajustar os parâmetros, o docente aciona u: Iniciar análise, enviando os dados para a caixa preta de processamento.

#### Caminho alternativo 2 (Validação de Entradas)

Durante o preenchimento na cena Informar dados da prova, as validações das regras de negócio ocorrem instantaneamente na própria cena, sem acionar o nó de processamento interno:

- Duração > 6h: Ao inserir um valor superior a 6 horas, a interface exibe imediatamente um alerta visual de validação. O docente ajusta o valor  na própria cena, voltando para o fluxo principal
<!--
#### Caminho alternativo 3 (Tratamento de Erro de Sistema / Modelos de IA)

Após preencher todos os parâmetros válidos e clicar em u: Iniciar análise, a conversa avança para o nó de processamento interno.

Caso ocorra uma indisponibilidade nos modelos de Linguagem Natural (BERT / RoBERTa) ou falha de comunicação com o servidor, o sistema emite uma transição por linha tracejada (d: falha ao carregar modelos de IA) para a Cena de Erro de Sistema.

Como todos os dados digitados foram validados e permanecem preservados na tela, o docente seleciona novamente o u: Iniciar análise, sem a necessidade de re-preencher o formulário.
-->

#### Alternativas e rupturas

| Situação | Onde ocorre | Como o usuário percebe | Caminho de recuperação/saída |
| --- | --- | --- | --- |
| Duração da prova excede 6 horas | Na própria cena do formulário (validação instantânea no campo) | Alerta visual imediato no campo informando que a duração não pode ultrapassar 6h (`d: Duração máxima de 6h excedida`) | O docente ajusta a duração para um valor menor ou igual a 6h na própria cena (`u: Corrigir erro`) |

<!--
| Falha temporária no servidor ou modelos de IA (BERT/RoBERTa) | No nó de processamento interno do sistema (Caixa Preta) | Mensagem na cena de erro de sistema  informando indisponibilidade (`d: falha ao carregar modelos de IA`) | O docente clica novamente no `u: iniciar análise` para novamente ir para o nó de processamento interno do sistema |
-->
### Checklist específico de modelagem

- [ ] Existe **ponto de abertura** coerente com o início do objetivo.
- [ ] As **cenas de conversa** representam tópicos/assuntos, não nomes de páginas apenas.
- [ ] As transições/falas deixam claro o que o usuário ou o sistema comunica.
- [ ] Há **ponto(s) de encerramento** para objetivos concluídos/abandonados quando aplicável.
- [ ] Processamentos do sistema estão representados conforme a notação adotada em aula, sem “inventar” fala do usuário.
- [ ] Rupturas (breakdowns) relevantes têm feedback e caminho de recuperação, não becos sem saída.
- [ ] Acessos ubíquos/atalhos só aparecem quando semanticamente justificáveis.
- [ ] O diagrama cobre caminhos alternativos importantes, e não apenas o “happy path”.
- [ ] Nomes de objetivos, tópicos e signos são coerentes com a Entrega 9.
- [ ] O diagrama é legível em tamanho normal no GitHub.
- [ ] O MoLIC representa a conversa usuário–sistema, não o fluxo interno do algoritmo.
- [ ] Processamento, filtros, administração, relatórios e históricos incluem retornos/rupturas quando relevantes.


## M02 — Enviar a avaliação em PDF

**Autor(a):** Beatriz Manaia Lourenço Berto <br>
**Cenário de interação de origem:** CI01  <br>
**Objetivo(s):** O01  <br>
**Tarefa(s) relacionada(s):** T01 - Analisar a prova  <br>
**Signos relevantes:** Prova, Área tracejada (dropzone), ícone de upload (seta), Texto instrucional, Texto de restrição, Botão "Escolher arquivo", Informações do arquivo (nome e tamanho), Botão "cancelar". 

### Diagrama

![MoLIC M01](../assets/10_molic/molic_enviar_prova.jpeg)

**Fonte editável:** [link editável](https://canva.link/tbgn4mxijuochce)

### Leitura do diagrama

<!--Explique em texto o caminho principal e pelo menos os caminhos alternativos/rupturas mais importantes. -->

#### Caminho principal

Pré-condição (precond): {prova elaborada} <br>
Objetivo (gco): Enviar arquivo de prova   <br>
Garantia de Sucesso (gcc): Enviar arquivo de prova <br>
1- (cena ubíqua)Acesso à plataforma: O docente acessa à plataforma e seleciona a opção "Analisar prova". <br>
2- Visualização dos requisitos: Ao acessar a cena Enviar avaliação, o sistema exibe as informações e restrições que o documento PDF precisa cumprir para a submissão.<br>
3- Confirmação do envio: O docente faz o upload do documento e confirma a ação ao clicar no botão "Enviar prova" (u: Enviar prova). <br>
4- Processamento: O sistema inicia a leitura e validação do documento (d: lendo pdf...). <br>
5- Validação de conformidade: O sistema confirma que o documento possui formato e tamanho válidos (d: arquivo em formato e tamanho válidos), satisfazendo a garantia de sucesso (gcc: Enviar arquivo de prova). <br>
6- Transição de tela: A interface avança automaticamente para a cena informar dados da prova. 

#### Caminho alternativo 1 (Cancelamento do carregamento)

Dado que a prova se encontra elaborada (precond: {prova elaborada}), o docente acessa à plataforma e seleciona a opção "Analisar prova" (cena ubíqua) com o objetivo de submeter o documento da avaliação (gco: Enviar arquivo de prova). Na cena Enviar avaliação, o sistema exibe os requisitos para o envio correto do documento PDF. Após selecionar e anexar o arquivo, o sistema avança para a cena Carregar arquivo, apresentando as informações carregadas (d: nome e tamanho do arquivo). Ao constatar que anexou o documento incorreto, o docente aciona a opção de cancelamento (u: Cancelar), interrompendo o envio e retornando à cena Enviar avaliação para nova seleção do arquivo.

#### Caminho alternativo 2 (Tratamento de Erro)

Dado que a prova se encontra elaborada (precond: {prova elaborada}), o docente acede à plataforma e seleciona a opção "Analisar prova" (cena ubíqua) com o objetivo de submeter o documento da avaliação (gco: Enviar arquivo de prova). Ao acessar a cena Enviar avaliação, o sistema exibe as informações de envio do documento PDF. O docente confirma a submissão ao clicar em "Enviar prova" (u: Enviar prova), momento em que o sistema executa o processamento do arquivo (d: lendo pdf...). Caso ocorra uma falha na validação (d: erro 1, 2, 3, 4), a interface redireciona para a cena de erro, exibindo a mensagem correspondente ao problema identificado (erro1: Formato Inválido, erro2: Erro ao preparar a análise. nenhuma questão encontrada, erro3: Arquivo excede tamanho ou erro4: server error). Para prosseguir, o docente seleciona a opção de correção (u: Corrigir erros sinalizados), retornando à cena Enviar avaliação para realizar os ajustes necessários e tentar uma nova submissão.


#### Alternativas e rupturas

| Situação | Onde ocorre | Como o usuário percebe | Caminho de recuperação/saída |
|---|---|---|---|
| Formato de arquivo inválido | na validação do documento enviado | mensagem de erro(feedback) informando que o formato do arquivo não é aceito | o docente retorna à cena de Enviar avaliação, corrige o formato e envia o arquivo novamente |
| Nenhuma questão encontrada | durante o processamento e a preparação da análise da prova, após o envio | mensagem informando que nenhuma questão foi identificada no documento(feedback) | o docente revisa o documento anexado, corrige possíveis problemas na estrutura da prova e realiza um novo envio |
| Arquivo excede o tamanho permitido | na validação do arquivo enviado | mensagem informando que ocorreu um erro interno e que não foi possível concluir o processamento(feedback)) | o docente pode tentar enviar o arquivo novamente ou sair da operação |
| Erro no servidor | durante o processamento do documento, após o envio | mensagem informando que ocorreu um erro interno e que não foi possível concluir o processamento(feedback) | o docnete pode tentar enviar o arquivo novamente ou sair da operação |
| Cancelamento do envio | Após enviar a avaliação | o docente seleciona a opção "cancelar, simbolizada pelo botão "X"na cor vermelha | o sistema interrompe a operação/remove o arquivo anexado e retorna à etapa anterior de enviar avaliação, sem prosseguri com o envio da prova |

### Checklist específico de modelagem

- [X] Existe **ponto de abertura** coerente com o início do objetivo.
- [X] As **cenas de conversa** representam tópicos/assuntos, não nomes de páginas apenas.
- [X] As transições/falas deixam claro o que o usuário ou o sistema comunica.
- [X] Há **ponto(s) de encerramento** para objetivos concluídos/abandonados quando aplicável.
- [X] Processamentos do sistema estão representados conforme a notação adotada em aula, sem “inventar” fala do usuário.
- [X] Rupturas (breakdowns) relevantes têm feedback e caminho de recuperação, não becos sem saída.
- [X] Acessos ubíquos/atalhos só aparecem quando semanticamente justificáveis.
- [X] O diagrama cobre caminhos alternativos importantes, e não apenas o “happy path”.
- [X] Nomes de objetivos, tópicos e signos são coerentes com a Entrega 9.
- [X] O diagrama é legível em tamanho normal no GitHub.
- [X] O MoLIC representa a conversa usuário–sistema, não o fluxo interno do algoritmo.
- [ ] Processamento, filtros, administração, relatórios e históricos incluem retornos/rupturas quando relevantes.


## M03 — Consultar as métricas/analise da prova

**Autor(a):** Nuno Martins Guilhermino da Silva RA: 22.126.099-5 <br>
**Cenário de interação de origem:** CI01 <br>
**Objetivo(s):** O03  <br>
**Tarefa(s) relacionada(s):**  T01 - Analisar a prova <br>
**Signos relevantes:** formalismo, similaridade de distratores, quantidade de palavras, distribuição do tempo de prova e o tempo estimado de leitura, resultados por questão, filtros, quantidade de questões, dificuldade das questões, prova, métricas estruturais, correlação com desempenho balão de ajuda contextual<br>

### Diagrama

![MoLIC M01](../assets/10_molic/molic_m03.svg)

**Fonte editável:** [link editável](https://canva.link/tbgn4mxijuochce)

### Leitura do diagrama

<!--Explique em texto o caminho principal e pelo menos os caminhos alternativos/rupturas mais importantes.-->

### Caminho principal

Pré-condição (precond): {Inserir dados da prova}

Objetivo (gco): Consultar as métricas/análise da prova

Garantia de Sucesso (gcc): Métricas da prova disponibilizadas para consulta e exploração.

1. **Abertura do objetivo:** Após a inserção e análise dos dados da prova, o usuário acessa a análise da prova.
2. **Exibição dos dados:** O sistema apresenta as métricas gerais e os resultados extraídos da análise da prova, como formalismo, similaridade de distratores, quantidade de palavras e tempo estimado de leitura e resolução.
3. **Continuação da interação:** O usuário pode consultar as métricas apresentadas, sem a necessidade de aplicar filtros.

### Caminho alternativo 1 (Usuário quer filtrar informações)

Dado que o usuário acessou as métricas da prova (precond: Dados da prova inseridos e analisados):

1. **Seleção dos filtros:** O usuário acessa a opção de filtragem e escolhe quais características deseja consultar, como formalismo, similaridade de distratores, quantidade de palavras, tempo de resolução e presença de imagens.
2. **Aplicação dos filtros:** O usuário envia os filtros selecionados e o sistema apresenta as informações e os gráficos correspondentes aos critérios escolhidos.
3. **Continuação da interação:** O usuário pode prosseguir com o uso normalmente.

### Caminho alternativo 2 (Usuário utiliza filtros sem resultados)

Dado que o usuário selecionou filtros que não possuem resultados correspondentes:

1. **Identificação da ruptura:** Após o envio dos filtros, o sistema identifica que não existem informações correspondentes aos critérios selecionados.
2. **Exibição do erro:** O sistema apresenta uma mensagem informando que não foram encontrados resultados para os filtros aplicados.
3. **Recuperação da ruptura:** O usuário pode limpar ou modificar os filtros selecionados e realizar uma nova consulta, permitindo que o sistema apresente os resultados correspondentes aos novos critérios.

### Caminho alternativo 3 (Métricas parcialmente indisponíveis)

Dado que a análise da prova foi realizada, mas algumas métricas não puderam ser calculadas devido à ausência de dados ou falhas no processamento:

1. **Exibição dos resultados:** O sistema apresenta as métricas e os gráficos que foram gerados corretamente.
2. **Aviso de indisponibilidade:** O sistema informa ao usuário quais métricas não puderam ser calculadas e, quando possível, o motivo, como a ausência de dados de acerto ou falha no processamento pelo modelo RoBERTa.
3. **Continuação da interação:** O usuário pode continuar consultando as métricas disponíveis. 

### Caminho alternativo 4 (Usuário desmarca todas as análises)

Dado que o usuário está consultando as métricas da prova e desmarca todas as análises disponíveis nos filtros:

1. **Identificação da ruptura:** O sistema identifica que nenhuma análise está selecionada para visualização.
2. **Exibição da mensagem:** O sistema informa ao usuário que nenhuma análise foi selecionada no filtro.
3. **Recuperação da ruptura:** O usuário pode acessar novamente os filtros e selecionar ao menos uma análise para voltar a visualizar os resultados.

### Caminho alternativo 5 (Usuário consulta informações sobre uma métrica)

Dado que o usuário está consultando os resultados da análise da prova:

1. **Solicitação de informações:** O usuário posiciona o cursor sobre o ícone de informações de uma métrica para consultar detalhes sobre seu cálculo.
2. **Exibição da explicação:** O sistema apresenta um tooltip contendo informações sobre o cálculo e o significado da métrica selecionada.
3. **Continuação da interação:** Ao retirar o cursor do ícone, o tooltip é ocultado e o usuário pode continuar consultando as métricas disponíveis.


#### Alternativas e rupturas

| Situação | Onde ocorre | Como o usuário percebe | Caminho de recuperação/saída |
|---|---|---|---|
| Filtro sem informação | Na escolha do filtro | Mensagem de explicação | O usuário redefine os filtros e os aplica novamente. |
### Checklist específico de modelagem

- [X] Existe **ponto de abertura** coerente com o início do objetivo.
- [X] As **cenas de conversa** representam tópicos/assuntos, não nomes de páginas apenas.
- [X] As transições/falas deixam claro o que o usuário ou o sistema comunica.
- [X] Há **ponto(s) de encerramento** para objetivos concluídos/abandonados quando aplicável.
- [X] Processamentos do sistema estão representados conforme a notação adotada em aula, sem “inventar” fala do usuário.
- [X] Rupturas (breakdowns) relevantes têm feedback e caminho de recuperação, não becos sem saída.
- [X] Acessos ubíquos/atalhos só aparecem quando semanticamente justificáveis.
- [X] O diagrama cobre caminhos alternativos importantes, e não apenas o “happy path”.
- [X] Nomes de objetivos, tópicos e signos são coerentes com a Entrega 9.
- [ ] O diagrama é legível em tamanho normal no GitHub.
- [X] O MoLIC representa a conversa usuário–sistema, não o fluxo interno do algoritmo.
- [X] Processamento, filtros, administração, relatórios e históricos incluem retornos/rupturas quando relevantes.

> Repita M02, M03... para todos os integrantes.

## Consolidação da equipe

### Cobertura dos objetivos

| Objetivo | MoLIC que cobre | Lacunas/duplicidades | Decisão |
|---|---|---|---|
| O01 | M02 | {{...}} | {{...}} |
| O04 | M02 | {{...}} | {{...}} |
| O05 | M01 | {{...}} | {{...}} |
| O06 | M03 | {{...}} | {{...}} |
### Preparação para o Figma

Liste os estados/telas que serão necessários **a partir das conversas modeladas**, incluindo feedback, confirmação, erro e recuperação.

Serão necessárias as telas de upload de prova, com os estados de confirmação de upload, erro caso o arquivo seja inválido ou ocorra algum erro de inicialização/servidor, junto com o formulário para inserir os dados das provas, também indicando inputs inválidos, como um tempo de prova maior do que o permitido. Além disso, é necessária a tela de métricas para mostrar ao usuário os resultados da análise da prova escolhida, tendo recuperação caso coloque filtros que não tenham informações relacionadas/vazio ou caso tenha alguma informação que não pode ser calculada. 
## Erros frequentes a evitar

- desenhar apenas caixas com nomes de telas e setas de navegação;
- não modelar falhas, cancelamento, volta ou recuperação;
- usar rótulos genéricos (“Tela 1”, “Processo 2”) sem tópico de conversa;
- criar no Figma fluxos que não existem no MoLIC;
- diagrama sem legenda/fonte editável e com texto ilegível.
