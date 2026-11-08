# Feedback do Professor > Entrega 08 > Equipe 05

## Avaliação geral

A Entrega 08 apresenta uma base consistente e mostra que a equipe conseguiu reunir decisões provenientes das entregas anteriores para discutir plataforma, princípios e metas de usabilidade. Há uma separação explícita entre contribuição técnica do TCC e camada de interação, existem capacidades e restrições da plataforma, foram formuladas metas qualitativas e quantitativas e o ciclo de Engenharia de Usabilidade de Mayhew foi escolhido como referência para a iteração.

O principal mérito desta entrega está na seção de metas quantitativas: a equipe utilizou as cinco dimensões trabalhadas em aula - **facilidade de aprendizado, facilidade de memorização, eficiência, baixa taxa de erros e satisfação** - e procurou associá-las à tarefa T01. Isso está na direção correta.

Entretanto, existem quatro pontos que precisam ser corrigidos antes de considerar a entrega consolidada.

O primeiro é obrigatório: a seção de **Princípios gerais do projeto não foi organizada nos dois grupos esperados - princípios direcionados ao negócio e princípios direcionados à interface**. A equipe reuniu LGPD, acessibilidade, contexto de uso e projeto centrado no usuário em uma única lista, sem distinguir a natureza de cada princípio.

O segundo é que várias metas quantitativas parecem mensuráveis, mas ainda não estão completamente operacionalizadas. Faltam elementos como população, intervalo de reaplicação, escala de satisfação e justificativa empírica para limites numéricos adotados.

O terceiro é que o ciclo de Mayhew foi citado corretamente, mas sua descrição está curta demais: o texto diz que haverá avaliação, revisão e nova avaliação, mas não explica suficientemente como o ciclo de vida de Engenharia de Usabilidade organiza as fases e quais artefatos deste projeto serão revisitados em cada uma delas.

Por fim, algumas características da plataforma misturam restrições técnicas internas, afirmações de usabilidade ainda não demonstradas e decisões de interface já fechadas. A seção precisa separar com mais cuidado o que é característica real da plataforma do que é uma consequência de design ainda sujeita a validação.

## Pontos positivos

- A equipe separa a contribuição técnica do TCC da camada de interação a ser avaliada em IHC.
- A seção de características da plataforma possui explicitamente **capacidades** e **restrições**, atendendo ao núcleo esperado para essa parte.
- Há preocupação com conectividade, tempo de processamento, privacidade, volume de dados e papéis/permissões.
- Várias características técnicas são traduzidas em possíveis consequências de interação, em vez de serem apenas listadas.
- A equipe registra que o MVP não possui persistência/histórico, o que evita justificar artificialmente telas de histórico apenas porque esse padrão apareceu em entregas anteriores.
- LGPD foi relacionada à minimização, finalidade e transparência no tratamento dos arquivos.
- WCAG 2.2 foi relacionada a teclado, contraste, identificação de erros e não utilização exclusiva de cores.
- A equipe utilizou as cinco metas de usabilidade de Nielsen na seção quantitativa/priorização.
- Todas as metas quantitativas foram associadas a T01, que continua sendo a tarefa mais bem sustentada pelo projeto.
- MU01 possui uma métrica clara de sucesso na primeira tentativa.
- MU03 utiliza tempo de execução como medida de eficiência.
- MU04 procura observar erros e recuperação, o que é mais útil do que simplesmente contar cliques.
- MU05 reconhece que satisfação precisa ser medida após a tarefa.
- O ciclo adotado é a Engenharia de Usabilidade de Mayhew, uma escolha adequada para esta etapa.
- A equipe explicita a ideia de avaliação seguida de revisão e nova avaliação, preservando o caráter iterativo do projeto.

## Correções prioritárias

### 1. Separar obrigatoriamente os princípios em dois grupos: negócio e interface

A seção 2 apresenta uma única relação de princípios:

- contexto de uso;
- LGPD;
- acessibilidade;
- projeto centrado no usuário.

Isso não atende à organização conceitual esperada para esta entrega.

A equipe precisa criar dois grupos claramente identificados.

O primeiro deve reunir **princípios direcionados ao negócio**, ou seja, regras, normas, restrições do domínio, legislação ou políticas que condicionam o funcionamento da solução. A LGPD é um exemplo claro desse grupo.

O segundo deve reunir **princípios direcionados à interface**, como guidelines, padrões de interação, princípios de usabilidade, recomendações de acessibilidade e regras que orientem a construção da interface. WCAG e princípios derivados de projeto centrado no usuário pertencem mais naturalmente a esse grupo.

