# Entrega 14 — Avaliação de usabilidade por observação de usuários

**Data:** 08/11/2026
**Status:**  🟨 Em andamento
**Responsabilidade:** solução consolidada por equipe. O número de participantes finais observados deve ser igual ao número de integrantes, conforme o modelo da disciplina; recomenda-se que cada integrante seja responsável por conduzir/analisar ao menos um participante.
<!--
anotacao topico 12 e 14....
todo metodo de avalaicao é baseado em 
-prearacao
-coleta de dados
-interpretacao
-consolidacao
-relato dos resultados

PREPARACAO PARA AVALIACAO: tem q ter perfies e numero de pariticpantes (10 usuarios eh produtivo p avalaicao p evitar falhas, n precisa passar de 10 pq ai tem recorrencia dos erros, tem so dado de peso dos erros p ve rmaior impacto..)

 Prototipo uso p avaliacao herusitica e teste de obs de usuario 

Faremos colocando pessoas de fora da equipe, colegas da turma, professores(preferencialmente), orientadors, familiares....  
 -->
## Objetivo da atividade

Observar usuários representativos realizando tarefas reais ou realisticamente simuladas para identificar problemas de eficácia, eficiência, compreensão e satisfação que não podem ser inferidos apenas por inspeção.

> **Participantes finais não devem ser membros da equipe.** Um integrante pode participar do teste piloto apenas para validar roteiro/equipamentos, sem contar na amostra final.

### Quando o usuário é um perfil profissional especializado

Em TCCs técnicos, o público pode ser DBA, analista, pesquisador, administrador, técnico ou outro especialista. Priorize participantes que possuam relação real com as tarefas. Se não for possível recrutar o perfil ideal, qualquer participante aproximado/proxy deve ser **justificado previamente e tratado como limitação**; não apresente o resultado como equivalente ao de especialistas reais.

O teste avalia a **interação com o protótipo**. Não é necessário que o participante valide o desempenho científico do algoritmo. Resultados simulados podem ser usados quando declarados e coerentes com a tarefa.

Tarefas podem envolver, por exemplo, interpretar um dashboard, configurar uma análise, encontrar uma execução no histórico usando filtros, comparar resultados, gerar relatório, revisar alerta ou administrar permissões.

## A. Fluxograma do processo — equipe 

![Fluxograma](../assets/14_testes/fluxogramaEntrega14.jpeg)

<!--O fluxograma deve representar, no mínimo: planejamento → recrutamento → consentimento → preparação → execução das tarefas/observação → pós-teste → consolidação/análise → recomendações.-->

## B. Procedimento de preparação e execução — equipe

### Passo 1 — Objetivos e versão avaliada 

