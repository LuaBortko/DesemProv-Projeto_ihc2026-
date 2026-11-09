# Entrega 13 — Avaliação de IHC por inspeção heurística

**Data:** 08/11/2026  <br> 
**Status:**  🟨 Em andamento <br> 
**Responsabilidade:** 1 avaliação completa por integrante, sobre todas as telas/estados relevantes do projeto.<br> 
<!--
criado p busc aproblema de usabilidade

1-criar fluxograma pra se tiver q desenha flux ode valaicao heruistica esses sao os passos, quantas vezes repete cad aum...

PASSO A PASSO DA HERUSTICA: FLUXOGRAMA Q CRIAREMOS 9anotacao topico 13)

Metodo baseado em inspecao, que mfaz inspeco somos nos especialistas 

todo metodo de avalaicao é baseado em 
-prearacao
-coleta de dados
-interpretacao
-consolidacao
-relato dos resultados

Teste de usabilidade nao tem usuario, é so especialista, pego heuristicas (regras parecidas com diretrizes) e do ranking dd atrnedimento ou n (ranking de violacao), indico quem violou  

No mercado indciamos violacoes 

Na entrega do plinio: avlaiamos interface fazendo relatorio de heuristica, nos como especialsitas avaliando heuristica, indicando onde violou ex se tela violou todas as heuristics tenho exemplo de violacao, se nao tive violacao heuristica n estudo baseado em nd pq nao violei. 

Ai pro plinio indico oq nao violei, oq foi atendido na avlaaicao heuristica 

Avalaicao heuristica de mercado mostra oq a pessoa violou e qual o prejuizo, impacto daquela violacao 

Pra disciplina coloca tb oq fizemos de bom 

Prototipo uso p avaliacao herusitica e teste de obs de usuario  

No mercado n faco avaliacao heurstica cm msm equipe q fez software pq tem regra de pricnipios de design e vo ve se desrregulou esses principios  
-->
## Objetivo da atividade

Encontrar problemas de usabilidade por inspeção sistemática da interface com as **10 heurísticas de Nielsen**. Cada avaliador trabalha individualmente primeiro; depois a equipe consolida problemas duplicados e prioridades.

> **Parte de violações:** registre somente problemas reais. Não invente uma violação para “preencher” cada heurística. Para provar que todas foram exercitadas, use a **matriz de cobertura H1–H10**. Para heurísticas sem violação, a disciplina solicita um exemplo didático de boa prática.

## 1. Heurísticas adotadas

1. Visibilidade do status do sistema
2. Compatibilidade entre o sistema e o mundo real
3. Controle e liberdade do usuário
4. Consistência e padrões
5. Prevenção de erros
6. Reconhecimento em vez de memorização
7. Flexibilidade e eficiência de uso
8. Estética e design minimalista
9. Ajudar usuários a reconhecer, diagnosticar e recuperar-se de erros
10. Ajuda e documentação

## Cobertura especial para interfaces administrativas e analíticas

Quando existirem, não limite a avaliação às “telas principais”. Inspecione também:

- dashboard em estados normal, vazio e erro;
- filtros sem resultado e filtros combinados;
- relatórios e exportação;
- histórico/listas longas;
- formulários CRUD (criação, edição, exclusão, validação);
- alteração de perfil/permissão;
- confirmações de ações destrutivas;
- processamento/loading/progresso;
- falha e recuperação;
- comparação de resultados;
- mensagens de termos técnicos, métricas e recomendações;
- ajuda/documentação contextual.

Em TCCs técnicos, observe especialmente se a interface comunica o estado do processamento e traduz informações técnicas para o vocabulário do usuário escolhido.

## 2. Escopo da inspeção

