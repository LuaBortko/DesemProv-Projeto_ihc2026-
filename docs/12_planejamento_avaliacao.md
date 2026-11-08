# Entrega 12 — Planejamento da avaliação de usabilidade (DECIDE)

**Data:** 08/11/2026<br> 
**Status:** 🟨 Em andamento<br> 
**Responsabilidade:** 1 solução por equipe<br> 

<!--Entrega eh p entender tecnicas de planejamento, qnd fa zplanejamento resp perg e sabe se vai faze teste de avaliaco heuristica, ou comunicabilidade ou observacao do usuario, ensina a planejar -->

## Objetivo da atividade

Planejar a avaliação antes de executá-la, ligando perguntas de avaliação a métodos, participantes, tarefas, métricas, aspectos práticos, ética e forma de análise.

## O que está sendo avaliado

Em projetos cuja interface foi criada ou ampliada para a disciplina, o plano deve declarar explicitamente que a avaliação investiga **a qualidade da interação/protótipo**, não a validade científica ou o desempenho técnico do algoritmo/modelo do TCC.

Exemplos de perguntas:

- o DBA consegue localizar e comparar duas execuções?
- o analista entende o significado de um indicador?
- o administrador consegue alterar uma permissão sem risco de erro não percebido?
- o usuário compreende que o processamento está em andamento e consegue recuperar-se de uma falha?
- os filtros ajudam a localizar o histórico relevante?
- um relatório permite identificar a informação necessária para a decisão?

Se o protótipo utiliza dados ou resultados simulados, documente isso no plano.

## A. Método DECIDE
<!--No final do planejamento tem frameworek onde cada letra (DECIDE) TEM REGRA COMO PATTERN. PCRIA PLANEJAENTO DE TESTE, ENVOLVE OBJ, PUBLICO ALVO, ETICA, QUE INSTURMENTO VAI USA(COMO GRAVA INFO DE USABILIDADE)


O da disciplina eh identifcia problemas  de iteracao e interface 


Metodo: pega isnturentos ex braisntorm ,questionario, entrevista, observacao, investigacaocontextual.... tecnicas p levanta requistios e posso reutiliza p testa software 

heristica segue roteiro desse de planejamento slide 35 do totpico 11 se relato dos resultados....
 
 PRECISAMOS TESTAR COM PROFESSORES AQUI???? coletar dados sobre experiencia de uso 
 -participacao dos usuarios podem ser relziadas em contexto real de uso ou em laboratorio
 
PRIMEIRA RESPSOTA ELE FLO PRA VOLTA PRA ENTREGA 8 E NAO VOLTEI AINDA ENT EH BOM VERMOS ISSO
SEGUNDA REPSOTA: COLOQUEI TDOS SOS EXEMPLOS DA AULA MAS É BOM PENSARMOS EM PERG ESPECIFCIAS PRO NOSSO -->