**Versão/commit/Figma:** verão atual do código disponível em: [Repositório TCC](https://github.com/beatrizmanaia26/TCC-DesempenhoEnem) 
**Metas de usabilidade relacionadas:** MU01 (facilidade de aprendizado), MU02 (facilidade de memorização), MU03 (eficiência), MU04 (taxa e gravidade de erros) e MU05 (satisfação).

### Passo 2 — Participantes <!--fazer -->

| ID | Perfil | Critérios que justificam participação | Integrante responsável |
|---|---|---|---|
| U01 | {{sem nome real}} | {{...}} | {{...}} |
| U02 | {{sem nome real}} | {{...}} | {{...}} |
| U03 | {{sem nome real}} | {{...}} | {{...}} |

### Passo 3 — Consentimento e privacidade 

- Termo/registro de consentimento: [Modelo de termo de consentimento](../instrumentos/termo_consentimento_modelo.md) <br>
- Gravação de tela/áudio/vídeo: Sim, mediante autorização do participante. A gravação de tela será utilizada para analisar a navegação, identificar dificuldades e verificar as ações realizadas durante as tarefas. A gravação de áudio poderá ser utilizada para registrar comentários e dúvidas verbalizadas durante a avaliação.<br>
- Forma de anonimização:  Os participantes serão identificados exclusivamente por códigos, como ⁠ U01 ⁠, ⁠ U02 ⁠ e ⁠ U03 ⁠, sem utilização de nomes ou outras informações pessoais nos registros e na apresentação dos resultados.<br>
- Local e período de armazenamento: Os registros da avaliação serão armazenados em pasta digital de acesso restrito à equipe, durante o período de realização e análise da atividade. Após a consolidação dos resultados e a conclusão da avaliação, os arquivos contendo gravações serão excluídos. <br>

### Passo 4 — Teste piloto <!-- LU E NUNO FAZEREM TESTE PILOTO NA QUARTA-->

**Data:** 
**O que foi validado:** roteiro, duração, entendimento das instruções, protótipo, gravação.  
**Mudanças após piloto:** {{...}}

### Passo 5 — Tarefas 

| ID | Cenário/instrução apresentada | Critério de sucesso | Métricas | Ligação com modelo |
|---|---|---|---|---|
| UT01 | Você é um professor e precisa analisar uma prova para compreender características de sua estrutura e identificar aspectos que possam influenciar o desempenho dos alunos. Utilize o sistema para enviar o arquivo da prova, preencher os parâmetros solicitados e realizar a análise. Ao final, explore os resultados apresentados e explique o que conseguiu compreender a partir das métricas disponíveis. | O participante consegue enviar o PDF aceito, preencher os par6ametros necessários, iniciar a análise e acessar os resultados. Além disso, consegue identificar e explicar o significado das principais métricas apresentadas, sem auxilio do moderador | taxa de sucesso, tempo de execução, quantidade de erros, taxa de recuperação, pedidos de ajudas, satisfação  pós tarefa|T01/M01/M02/M03/f01,f02,f02e1,f02e2,f02e3,f02e4,f03,f03_1,f03_2,f03_3, f03_4,f03e1, f04,f04_1,f04_2,f04_3,F04_4,F04e1,f04e2 |

### Passo 6 — Protocolo do moderador <!--fazer -->

1. Receber participante e explicar que **o produto está sendo avaliado, não a pessoa**.
2. Obter consentimento.
3. Aplicar perfil pré-teste mínimo necessário.
4. Ler instruções padronizadas.
5. Observar sem ensinar o caminho; registrar pedidos de ajuda separadamente.
6. Se usar *think aloud*, explicar e aplicar de forma consistente.
7. Após cada tarefa, registrar satisfação/SEQ ou escala definida.
8. Fazer pós-teste/entrevista breve.
9. Encerrar e explicar uso dos dados.

## C. Resultados — por participante <!--fazer -->

### U01 — {{perfil resumido}}

| Tarefa | Grau de sucesso | Erros | Tipos de erro/dificuldade | Ajudas | Tempo | Satisfação | Evidência/observação |
|---|---|---:|---|---:|---|---|---|
| UT01 | total/parcial/falha | {{n}} | {{...}} | {{n}} | {{mm:ss}} | {{escala}} | {{fala/comportamento}} |

**Link da gravação (se autorizado):** {{...}}  
**Resposta pós-teste:** {{...}}

### U03 — {{perfil resumido}}

| Tarefa | Grau de sucesso | Erros | Tipos de erro/dificuldade | Ajudas | Tempo | Satisfação | Evidência/observação |
|---|---|---:|---|---:|---|---|---|
| UT01 | total/parcial/falha | {{n}} | {{...}} | {{n}} | {{mm:ss}} | {{escala}} | {{fala/comportamento}} |

**Link da gravação (se autorizado):** {{...}}  
**Resposta pós-teste:** {{...}}

### U03 — {{perfil resumido}}

| Tarefa | Grau de sucesso | Erros | Tipos de erro/dificuldade | Ajudas | Tempo | Satisfação | Evidência/observação |
|---|---|---:|---|---:|---|---|---|
| UT01 | total/parcial/falha | {{n}} | {{...}} | {{n}} | {{mm:ss}} | {{escala}} | {{fala/comportamento}} |

**Link da gravação (se autorizado):** {{...}}  
**Resposta pós-teste:** {{...}}

> Repita para U02, U03...

## D. Consolidação por tarefa <!--fazer -->

| Tarefa | Taxa de sucesso | Tempo típico | Erros recorrentes | Satisfação | Meta atendida? | Problemas prioritários |
|---|---:|---|---|---|---|---|
| UT01 | {{...}} | {{...}} | {{...}} | {{...}} | sim/não | {{...}} |
| UT02 | {{...}} | {{...}} | {{...}} | {{...}} | sim/não | {{...}} |
| UT03 | {{...}} | {{...}} | {{...}} | {{...}} | sim/não | {{...}} |

## E. Achados e recomendações <!--fazer -->

| ID | Achado | Evidência (quant. + qual.) | Impacto | Recomendação | Artefatos a revisar |
|---|---|---|---|---|---|
| AU01 | {{...}} | {{2/4 falharam + fala U03...}} | {{...}} | {{...}} | {{MoLIC/Figma/signos...}} |

## F. Comparação com a avaliação heurística <!--fazer -->

| Problema | Detectado na heurística? | Detectado por usuários? | O que aprendemos |
|---|---|---|---|
| {{...}} | sim/não | sim/não | {{...}} |

## G. Conclusão <!--fazer -->

A conclusão deve responder:

1. Quais metas de usabilidade foram atingidas?
2. Quais problemas foram recorrentes e com quais perfis/tarefas?
3. O que surpreendeu a equipe?
4. Quais mudanças são prioritárias?
5. Que limitações do teste impedem generalizações amplas?

## Checklist

- [ ] Número de participantes finais atende ao enunciado.
- [ ] Participantes são representativos do público e não são membros da equipe.
- [ ] Se foram usados participantes proxy, a justificativa e a limitação estão explícitas.
- [ ] O teste avalia a interação; não confunde usabilidade do protótipo com desempenho técnico do TCC.
- [ ] Tarefas administrativas/analíticas usadas no teste são rastreáveis a objetivos e cenários.
- [ ] Há consentimento e anonimização.
- [ ] Foi realizado teste piloto.
- [ ] Tarefas têm critérios de sucesso definidos antes do teste.
- [ ] Moderadores não ensinaram o caminho durante a tarefa.
- [ ] Resultados estão separados por usuário e por tarefa.
- [ ] Foram registrados sucesso, erros, ajudas, tempo e satisfação quando aplicáveis.
- [ ] Conclusão combina evidência quantitativa e qualitativa.
- [ ] Achados geram recomendações e atualização da rastreabilidade.