| Item | Definição |
|---|---|
| Versão avaliada | verão atual do código disponível em: [Repositório TCC](https://github.com/beatrizmanaia26/TCC-DesempenhoEnem) |
| Telas/estados | f01, f02, f02e1, f02e2, f02e3, f02e4, f03, f03_1, f03_2, f03_3, f03_4, f03e1, f04, f04_1, f04_2, f04_3, f04_4, f04_5,|
| Fluxos | M01/M02/M03 |
| Dispositivo/viewport | Notebook |
| Avaliadores | Beatriz Manaia Lourenço Berto, Luana Bortko Rodrigues, Nuno Martins Guilhermino da Silva |

## 3. Procedimento individual

Cada avaliador deve:

1. percorrer os fluxos/telas ao menos uma vez para familiarização;
2. inspecionar novamente aplicando sistematicamente H1–H10;
3. registrar cada problema com evidência e contexto;
4. atribuir severidade **depois de compreender bem o problema**, justificando a decisão;
5. não discutir achados com os demais antes de terminar a inspeção individual, quando o objetivo for preservar independência.

### Escala de severidade (0–4)

| Grau | Interpretação |
|---:|---|
| 0 | não é considerado problema de usabilidade |
| 1 | problema cosmético; corrigir se houver tempo |
| 2 | problema menor; baixa prioridade |
| 3 | problema maior; alta prioridade |
| 4 | catástrofe de usabilidade; correção imperativa antes de disponibilizar |

Ao justificar, considere **frequência, impacto e persistência** do problema no contexto real de uso.

---

## Avaliador A01 — Beatriz Manaia Lourenço Berto

### 4. Matriz de cobertura das 10 heurísticas

| Heurística | Telas/fluxos examinados | Houve violação? | IDs dos achados | Exemplo de boa prática se não violada |
|---|---|---|---|---|
| H1 | {{...}} | sim/não | {{V01...}} | {{...}} |
| H2 | {{...}} | sim/não |  |  |
| H3 | {{...}} | sim/não |  |  |
| H4 | {{...}} | sim/não |  |  |
| H5 | {{...}} | sim/não |  |  |
| H6 | {{...}} | sim/não |  |  |
| H7 | {{...}} | sim/não |  |  |
| H8 | {{...}} | sim/não |  |  |
| H9 | {{...}} | sim/não |  |  |
| H10 | {{...}} | sim/não |  |  |


### 5. Declaração de violações

| ID | Heurística | Tela/estado | Problema observado | Evidência | Severidade | Justificativa da severidade | Recomendação |
|---|---|---|---|---|---:|---|---|
| V01 | H1 | {{F02}} | {{o que ocorre, em que ação e qual consequência}} | ![print](../assets/13_heuristica/v01.svg) | 3 | {{frequência/impacto/persistência}} | {{correção específica}} |

**Qualidade do relato:** o problema deve ser observável e localizado. Evite “interface confusa” sem dizer **o que**, **onde**, **quando** e **para quem**.

### 6. Boas práticas — heurísticas não violadas (atividade didática)

| Heurística sem violação | Exemplo no sistema | Evidência | Por que atende |
|---|---|---|---|
| {{H4}} | {{...}} | {{print}} | {{...}} |


## Avaliador A01 — Luana Bortko Rodrigues

### 4. Matriz de cobertura das 10 heurísticas

| Heurística | Telas/fluxos examinados | Houve violação? | IDs dos achados | Exemplo de boa prática se não violada |
|---|---|---|---|---|
| H1 | {{...}} | sim/não | {{V01...}} | {{...}} |
| H2 | {{...}} | sim/não |  |  |
| H3 | {{...}} | sim/não |  |  |
| H4 | {{...}} | sim/não |  |  |
| H5 | {{...}} | sim/não |  |  |
| H6 | {{...}} | sim/não |  |  |
| H7 | {{...}} | sim/não |  |  |
| H8 | {{...}} | sim/não |  |  |
| H9 | {{...}} | sim/não |  |  |
| H10 | {{...}} | sim/não |  |  |


### 5. Declaração de violações

| ID | Heurística | Tela/estado | Problema observado | Evidência | Severidade | Justificativa da severidade | Recomendação |
|---|---|---|---|---|---:|---|---|
| V01 | H1 | {{F02}} | {{o que ocorre, em que ação e qual consequência}} | ![print](../assets/13_heuristica/v01.svg) | 3 | {{frequência/impacto/persistência}} | {{correção específica}} |

**Qualidade do relato:** o problema deve ser observável e localizado. Evite “interface confusa” sem dizer **o que**, **onde**, **quando** e **para quem**.

### 6. Boas práticas — heurísticas não violadas (atividade didática)

| Heurística sem violação | Exemplo no sistema | Evidência | Por que atende |
|---|---|---|---|
| {{H4}} | {{...}} | {{print}} | {{...}} |


## Avaliador A01 — Nuno Martins Guilhermino da Silva

### 4. Matriz de cobertura das 10 heurísticas

| Heurística | Telas/fluxos examinados | Houve violação? | IDs dos achados | Exemplo de boa prática se não violada |
|---|---|---|---|---|
| H1 | {{...}} | sim/não | {{V01...}} | {{...}} |
| H2 | {{...}} | sim/não |  |  |
| H3 | {{...}} | sim/não |  |  |
| H4 | {{...}} | sim/não |  |  |
| H5 | {{...}} | sim/não |  |  |
| H6 | {{...}} | sim/não |  |  |
| H7 | {{...}} | sim/não |  |  |
| H8 | {{...}} | sim/não |  |  |
| H9 | {{...}} | sim/não |  |  |
| H10 | {{...}} | sim/não |  |  |


### 5. Declaração de violações

| ID | Heurística | Tela/estado | Problema observado | Evidência | Severidade | Justificativa da severidade | Recomendação |
|---|---|---|---|---|---:|---|---|
| V01 | H1 | {{F02}} | {{o que ocorre, em que ação e qual consequência}} | ![print](../assets/13_heuristica/v01.svg) | 3 | {{frequência/impacto/persistência}} | {{correção específica}} |

**Qualidade do relato:** o problema deve ser observável e localizado. Evite “interface confusa” sem dizer **o que**, **onde**, **quando** e **para quem**.

### 6. Boas práticas — heurísticas não violadas (atividade didática)

| Heurística sem violação | Exemplo no sistema | Evidência | Por que atende |
|---|---|---|---|
| {{H4}} | {{...}} | {{print}} | {{...}} |



> Repita a seção para A02, A03... um avaliador por integrante.

## 7. Consolidação da equipe

Problemas iguais ou muito semelhantes encontrados por avaliadores diferentes devem ser consolidados, preservando quem os encontrou.

| ID consolidado | Achados individuais | Heurística | Problema | Severidade final | Prioridade | Responsável pela correção |
|---|---|---|---|---:|---|---|
| HC01 | V01(A01), V04(A02) | H1 | {{...}} | {{...}} | alta | {{...}} |

## 8. Síntese e plano de melhoria

- Quantidade de problemas por heurística e severidade.
- Problemas críticos/graves que bloqueiam teste ou release.
- Padrões recorrentes entre telas.
- Correções que serão feitas antes/para a avaliação com usuários.

## Checklist

- [ ] Cada integrante fez uma inspeção completa e identificada.
- [ ] Todas as telas/estados relevantes foram examinados.
- [ ] Estados administrativos, filtros, relatórios, históricos, processamento e erros foram incluídos quando existentes.
- [ ] A inspeção avaliou a interface/protótipo, não o mérito técnico do algoritmo/modelo.
- [ ] H1–H10 aparecem na matriz de cobertura de cada avaliador.
- [ ] Parte de violações contém apenas violações, sem “forçar” exemplos.
- [ ] Todo problema tem print/localização e contexto.
- [ ] Severidade possui justificativa, não apenas número.
- [ ] Recomendação resolve a causa ou reduz o impacto.
- [ ] Achados duplicados foram consolidados ao final.