| Etapa | Aplicação no projeto |
|---|---|
| **D — Determine the goals** | Os objetivos da avaliação são identificar problemas de iteração e interface e também analisar a aproprieação da tecnologia | 
| **E — Explore the questions** | O usuário consegue operar o sistema sem grandes dificuldades? O usuário consegue analisar as métricas da prova?As métricas disponibilizadas auxiliam na compreensão da avaliação?Quais objetivos dos usuários podem ser alcançados através do sistema e quais não podem ser alcançados através do sistema?Quais barreiras o usuário encontra para atingir seus objetivos? A tecnologia disponível pode oferecer maneiras mais interessantes ou eficientes de os usuários atingirem seus objetivo? O usuário consegue operar o sistema com quanta eficiência? Em quanto tempo? Após cometer quantos erros? Que parte da interface e da interação o deixa insatisfeito? Quais são os pontos fortes e fracos do sistema, na opinião dos usuários? Que parte da interface o desmotiva a explorar novas funcionalidades? Ele entende o que significa e para que serve cada elemento da interface? Ele vai entender o que deve fazer em seguida? Ele tem acesso a todas as informações oferecidas pelo sistema? O que é possível modificar no sistema interativo para adequá-lo melhor ao ambiente de trabalho? Há problemas de feedback?|
| **C — Choose the evaluation paradigm and techniques** | Serão utilizados os métodos de inspeção heurística e observação de usuários devido a sua obrigatoriedade pelo professor da disciplina. |
| **I — Identify the practical issues** | Participantes: 3 a 5 desenvolvedores (para a inspeção heurística) e 1 a 3 professores (para a observação de uso). Recrutamento: Professores serão convidados via contato direto (pessoalmente) no período de aula. Devido à janela de 1 semana para a realização dos testes, eles terão que ser rápidos. Ambiente: As sessões com os professores serão presenciais, na faculdade. A inspeção heurística será presencial/Google Meet entre a equipe. Equipamentos: Computador com acesso à internet, microfone, câmera. Piloto: Um integrante da equipe fará o papel de "professor" 1 dia antes para validar o roteiro e o tempo (máximo 40 min). Cronograma: Semana 1: Dias 1-2 (Recrutamento e Heurística); Dias 3-4 (Testes com Professores); Dias 5-7 (Análise de dados e redação). Responsáveis: Luana (Facilitadora), Beatriz (Observador/Anotações), Nuno (Análise e Cronometragem). Riscos Técnicos: Falha na conexão ou no protótipo local. |
| **D — Decide how to deal with ethical issues** | Os participantes devem ser respeitados e não podem ser prejudicados direta ou indiretamente, nem durante os experimentos, nem após a divulgação dos resultados. Para os testes presenciais na faculdade com os professores, adotaremos as seguintes medidas, alinhadas à Resolução 196/96:  1. Autonomia e Consentimento Livre e Esclarecido: Antes de iniciar o teste, o professor receberá e assinará o Termo de Consentimento. Será esclarecido que ele tem total liberdade para recusar-se a participar ou desistir a qualquer momento, sem qualquer prejuízo ou constrangimento.  2. Não Maleficência e Ambiente Seguro: Como o teste ocorre na faculdade, garantiremos uma sala reservada e silenciosa. O facilitador deixará claro que o objeto de avaliação é o sistema e não a capacidade do professor. Se o professor errar, a equipe não o julgará; pelo contrário, o erro será tratado como uma oportunidade de melhoria da interface, evitando qualquer estresse ou sensação de incapacidade. 3. Confidencialidade e Anonimato: Na divulgação dos resultados, os nomes dos professores serão totalmente anonimizados (ex: Professor P1, Professor P2).  4. Proteção de Dados de Terceiros: Como o sistema analisa provas (arquivos PDF), orientaremos os professores a utilizarem arquivos de prova modelo ou sem dados sensíveis de alunos reais. Caso utilizem provas reais, garantiremos que os PDFs não serão retidos após a avaliação, respeitando a privacidade dos estudantes.|
| **E — Evaluate, interpret and present the data** | Consolidação: Os dados quantitativos (tempo, erros, notas de satisfação) serão organizados em gráficos e tabelas de frequência/média. Os dados qualitativos (falas e observações) serão agrupados por temas (ex: "dificuldade de feedback", "confusão nos gráficos").  Comparação com Metas: Os resultados serão comparados diretamente com os critérios de sucesso da seção B (ex: verificar se a taxa de sucesso passou de 90% ou se a média de erros ficou abaixo de 1).  Apresentação: Os resultados serão apresentados em um relatório contendo: gráficos comparativos, citações anônimas dos professores para ilustrar os problemas e uma lista final de melhorias para a interface, classificada por gravidade (grave, moderado, leve).|

## B. Perguntas de avaliação

<!-- importante usa metodo de observação de uso (que ehentrega  14)
axcho que tambem caberia fazer o de inspecao: Inspecao nos avlaiadores usamos interfface e fazemoa analise potencial -->

