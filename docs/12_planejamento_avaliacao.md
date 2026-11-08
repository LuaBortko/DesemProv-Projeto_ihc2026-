# Entrega 12 — Planejamento da avaliação de usabilidade (DECIDE)

<!-- LER ANOTACAO TOPICO 12 PRINCIPALMENTE O NAO GRIFADO E VER ANOTACAO AULA -->

**Data:** 08/11/2026  <br> 
**Status:** 🟨 Em andamento  <br> 
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
 
 -->

<!--PRIMEIRA RESPSOTA ELE FLO PRA VOLTA PRA ENTREGA 8 E NAO VOLTEI AINDA ENT EH BOM VERMOS ISSO
SEGUNDA REPSOTA: COLOQUEI TDOS SOS EXEMPLOS DA AULA MAS É BOM PENSARMOS EM PERG ESPECIFCIAS PRO NOSSO -->


| Etapa | Aplicação no projeto |
|---|---|
| **D — Determine the goals** | Os objetivos da avaliação são identificar problemas de iteração e interface e também analisar a aproprieação da tecnologia | 
| **E — Explore the questions** | O usuário consegue operar o sistema sem grandes dificuldades? O usuário consegue analisar as métricas da prova?
As métricas disponibilizadas auxiliam na compreensão da avaliação?
Quais objetivos dos usuários podem ser alcançados através do sistema e quais não podem ser alcançados através do sistema?
Quais barreiras o usuário encontra para atingir seus objetivos? 
A tecnologia disponível pode oferecer maneiras mais interessantes ou eficientes de os usuários atingirem seus objetivo? O usuário consegue operar o sistema com quanta eficiência? Em quanto tempo? Após cometer quantos erros? Que parte da interface e da interação o deixa insatisfeito? Quais são os pontos fortes e fracos do sistema, na opinião dos usuários? Que parte da interface o desmotiva a explorar novas funcionalidades? Ele entende o que significa e para que serve cada elemento da interface? Ele vai entender o que deve fazer em seguida? Ele tem acesso a todas as informações oferecidas pelo sistema? O que é possível modificar no sistema interativo para adequá-lo melhor ao ambiente de trabalho? Há problemas de feedback?|
| **C — Choose the evaluation paradigm and techniques** | Quais métodos serão usados e por quê? Ex.: inspeção heurística + observação de usuários. |
| **I — Identify the practical issues** | Participantes, recrutamento, ambiente, equipamentos, piloto, cronograma, responsáveis, riscos técnicos. |
| **D — Decide how to deal with ethical issues** | Consentimento, privacidade, gravação, anonimização, interrupção, dados sensíveis.  SEMPRE TEM QUESTAO ETICA QND ENVOVLE pessoa, abrir slide la tipo, termo de concenriment odo exclarecido ,pss pode desistir a qrr momento, tme q te rambiente cofnortavel n posso deixa pss estressada...|
| **E — Evaluate, interpret and present the data** | Como dados quantitativos/qualitativos serão consolidados, comparados às metas e apresentados. |

## B. Perguntas de avaliação

<!-- importante usa metodo de observação de uso (que ehentrega  14)
axcho que tambem caberia fazer o de inspecao: Inspecao nos avlaiadores usamos interfface e fazemoa analise potencial -->


<!--
O usuário consegue operar o sistema sem grandes dificuldades?
O usuário consegue analisar as métricas da prova?
As métricas disponibilizadas auxiliam na compreensão da avaliação?
Quais objetivos dos usuários podem ser alcançados através do sistema e quais não podem ser alcançados através do sistema?
Quais barreiras o usuário encontra para atingir seus objetivos? 
A tecnologia disponível pode oferecer maneiras mais interessantes ou eficientes de os usuários atingirem seus objetivo?
O usuário consegue operar o sistema com quanta eficiência? Em quanto tempo? 
Após cometer quantos erros? 
Que parte da interface e da interação o deixa insatisfeito? 
Quais são os pontos fortes e fracos do sistema, na opinião dos usuários?
Que parte da interface o desmotiva a explorar novas funcionalidades?
Ele entende o que significa e para que serve cada elemento da interface? 
Ele vai entender o que deve fazer em seguida? 
Ele tem acesso a todas as informações oferecidas pelo sistema?
O que é possível modificar no sistema interativo para adequá-lo melhor ao ambiente de trabalho?
há problemas de feedback?
-->