“Contexto de uso”, isoladamente, não é um princípio ou norma. Ele é uma informação que ajuda a justificar decisões de design. A equipe deve decidir se existe algum princípio concreto derivado desse contexto ou se esse item deve ser deslocado para outra parte da documentação.

O importante não é apenas mudar o título. A equipe precisa demonstrar que compreende a diferença entre **uma regra que condiciona o negócio/sistema** e **uma regra que orienta a interface**.

### 2. Revisar as características da plataforma para separar capacidade, restrição e decisão de design

A equipe fez corretamente duas linhas explícitas para “Capacidades” e “Restrições”, mas outras linhas misturam diferentes níveis de decisão.

Por exemplo, a linha “Software” descreve Vue.js, Node.js e Python e afirma que o usuário “requer npm/Node.js instalado localmente”. Isso entra em conflito com a própria descrição de que o docente utiliza o sistema pelo navegador enquanto frontend, backend e modelos ficam hospedados em servidor cloud.

Se o usuário acessa a aplicação web pelo navegador, dependências de desenvolvimento não devem aparecer como requisito do usuário final.

Outro exemplo é:

> “Interface intuitiva sem necessidade de conhecimento técnico”

Isso não é uma capacidade técnica já comprovada. É uma **meta ou intenção de usabilidade** que deverá ser verificada.

Da mesma forma, “sem persistência” aparece dentro das capacidades, mas funciona mais como restrição/decisão arquitetural do MVP.

A equipe deve revisar a seção perguntando para cada item:

- esta é uma capacidade real da plataforma?
- esta é uma restrição real?
- esta é uma escolha de arquitetura?
- esta é uma característica da interface?
- ou esta é apenas uma solução de design ainda não validada?

A consequência para IHC só deve ser derivada depois dessa classificação.

### 3. Evitar consequências de IHC excessivamente fechadas antes da avaliação

Em várias características, a equipe transforma a condição técnica diretamente em uma solução específica:

- spinner;
- barra/progresso;
- retry automático;
- mensagem de servidor offline;
- checkbox de concordância;
- notificação;
- botão de remoção;
- determinados filtros.

Essas alternativas podem ser adequadas, mas nesta etapa ainda devem ser entendidas como **possíveis respostas de design**, e não como consequências inevitáveis.

Por exemplo, a necessidade de informar que o processamento está ocorrendo é uma consequência de usabilidade. “Utilizar spinner” é uma alternativa específica.

A equipe deve procurar registrar primeiro a necessidade de interação e só depois a alternativa escolhida, preservando espaço para avaliação e revisão.

### 4. Corrigir inconsistências entre as características técnicas

Há alguns pontos da descrição que precisam ser harmonizados.

A equipe afirma:

- processamento no servidor;
- cliente acessando pelo navegador;
- servidor cloud;
- necessidade de npm/Node.js instalado localmente.

Essas afirmações não parecem pertencer ao mesmo cenário de uso.

Também aparece “análise em tempo real”, enquanto outra linha indica processamento entre 10 e 30 segundos e possibilidade de fila de alguns minutos.

Nesse caso, “tempo real” precisa ser usado com cautela. Para o usuário, trata-se de uma análise iniciada sob demanda e que pode exigir espera.

Essas inconsistências técnicas importam em IHC porque alteram a forma como o usuário deve ser informado sobre disponibilidade, espera e falha.

### 5. As metas qualitativas estão adequadas, mas precisam ser claramente diferenciadas das quantitativas

As metas qualitativas são pertinentes ao projeto:

- compreender o envio;
- compreender parâmetros;
- compreender métricas;
- entender limitações;
- recuperar-se de erros;
- perceber a etapa atual.

O problema é que algumas evidências desejadas já se aproximam bastante de critérios observáveis que poderiam ser convertidos em metas quantitativas.

Isso não é necessariamente errado, mas a equipe deve deixar claro o papel de cada conjunto.

As metas qualitativas devem orientar **qualidade da experiência e compreensão**. As quantitativas devem estabelecer critérios verificáveis para decidir se um nível aceitável foi atingido.

### 6. MU01 precisa definir melhor a população e o significado de “sem auxílio”

MU01 estabelece:

> taxa de sucesso na primeira tentativa ≥ 90%

A métrica é apropriada para facilidade de aprendizado.

Entretanto, falta indicar com que população esse percentual será calculado. “Docentes” aparece em outras seções, mas a própria meta deve estar vinculada explicitamente ao perfil que será testado.

Também é necessário definir “sem auxílio”.

Por exemplo:

- perguntar ao moderador conta como auxílio?
- consultar uma ajuda da própria interface conta como auxílio?
- utilizar tooltip conta como auxílio?
- corrigir um erro sozinho continua sendo sucesso?