| ID | Pergunta | Método | Métrica/evidência | Critério esperado |
|---|---|---|---|---|
| QA01 | O usuário consegue operar o sistema sem grandes dificuldades? | heurística, observação | Taxa de conclusão das tarefas, quantidade de erros, solicitações de ajuda e  abandonos | Taxa de sucesso de pelo menos 90% na primeira tentativa sem auxilio (MU01) |
| QA02 | O usuário consegue analisar as métricas da prova? | heurística, observação | Taxa de interpretação correta das métricas, dúvidas apresentadas e violações heurísticas relacionadas a compreensão | Os usuários conseguem interpretar as métricas e identificar informações relevantes para analisar a prova |
| QA03 | As métricas disponibilizadas auxiliam na compreensão da avaliação? | observação | Relatos dos usuários, interpretações realizadas e necessidades não atendidas | As métricas são compreensíveis e fornecem informações relevantes para apoiar a análise da prova |
| QA04 | Quais objetivos dos usuários podem ser alcançados através do sistema e quais não podem ser alcançados através do sistema? | observação | Tarefas concluídas, parcialmente concluídas ou não realizadas e necessidades não atendidas | Os principais objetivos relacionados à análise da prova podem ser alcançados pelo sistema, com identificação de possíveis limitações |
| QA05 | Quais barreiras o usuário encontra para atingir seus objetivos? | heurística,observação | Quantidade e tipo de dificuldades, erros, dúvidas, interrupções e violações heurísticas identificadas | Os  usuários conseguem superar as dificuldades sem comprometer a conclusão das tarefas com média inferior a um erro por usuário (MU04) |
| QA06 | A tecnologia disponível pode oferecer maneiras mais interessantes ou eficientes de os usuários atingirem seus objetivo? | observação | Sugestões dos usuários, dificuldades recorrentes e oportunidades de melhoria identificadas durante o uso | São identificadas oportunidades de melhoria que tornem a interação mais simples, eficiente e adequada às necessidades dos professores |
| QA07 | O usuário consegue operar o sistema com quanta eficiência? Em quanto tempo? Após cometer quantos erros?  | heurística, observação | Tempo de execução, taxa de sucesso, quantidade de erros e solicitações de ajuda por tarefa| Tempo mediano de execução de até 15 minutos (MU03) e média inferior a um erro por uusário (MU04) |
| QA08 | Que parte da interface e da interação o deixa insatisfeito? | heurística, observação | Relátos de insatisfação, dificuldades percebidas e violações heurísticas identifciadas | Atingir pelo menos 75% de satisfação na avaliação pós-tarefa (MU05) |
| QA09 | Quais são os pontos fortes e fracos do sistema, na opinião dos usuários? | observação | Comentários positivos de negativos, sugestões e aspectos destacados pelos participantes | Identificar os principais pontos positivos e aspectos que precisam de melhorias, considerando a meta de satisfaçã de pelo menos 75% (MU05) |
| QA10 | Que parte da interface o desmotiva a explorar novas funcionalidades? | heurística, observação | Funcionalidades não exploradas, desist6encias, dúvidas e relatoa de desmotivação | A interface apresenta funcionalidades acessíveis e compreensíveis, incentivando a exploração sem gerar insegurança ou confusão |
| QA11 | Ele entende o que significa e para que serve cada elemento da interface?  | heurística, observação | Interpretação dos rótulos, ícones, indicadores e funcionalidades, dúvidas e interpretações incorretas | Os elementos da interface possuem identificação clara e seus significados e funções são compreendidos pelos usuários |
| QA12 | Ele vai entender o que deve fazer em seguida? | heurística | Hesitações, solicitaçÕes de ajuda, erros de navegação e violações relacionadas ã orientação e conssitência| a interface fornece indicações claras sobre a sproóximas ações, permitindo a continuidade da interação sem dúvidas |
| QA13 | Ele tem acesso a todas as informações oferecidas pelo sistema? | observação | Informações não localizadas, elementos inacessíveis, dificuldades de navegação e violações identificadas. | Os usuários conseguem localizar e acessar as informações necessárias para realizar suas tarefas |
| QA14 | O que é possível modificar no sistema interativo para adequá-lo melhor ao ambiente de trabalho? | observação | Necessidades relatadas, sugestões de adaptação e incompatibilidade entre interface e o contexto de trabalho | São identificadas adaptaçÕes que aproximem a interface das necessidades e práticas de trabalho dos professores |
| QA15 | Há problemas de feedback? | heurística, observação | Ausência ou inadequação de mensagens, respostas às ações, indicadores de carregamento e confirmações de operações | O sistema fornece feedback claro e oportuno, permitindo que o usuário compreenda o resultado de suas ações e o estado da interação. |

## C. Escopo e participantes

| Item | Planejamento |
|---|---|
| Perfis | {{...}} |
| Critérios de inclusão/exclusão | {{...}} |
| Nº de participantes | {{...}} |
| Ambiente | presencial/remoto/campo/laboratório |
| Dispositivo | {{...}} |
| Protótipo/versão | {{...}} |
| Teste piloto | {{quem, quando, o que validar}} |

## C. Escopo e participantes