| ID | Pergunta | Método | Métrica/evidência | Critério esperado |
|---|---|---|---|---|
| QA01 | O usuário consegue operar o sistema sem grandes dificuldades? | heurística, observação | Taxa de conclusão das tarefas, quantidade de erros | {{MU01}} |

| QA02 | O usuário consegue analisar as métricas da prova? | heurística, observação | violações H1 | {{...}} |
| QA03 | As métricas disponibilizadas auxiliam na compreensão da avaliação? | observação | violações H1 | {{...}} |
| QA04 | Quais objetivos dos usuários podem ser alcançados através do sistema e quais não podem ser alcançados através do sistema? | observação | violações H1 | {{...}} |
| QA05 | Quais barreiras o usuário encontra para atingir seus objetivos? | heurística,observação | violações H1 | {{...}} |
| QA06 | A tecnologia disponível pode oferecer maneiras mais interessantes ou eficientes de os usuários atingirem seus objetivo? | observação | violações H1 | {{...}} |
| QA07 | O usuário consegue operar o sistema com quanta eficiência? Em quanto tempo? Após cometer quantos erros?  | heurística, observação | violações H1 | {{...}} |
| QA08 | Que parte da interface e da interação o deixa insatisfeito? | heurística, observação | violações H1 | {{...}} |
| QA09 | Quais são os pontos fortes e fracos do sistema, na opinião dos usuários? | observação | violações H1 | {{...}} |
| QA10 | Que parte da interface o desmotiva a explorar novas funcionalidades? | heurística, observação | violações H1 | {{...}} |
| QA11 | Ele entende o que significa e para que serve cada elemento da interface?  | heurística, observação | violações H1 | {{...}} |
| QA12 | Ele vai entender o que deve fazer em seguida?  | heurística | violações H1 | {{...}} |
| QA13 | Ele tem acesso a todas as informações oferecidas pelo sistema? | observação | violações H1 | {{...}} |
| QA14 | O que é possível modificar no sistema interativo para adequá-lo melhor ao ambiente de trabalho? | observação | violações H1 | {{...}} |
| QA15 | Há problemas de feedback? | heurística, observação | violações H1 | {{...}} |




| QA01 | {{usuários completam T01 sem ajuda?}} | observação | sucesso, ajuda, erro | {{MU01}} |
| QA02 | {{há problemas de feedback?}} | heurística | violações H1 | {{...}} |

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

## D. Lista de tarefas de avaliação

| ID | Cenário neutro entregue ao usuário | Objetivo oculto da avaliação | Critério de sucesso | Tempo-limite (se houver) |
|---|---|---|---|---|
| UT01 | {{...}} | {{T01/O01}} | {{...}} | {{...}} |

> Uma boa instrução descreve o objetivo do participante sem dizer **onde clicar** ou usar o rótulo exato do controle que está sendo testado.

## E. Instrumentos

- [Modelo de termo de consentimento](../instrumentos/termo_consentimento_modelo.md)
- [Roteiro de teste](../instrumentos/roteiro_teste_usabilidade.md)
- [Planilha de observação](../instrumentos/planilha_observacao_modelo.md)
- [Formulário de avaliação heurística](../instrumentos/formulario_heuristica_modelo.md)
- {{questionário pré/pós-teste}}

## F. Plano de análise

Defina antes dos testes:

- sucesso total / parcial / falha;
- o que conta como erro, dúvida, ajuda e abandono;
- como tempo será medido;
- escala de satisfação pós-tarefa;
- como observações/falas serão codificadas;
- como problemas serão priorizados;
- como comparar resultados às metas de usabilidade.

## Checklist

- [ ] As seis etapas DECIDE foram contextualizadas, não apenas expandidas por sigla.
- [ ] Perguntas de avaliação têm método e evidência correspondentes.
- [ ] O plano distingue avaliação de IHC de avaliação técnica/científica do TCC.
- [ ] Dados ou processamentos simulados no protótipo estão declarados.
- [ ] Tarefas vêm de objetivos/cenários relevantes.
- [ ] Critérios de sucesso foram definidos antes da coleta.
- [ ] Questões práticas e éticas estão resolvidas.
- [ ] Instrumentos estão prontos antes da Entrega 13/14.
- [ ] Plano diz como dados serão analisados e apresentados.