Essas regras precisam existir antes da aplicação do teste, senão dois avaliadores poderão contabilizar o mesmo comportamento de formas diferentes.

### 7. MU02 não é verificável enquanto o intervalo de memorização não for definido

MU02 pretende medir facilidade de memorização por:

> “taxa de re-conclusão sem ajuda após intervalo de tempo”

A ideia é correta, mas falta justamente o dado que caracteriza memorização: **qual intervalo?**

Repetir a tarefa cinco minutos depois mede algo muito diferente de repeti-la uma semana ou um mês depois.

A equipe deve definir o intervalo considerado coerente com a frequência esperada de uso do sistema.

Esse ponto também se conecta a H05, que ainda investiga quando e com que frequência docentes utilizariam a solução.

### 8. MU03 possui um limite quantitativo sem justificativa suficiente

MU03 define:

> tempo mediano ≤ 15 minutos

A dimensão de eficiência está correta, mas o limite de 15 minutos parece arbitrário.

A justificativa explica por que eficiência importa, mas não explica **por que 15 minutos representa um nível aceitável**.

Além disso, T01 precisa ser delimitada com precisão:

- o cronômetro começa quando o usuário abre a interface?
- quando escolhe o arquivo?
- inclui os 10–30 segundos de processamento do servidor?
- termina quando o dashboard aparece?
- termina apenas quando o usuário interpreta as métricas?

Sem essa definição, o resultado não será comparável.

Também há um erro de formatação no texto da meta (`<=15min>`), que deve ser corrigido.

### 9. MU04 mistura taxa de erro e gravidade, mas mede apenas parcialmente esses conceitos

A meta foi chamada de:

> “taxa e Gravidade de Erros”

mas o critério principal é:

> “< 1 erros por usuário”

e o procedimento prevê registrar erros e tempo de recuperação.

Isso mede quantidade de erros e recuperação, mas não define **gravidade**.

Um erro pequeno, rapidamente corrigido, não deve necessariamente ter o mesmo peso de um erro que impede a conclusão da tarefa ou produz interpretação incorreta de uma métrica.

A equipe deve definir níveis de gravidade ou separar:

- quantidade/taxa de erro;
- capacidade/tempo de recuperação;
- gravidade do problema.

Também é preciso rever a justificativa:

> “docentes com pouco conhecimento tecnológico tendem a cometer mais erros”

Essa afirmação ainda é uma hipótese do projeto, não um fato estabelecido. A própria H04 continua metodologicamente problemática na rastreabilidade.

### 10. MU05 precisa definir a escala de satisfação

MU05 estabelece:

> satisfação > 75%

mas não informa como esse percentual será obtido.

“Questionário curto aplicado imediatamente após a tarefa” ainda não define a métrica.

A equipe precisa especificar:

- qual escala será utilizada;
- quais itens a compõem;
- como será calculada a pontuação;
- o que significa 75%.

Sem isso, “75% de satisfação” não é reproduzível.

Não é necessário adotar obrigatoriamente uma escala específica, mas o instrumento e o cálculo precisam estar definidos antes do teste.

### 11. A priorização usa corretamente apenas as cinco metas de Nielsen, mas pesos iguais não produzem prioridade

A equipe utilizou corretamente:

- facilidade de aprendizado;
- facilidade de memorização;
- eficiência;
- baixa taxa de erro;
- satisfação.

Portanto, a seleção das metas está alinhada ao conjunto solicitado.

Entretanto, todas receberam 20%.

Matematicamente isso soma 100%, mas conceitualmente significa que **nenhuma foi priorizada em relação às demais**.

Se a atividade exige priorização, a equipe deve discutir quais dimensões são mais importantes para este projeto e justificar diferenças de peso.

Neste caso, há boas razões para debater, por exemplo, se compreensão inicial e prevenção de erro deveriam ter maior peso em um sistema de uso potencialmente esporádico e que apresenta métricas técnicas.

Não é necessário chegar a uma distribuição específica. A equipe precisa apenas realizar uma priorização verdadeira, e não transformar “todas são importantes” em sinônimo de “todas têm a mesma prioridade”.

Também devem ser corrigidos os registros `20%%`.

### 12. Descrever efetivamente o Ciclo de Vida de Engenharia de Usabilidade de Mayhew

A escolha de Mayhew está correta.

O texto atual, porém, apenas afirma que:

1. serão realizadas avaliações;
2. problemas serão encontrados;
3. artefatos serão revisados;
4. novas avaliações serão realizadas.

Isso descreve iteração, mas ainda não demonstra o modelo de ciclo de vida adotado.