| Item | Planejamento |
| ------ | ------ |
| Perfis | **Avaliadores (Inspeção Heurística):** 3 integrantes da equipe de desenvolvimento, com conhecimento prévio nas 10 Heurísticas de Nielsen e na notação do MoLIC. **Usuários (Observação de Uso):** 1 a 3 professores da própria faculdade (docentes universitários da instituição) que elaboram e aplicam avaliações com questões de múltipla escolha e utilizam computador em sua rotina acadêmica. |
| Critérios de inclusão/exclusão | **Inclusão:** Docentes da própria faculdade que elaboram e aplicam provas objetivas/múltipla escolha em suas disciplinas; uso habitual de computador com internet; disponibilidade para realizar a sessão presencial de até 30 minutos no ambiente universitário. **Exclusão:** Docentes que não aplicam avaliações de múltipla escolha. |
| Nº de participantes | **Inspeção Heurística:** 3 avaliadores internos da equipe. **Observação de Uso:** 1 a 3 professores da própria faculdade (conforme delimitado na etapa *Identify practical issues* do método DECIDE). |
| Ambiente | **Observação de Uso:** Presencial, em sala reservada e silenciosa na própria faculdade (para evitar ruídos e interrupções) **Inspeção Heurística:** Presencial/Remoto em reunião síncrona (Google Meet) entre os membros da equipe. |
| Dispositivo | Computador ou notebook com acesso à internet, navegador web atualizado, microfone e software de gravação de tela e áudio (ex.: OBS Studio). |
| Protótipo/versão | Sistema web funcional em desenvolvimento (versão parcial) do DesemProv, cobrindo os fluxos de upload da prova em PDF, o formulário de parâmetros de configuração (duração, velocidade de leitura, dificuldade e acertos por questão) e o painel de visualização das métricas estruturais. Por se tratar de uma versão parcial em desenvolvimento, limitações funcionais ou dados eventualmente simulados serão declarados e instruídos no roteiro de teste. |
| Teste piloto | **Quem:** 1 integrante da equipe (desempenhando o papel de "professor"). **Quando:** 1 dia antes do início das sessões presenciais com os professores convidados. **O que validar:** Clareza das instruções e do roteiro de tarefas; cumprimento do tempo máximo de 30 minutos por sessão e o tempo de execução das tarefas; funcionamento dos softwares de gravação (tela/áudio); estabilidade do protótipo. |

## D. Lista de tarefas de avaliação

| ID | Cenário neutro entregue ao usuário | Objetivo oculto da avaliação | Critério de sucesso | Tempo-limite (se houver) |
|---|---|---|---|---|
| UT01 | "Você acabou de criar uma prova de alguma matéria que leciona e quer saber métricas sobre o formato da sua prova como: relação dos distraotres das alternativas, se o tempo para fazer as questÕes é suficiente." | T01/O01 | Concluir upload, preencher as informações da prova e gerar a análise | 5 minutos |
| UT02 | "Você quer avaliar uma prova já aplicada que teve um desempenho fora do esperado, para isso deseja analisar as caracteristicas de formato da sua avaliação" | T01/O02 | Concluir upload, preencher as informações da prova e gerar a análise | 5 minutos |
| UT03 | "Analisando os resultados/métricas geradas pelo sistema, identifique informações úteis para você, como elaborador de prova" | T01/O01/O02 | Localizar as informações e analisar as métricas e gráficos disponibiloizados | 10 minutos |

> Uma boa instrução descreve o objetivo do participante sem dizer **onde clicar** ou usar o rótulo exato do controle que está sendo testado.

## E. Instrumentos

- [Modelo de termo de consentimento](../instrumentos/termo_consentimento_modelo.md)
- [Roteiro de teste](../instrumentos/roteiro_teste_usabilidade.md)
- [Planilha de observação](../instrumentos/planilha_observacao_modelo.md)
- [Formulário de avaliação heurística](../instrumentos/formulario_heuristica_modelo.md)
- [Questionário pré-teste](../instrumentos/questionario_pre.md)
- [Questionário pós-teste](../instrumentos/questionario_pos.md)
<!-- {{questionário pré/pós-teste}}-->

## F. Plano de análise

Defina antes dos testes:
<!--
- sucesso total / parcial / falha;
- o que conta como erro, dúvida, ajuda e abandono;
- como tempo será medido;
- escala de satisfação pós-tarefa;
- como observações/falas serão codificadas;
- como problemas serão priorizados;
- como comparar resultados às metas de usabilidade.
-->

### 1. Critérios de Desempenho

- Sucesso Total (Sem Ajuda): O participante conclui o objetivo da tarefa autonomamente, sem intervenção do facilitador e sem cometer erros irrecuperáveis.
- Sucesso Parcial (Com Ajuda/Recuperação): O participante conclui o objetivo após cometer algum erro de percurso recuperado por ele mesmo, ou necessitando de uma dica pontual do facilitador.
- Falha: O participante desiste de concluir a tarefa, comete um erro crítico não recuperado, ou necessita de intervenção direta do facilitador para realizar a ação por ele.

### 2. Categorização dos Eventos da Interação

