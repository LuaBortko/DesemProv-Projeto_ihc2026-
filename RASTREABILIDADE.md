# Matriz de rastreabilidade de IHC

A matriz deve ser atualizada ao longo do semestre. Ela ajuda a demonstrar que a interface não surgiu arbitrariamente e registra **como o conhecimento da equipe evoluiu**.

Para projetos cujo TCC não previa interface, esta matriz é especialmente importante: deve ficar visível a passagem da **contribuição técnica do TCC** para um **cenário de uso plausível**, e desse cenário para as decisões de interação.

## 1. Derivação do escopo de IHC a partir do TCC

| Elemento | Registro da equipe | Evidência/justificativa | Estado |
|---|---|---|---|
| Tema do TCC | Estrutura e formatação das provas o ENEM: Impacto no desempenho geral dos participantes | TCC | definido |
| Resultado técnico esperado | análise e sistema | TCC | definido |
| O TCC previa interface? | sim | MVP | definido |
| Capacidade/contribuição central | analisar se o formato da prova do ENEM impacta no desempenho dos candidatos | TCC | definido |
| Possíveis beneficiários/stakeholders | docentes e alunos | hipótese | H |
| Usuário escolhido para IHC | docente | pois ele é o único usuário que utiliza o sistema | H |
| Objetivo principal do usuário | Aprimorar as aulas a partir de avaliações que representem de forma mais adequada o desempenho dos estudantes. | [H] | [H] |
| Contexto de uso adotado | Uma docente, ao elaborar uma prova para seus estudantes, deseja garnatir que está os avaliando com base nos conhecimentos obtidos nas aulas, por isso, utiliza nosso sistema para identificar o impacto do formato de sua prova no desempenho de seus alunos. | [H] | H  |
| Interface/recorte de IHC | Sim | O recorte existe, correspondendo ao MVP do TCC. | revisada |
| Relação com o TCC | parte prevista | [F] | definido |

> Se o escopo de IHC mudar ao longo do semestre, preserve a decisão anterior no histórico e registre **qual evidência motivou a mudança**.

## 2. Registro de hipóteses e lacunas da Entrega 1

Use esta tabela para itens importantes marcados como `[H]` ou `[?]`. Preserve o histórico: não apague uma hipótese refutada.