A equipe deve explicar, de forma resumida, como o processo de Engenharia de Usabilidade organiza o trabalho e relacionar isso ao projeto.

É importante deixar claro que o ciclo envolve, de maneira iterativa, atividades como:

- compreender e especificar requisitos de usabilidade;
- conhecer usuários, tarefas e plataforma;
- estabelecer princípios e metas;
- produzir soluções de design;
- avaliar essas soluções;
- retornar aos artefatos anteriores quando os resultados indicarem problemas.

Não é necessário reproduzir um fluxograma inteiro da teoria, mas o leitor precisa conseguir entender **qual modelo está sendo seguido e onde o projeto se encontra nele**.

### 13. Tornar a seção de iteração específica para os artefatos da Equipe 05

O texto diz genericamente que “requisitos, análise de tarefas e protótipos” poderão ser revisitados.

A equipe já possui artefatos concretos e pode ser mais precisa.

Por exemplo:

- uma dificuldade de compreensão de métrica pode exigir revisão de R03, das explicações do protótipo e das metas relacionadas;
- problemas no envio podem afetar T01, o HTA/GOMS/CTT e o fluxo do protótipo;
- resultados da coleta podem alterar personas, cenários e hipóteses;
- problemas encontrados nas avaliações futuras devem gerar decisão registrada na rastreabilidade.

A seção deve mostrar que o ciclo iterativo não é apenas “corrigir tela”, mas **revisitar o conhecimento que justificou a tela**.

### 14. Atualizar a rastreabilidade para refletir decisões de usabilidade

A `RASTREABILIDADE.md` ainda preserva problemas apontados anteriormente, como H04 marcada como fechada com uma justificativa que não constitui evidência empírica.

Além disso, as metas MU01–MU05 ainda não aparecem integradas à cadeia de rastreabilidade.

Como a Entrega 08 produz critérios que futuramente serão verificados, a equipe deve garantir que as avaliações posteriores consigam responder:

- qual tarefa está sendo avaliada;
- qual meta de usabilidade está sendo medida;
- qual problema foi encontrado;
- qual artefato será revisado;
- qual decisão/melhoria foi tomada.

Não é necessário criar uma estrutura burocrática nova, mas as metas precisam continuar rastreáveis até as Entregas 12–14.

### 15. Revisar o checklist final

O checklist marca quase toda a entrega como atendida, mas deixa desmarcado:

> “Metas poderão ser verificadas nas Entregas 12–14.”

Esse é justamente um dos pontos centrais desta entrega.

Hoje, algumas metas ainda não podem ser verificadas de maneira reproduzível porque faltam definições como intervalo de memorização, escala de satisfação, população e critérios operacionais.

Antes de considerar a entrega concluída, esse item precisa se tornar verdadeiro não por marcar a caixa, mas por corrigir as metas.

## Recomendações de melhoria

### 1. Reduzir detalhes técnicos que não alteram a interação

Informações como memória mínima do servidor, tecnologias internas e detalhes de processamento podem ser importantes para o TCC, mas nesta entrega só devem permanecer se produzirem consequência concreta para a experiência do usuário.

O foco deve ser: **o que essa característica muda na interação?**

### 2. Tratar segurança de forma compatível com a experiência real

Mostrar “cadeado HTTPS” manualmente dentro da interface pode não ser necessário, pois o navegador já possui mecanismos próprios de comunicação de conexão segura.

O ponto importante é informar de forma compreensível:

- que arquivo é enviado;
- para onde vai;
- por quanto tempo permanece;
- para que finalidade é usado.

### 3. Evitar prometer “interface intuitiva”

“Intuitiva” não deve ser uma característica declarada pela própria equipe.

Ela deve ser consequência observada em avaliação.

As metas de aprendizado, erro e satisfação são justamente a forma de transformar esse desejo em algo verificável.

### 4. Relacionar a frequência de uso à memorização

Se o sistema for usado apenas quando o docente prepara uma avaliação, pode haver intervalos relativamente longos entre usos.

Nesse caso, facilidade de memorização pode ganhar importância maior do que em um sistema utilizado diariamente.

Essa é uma boa razão para conectar H05 às metas de Nielsen e à priorização.

#




A equipe está com uma boa base nesta entrega: as cinco metas de Nielsen foram reconhecidas corretamente e existe uma tentativa concreta de transformá-las em medidas. Agora é necessário dar o passo que separa uma “meta com número” de uma **meta de usabilidade realmente verificável**. Escrever “90%”, “15 minutos” ou “75%” é fácil; o trabalho de engenharia de usabilidade começa quando duas pessoas diferentes conseguem aplicar o mesmo protocolo e chegar à mesma conclusão sobre se a meta foi atingida.