- Erro: Ação na interface que afasta o participante do objetivo da tarefa (ex.: tentar digitar caracteres em campos numéricos, tentar enviar arquivo fora das especificações, clicar em elementos não interativos).
- Dúvida: Manifestação verbal de incerteza (ex.: "O que significa 1100 char/min?") ou hesitação visível sem ação na tela por mais de 10 segundos.
- Solicitação de Ajuda: Pedido explícito do participante por orientação quando se sente bloqueado na tarefa.
- Abandono: Declaração explícita do participante de que não consegue ou não deseja continuar a tarefa.

### 3. Medição de Tempo e Eficiência

- A medição do tempo será realizada em segundos, utilizando a gravação de áudio/vídeo da sessão (via OBS Studio ou Google Meet).
- **Tempo Total da Sessão:** A sessão presencial terá duração total de aproximadamente 30 minutos, cobrindo acolhimento, assinatura do TCLE, instrução, tarefas e questionário pós-teste.
- **Tempo de Execução das Tarefas:** Para medir a eficiência da interface, será cronometrado o tempo de interação ativa no sistema. A cronometragem de cada tarefa inicia imediatamente após a leitura do cenário neutro e encerra quando o participante conclui o objetivo. A soma do tempo de execução de todas as tarefas será comparada à meta MU03 (tempo mediano de execução no sistema de até 15 minutos).

### 4. Escala de Satisfação Pós-Tarefa e Pós-Teste

- Avaliação Pós-Tarefa (Single Ease Question - SEQ): Ao final de cada tarefa, o participante responderá a uma escala visual de 1 a 7 (*"Quão fácil ou difícil foi realizar esta tarefa?"*).
- Avaliação Pós-Teste (Satisfação Perceptual): Questionário final pós-teste para avaliar a clareza dos feedbacks, utilidade visual e conforto de uso do DesemProv, buscando atingir a meta de satisfação de pelo menos 75% (MU05).

### 5. Codificação de Dados Qualitativos (Think Aloud)

As falas e comportamentos gravados durante o teste de observação serão transcritos e categorizados nas seguintes classes:

- PI (Problema de Interface): Rótulos confusos, botões pouco visíveis, falta de contraste ou ausência de indicação de estado.
- PS (Problema de Signo/Conceito): Dificuldade de compreensão sobre o significado pedagógico de uma métrica ou parâmetro (ex.: formalismo, tempo de leitura).
- SE (Sugestão/Elogio): Comentários positivos ou sugestões espontâneas de adaptação ao ambiente de trabalho docente.

### 6. Classificação de Severidade dos Problemas (Graus de Nielsen)

Os problemas identificados (na inspeção heurística e na observação de uso) serão priorizados conforme os graus de severidade de Nielsen:

- Grau 0 (Sem Importância): Não afeta a usabilidade da interface.
- Grau 1 (Cosmético): Necessita de ajuste estético/visual; não prejudica a realização das tarefas.
- Grau 2 (Menor): Causa pequena hesitação ou erro leve com fácil recuperação; baixa prioridade de correção.
- Grau 3 (Maior): Dificulta consideravelmente a execução da tarefa e gera frustração; alta prioridade de correção.
- Grau 4 (Catastrófico): Impede a conclusão da tarefa ou causa perda indesejada de dados; correção crítica e obrigatória.

### 7. Confronto com as Metas de Usabilidade

Os dados consolidados serão comparados com os critérios esperados definidos na Tabela B:

- MU01 (Taxa de Sucesso): Confirmar se atingiu pelo menos 90% de sucesso sem auxílio.
- MU03 (Tempo de Execução): Verificar se o tempo mediano permaneceu dentro do limite de 15 minutos.
- MU04 (Taxa de Erros): Validar se a média de erros por usuário ficou inferior a 1 erro por tarefa.
- MU05 (Satisfação): Verificar se o nível geral de satisfação atingiu a meta de pelo menos 75%.

## Checklist

- [X] As seis etapas DECIDE foram contextualizadas, não apenas expandidas por sigla.
- [X] Perguntas de avaliação têm método e evidência correspondentes.
- [X] O plano distingue avaliação de IHC de avaliação técnica/científica do TCC.
- [X] Dados ou processamentos simulados no protótipo estão declarados.
- [X] Tarefas vêm de objetivos/cenários relevantes.
- [X] Critérios de sucesso foram definidos antes da coleta.
- [X] Questões práticas e éticas estão resolvidas.
- [ ] Instrumentos estão prontos antes da Entrega 13/14.
- [X] Plano diz como dados serão analisados e apresentados.