| ID | Afirmação / dúvida inicial | Tipo | Por que importa | Como/onde investigar | Evidência obtida | Estado atual | Impacto no projeto |
|---|---|---|---|---|---|---|---|
| H01 | O formato da prova impacta do desempenho do aluno | H | Fundamenta a proposta do TCC, pois é necessário verificar se características estruturais da prova apresentam relação com o desempenho dos candidatos. | TCC | [link repositório tcc](https://github.com/beatrizmanaia26/TCC-DesempenhoEnem) | fechado | média |
| H02 | Poderá fornecer subsídios para que professores e elaboradores de provas avaliem características estruturais de suas avaliações, contribuindo para ajustes que tornem o nível de dificuldade mais adequado aos objetivos propostos | H | Permite verificar se os resultados obtidos pelo TCC possuem aplicabilidade prática e podem efetivamente apoiar a elaboração e revisão de avaliações. | TCC | MVP | fechado | alto |
| H03 | Aprimorar as aulas a partir de avaliações que representem de forma mais adequada o desempenho dos estudantes | H | Permite avaliar se a utilização dos resultados pode contribuir para o processo de ensino, indo além da análise das avaliações em si.| Entrega 7 | Não tem | fechado | alto |
| H04 | Um docente do Estado de São Paulo precisa ter um mínimo de conhecimento tecnológico | H | É importante para compreender o perfil e o contexto de uso do público-alvo, orientando o desenvolvimento de uma interface compatível com suas necessidades e conhecimentos tecnológicos. | Entrega 3 - persona 1 e 3, entrega 4 e Entrega 7 | Estamos desenvolvendo um sistema que apresenta funcionalidades básicas por parte do usuário, como fazer upload e conectar o dispositivo à intenret, com base nisso, difernetes tipos de personas, como as exploradas na entrega3 conseguem utilizar o sistema, desde que tenham o mínimo de conhecimento tecnológico. | fechado | alto |
| H05 | Os docentes utilizariam a interface durante a elaboração ou revisão das avaliações, antes de sua aplicação. | H | Não tem. | Entrega 3(persona 1 e 3) e 7 | Permite compreender em que períodos a interface seria utilizada | fechado | baixa |
| H06 | O detalhamento de como cada métrica foi calculada pode auxiliar os docentes na interpretação dos resultados. | H | Permite investigar a necessidade de explicações adicionais sobre os resultados apresentados pela interface. | Entrega 7 | Entrega 2 e [link repositório tcc](https://github.com/beatrizmanaia26/TCC-DesempenhoEnem)  | fechado | alto |
| H07 | Os docentes possuem conhecimento prévio de ferramentas voltadas à criação, gerenciamento ou análise de avaliações. | [?] | Permite identificar a familiaridade dos docentes com ferramentas semelhantes e compreender como essa experiência pode influenciar suas expectativas e sua interação com a interface proposta. | Entregas 2,3(persona 1 e 3) e 7 | Não tem | fechado | alto |
| H08 | A apresentação das métricas pode auxiliar os docentes a decidir quais características estruturais da avaliação devem ser mantidas ou ajustadas. | H | Permite investigar se os resultados apresentados são suficientes para apoiar decisões durante a revisão da prova. | Entrega 7 | Entrega2 | fechado | alto |
| H09 | Aluno poderia ser afetado pelo sistema indiretamente | H | Caso o aluno seja impactado pelo sistema indiretamente ao utilizar o resultado (prova), características desses indivíduos poderiam ser levadas em consideração e validadas pelo sistema | Entrega 3 - persona 02 | Não consideramos que o aluno tem impacto no sistema de avaliação com base no ENEM pois o seu desenvolvimento é pautado apenas nas análises das provas do ENEM, sem sofrer influências de caraterísticas específicas dos alunos. | fechado | baixo |
| H10 | Após identificar resultados abaixo do esperado em uma avaliação, o docente pode querer analisar suas características estruturais para investigar possíveis fatores que contribuam para o desempenho dos alunos. | H | Permite investigar se existe a necessidade de utilizar o sistema após a aplicação de uma avaliação, apoiando a reflexão sobre os resultados obtidos e o planejamento de melhorias em avaliações futuras. | Entrega 7 | Cenário hipotético (C01) | fechado | Média |
| H11 | Ao preparar avaliações diferentes para turmas distintas, o docente pode querer comparar suas características estruturais para identificar diferenças que mereçam revisão antes da aplicação. | H | Permite investigar se a comparação entre versões de uma avaliação é uma necessidade relevante e se as informações fornecidas pelo sistema podem apoiar a revisão das provas. | Entrega 7 | Cenário hipotético | fechado | Média |

## 3. Rastreabilidade entre contribuição técnica, necessidades e artefatos
<!-- Usei de "metrica" pra esse a parte final do doc2 (top 5) -->
<!-- Como tava antes 
| R01 | Apresentação visual das métricas | O docente precisa consultar e interpretar diferentes métricas relacionadas à prova | P01, P02 e P03 | {{C01}} | {{T01}} | {{links}} | {{...}} | {{M01}} | {{F01...}} | {{V01 ou —}} | {{UT01}} | {{...}} |
-->
<!-- Coloquei a C02 também como situação problma por conta da entrega 5 mencionar a C02 na T01 - Assinado, Nuno <3 -->
| ID | Capacidade do TCC utilizada | Necessidade/problema | Persona | Cenário problema | Objetivo/tarefa | HTA/GOMS/CTT | Cenário de interação / signos | MoLIC | Tela(s) Figma | Heurística / problema | Tarefa no teste | Decisão/melhoria |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| R01 | Apresentação visual das métricas | O docente precisa consultar e interpretar diferentes métricas relacionadas à prova | P01 e P03 | C01, C02 e C03 | Consultar os resultados da análise | T01 | `assets\05_tarefas\hta_t01_correcao.jpeg`, `assets\05_tarefas\ctt_t01_correcao.jpeg` | CI01, CI02 e CI03 | M03 | F04, F04.1, F04.4 | UT01 e UT02 | Utilizar diferentes formas de apresentação para organizar e facilitar a interpretação das métricas. |
| R02 | Upload e processamento da prova | A entrada pode exigir conhecimento da estrutura dos dados e configurações adicionais | P01 e P03 | C01, C02 e C03 | Enviar a prova para análise | T01 e T03 | `assets\05_tarefas\hta_t01.jpeg`, `assets\05_tarefas\ctt_t01.jpeg`, `assets\05_tarefas\hta_t03.png`, `assets\05_tarefas\ctt_t03.png` | CI01, CI02 e CI03 | M01 e M02 | F01, F02, F03, F03.1, F03.2, F03.3, F03.4, F02E1, F02E2, F02E3, F02E4 e F03E1 | UT01 e UT02 | Simplificar a etapa de upload e reduzir a quantidade de configurações necessárias. |
| R03 | Explicabilidade das métricas | Métricas e terminologias técnicas podem exigir conhecimento prévio para serem interpretadas | P01 e P03 | C01, C02 e C03 | Compreender o significado das métricas e dos resultados | T01 | `assets\05_tarefas\hta_t01.jpeg`, `assets\05_tarefas\ctt_t01.jpeg` | CI01, CI02 e CI03 | M03 | F04, F04.2, F04.4 | UT01 e UT02 | Apresentar explicações sobre o funcionamento da análise, o significado das métricas e a obtenção dos resultados. |
| R04 | Organização e hierarquia das informações | A apresentação simultânea de muitas informações pode dificultar a consulta dos resultados | P01 e P03 | C01, C02 e C03 | Consultar os resultados da análise | T01 | `assets\05_tarefas\hta_t01.jpeg`, `assets\05_tarefas\ctt_t01.jpeg`| CI01, CI02 e CI03 | M03 | F04, F04.1, F04.2, F04.3 | UT01 e UT02 | Priorizando a visibilidade das informações relevantes e evitar o excesso de elementos na apresentação dos resultados |


## 4. Rastreabilidade de padrões de interface

Use esta tabela quando o projeto incorporar padrões como dashboard, relatório, histórico, filtros ou administração. O objetivo é **justificar o padrão**, não apenas listar telas.
<!-- Como tava antes
| F01 | dashboard | {{T01}} | {{...}} | {{H01/evidência...}} | {{C01/M01}} |
-->
| ID da tela/fluxo | Padrão de interface | Objetivo/tarefa que justifica | Informação/ação principal | Evidência de necessidade | Artefatos relacionados |
|---|---|---|---|---|---|
| F01 | dashboard | Apresentar uma visão geral dos principais resultados da análise | Métricas e indicadores gerais da prova | Dashboard identificado em CO01/CO02 e também em interfaces utilizadas pelo público; permite reunir informações de resultados em uma visão inicial. | CO01,CO02,R01, R04, P01 e P03 |
| F02 | upload | Enviar a prova para processamento e análise | Seleção e envio da prova | CO01, CO02 e CO03 apresentam etapas de entrada de dados. A análise do Xcalibre evidencia que estruturas e parâmetros adicionais podem aumentar a complexidade dessa etapa. | CO01, CO02, CO03, R02, P01 e P03 |
| F03 | detalhamento pós-processamento | Aprofundar a análise após a visualização inicial dos resultados | Detalhes das métricas e explicações sobre os resultados | O padrão foi identificado nas ferramentas analisadas e foi considerado aplicável ao escopo. Também está relacionado à necessidade de explicar métricas e resultados técnicos. | CO02, CO03, R03, R04, P01 e P03 |
| F04 | exportação/download | Armazenar e consultar os resultados posteriormente | Exportação das métricas e resultados | Identificado em uma das ferramentas analisadas, permitindo o usuário armazenar os resultados obtidos | CO03, P01 e P03 |

## 5. Registro de mudanças de escopo

| Data | O que mudou | Evidência/feedback que motivou | Artefatos afetados | Responsável |
|---|---|---|---|---|
| {{...}} | {{...}} | {{...}} | {{...}} | {{...}} |

## Como usar

- Use identificadores estáveis (`H01`, `P01`, `C01`, `T01`, `M01`, `F01`, `UT01`).
- Quando uma necessidade/problema tiver origem em hipótese da Entrega 1, cite o ID correspondente.
- Em TCC sem interface original, pelo menos uma linha deve mostrar claramente **como uma capacidade técnica chega até uma tarefa de usuário e uma tela/fluxo**.
- Uma linha pode se desdobrar quando um objetivo possui múltiplos caminhos.
- Não force relação inexistente: se algo ainda não foi modelado, marque `PENDENTE`.
- Ao remover uma funcionalidade, registre a decisão em vez de apagar silenciosamente o histórico.
- Dashboard, CRUD, filtros e relatórios só devem aparecer quando houver objetivo/tarefa que os justifique.
