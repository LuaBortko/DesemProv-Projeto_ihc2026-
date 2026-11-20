[Dúvida para o professor: há uma inconsistência entre as próprias fontes da disciplina na numeração das heurísticas H5–H8. O modelo `13_avaliacao_heuristica.md` enumera H5 = Prevenção de erros, H6 = Reconhecimento em vez de memorização, H7 = Flexibilidade e eficiência de uso e H8 = Estética e design minimalista. Já a sequência apresentada em `Entrega13-Heuristica.pptx` coloca, após H4, Reconhecimento, Flexibilidade, Estética e somente depois Prevenção, o que corresponde à convenção H5 = Reconhecimento, H6 = Flexibilidade, H7 = Estética e H8 = Prevenção. A equipe utiliza a segunda sequência nas matrizes individuais, mas mantém a primeira lista na seção 1 do próprio documento. No parecer abaixo, tratei isso como inconsistência de padronização e avaliei o conceito da heurística, sem considerar automaticamente que o aluno desconheceu a teoria.]

[O link externo `https://github.com/beatrizmanaia26/TCC-DesempenhoEnem`, registrado como versão avaliada, foi testado e o repositório público está acessível. A correção, entretanto, foi feita sobre o ZIP de 19/11/2026 fornecido para esta equipe, conforme solicitado.]

[Os prints utilizados nas declarações de violações e nos exemplos de boas práticas estão armazenados em `assets/13_heuristica/` e puderam ser analisados visualmente. Não houve impedimento técnico para analisar as evidências.]

[Não foram identificados em `docs/13_avaliacao_heuristica.md` ou na `RASTREABILIDADE.md` comandos destinados ao avaliador ou a uma ferramenta de IA com objetivo de manipular a correção, alterar critérios ou induzir nota. Os comentários HTML encontrados são anotações informais de aula e de trabalho da equipe.]

# Feedback do Professor > Entrega 13 > Equipe 05

## Avaliação geral

A equipe cumpriu a responsabilidade individual desta entrega. Existem três integrantes e foram apresentadas três inspeções identificadas: A01 — Beatriz Manaia Lourenço Berto, A02 — Luana Bortko Rodrigues e A03 — Nuno Martins Guilhermino da Silva. Cada avaliador percorreu as dez heurísticas, registrou violações quando julgou existentes e apresentou exemplos didáticos para as heurísticas consideradas atendidas.

Também foi atendido um ponto importante da atividade: as violações possuem evidência visual. Os seis achados individuais registrados — V01 a V06 — possuem prints associados, e o diretório `assets/13_heuristica/` contém um conjunto amplo de imagens para sustentar tanto problemas quanto exemplos positivos da interface.

A equipe também realizou a consolidação coletiva, agrupando V03/V05 e V04/V06 e mantendo V02 como problema individual aceito pelo grupo. Isso demonstra que a etapa não ficou limitada a três relatórios independentes.

Entretanto, a entrega ainda precisa de correções conceituais e de consolidação antes de ser considerada concluída. O problema mais importante é que o próprio documento utiliza **duas numerações diferentes para H5–H8**. A seção 1 declara uma ordem, enquanto as matrizes individuais e os comentários internos utilizam outra. Assim, não é possível saber apenas pelo ID se `H8`, por exemplo, significa estética/minimalismo ou prevenção de erros. Em uma avaliação heurística, isso compromete diretamente a interpretação dos achados.

Além disso, a consolidação não preservou todos os problemas encontrados: V01, da avaliadora A01, desaparece da seção 7, apesar de tratar de terminologia técnica e parcialmente se sobrepor ao problema consolidado HC01. Há também problemas visíveis nas próprias evidências que não foram reconhecidos de forma consistente, principalmente mensagens como “Network Error”, “Erro ao inicializar o modelo BERT/RoBERTa” e a apresentação de JSON bruto ao docente.

Portanto, a equipe realizou a inspeção e possui material suficiente, mas precisa revisar a **correta associação heurística → problema → evidência → severidade → consolidação**.

## Pontos positivos

- Os três integrantes realizaram avaliações individualizadas e identificadas.
- O escopo lista explicitamente as telas e estados avaliados.
- A equipe incluiu estados de sucesso, erro, filtros, entrada de parâmetros e resultados, e não apenas as telas principais.
- Os três avaliadores percorreram H1–H10.
- A01 identificou corretamente um problema relevante de correspondência com o mundo real relacionado a termos como `IQR` e “texto introdutório”.
- A02 e A03 identificaram de forma independente a ambiguidade do uso de `Q1`, `Q2` e `Q3` na explicação dos quartis, o que dá força ao achado consolidado.
- A02 e A03 também identificaram independentemente o problema de permitir a entrada de duração acima do limite antes de apresentar o erro.
- Há tentativa de justificar severidade considerando frequência e impacto.
- As recomendações propostas são, em geral, direcionadas à causa do problema e não apenas descrições vagas.
- A equipe forneceu exemplos visuais para as heurísticas consideradas não violadas.
- Os exemplos de visibilidade do estado do sistema são concretos: carregamento, mensagens de erro, preenchimento de dificuldade e impossibilidade de apresentar determinados gráficos.
- Os exemplos de controle e liberdade mostram caminhos de retorno, remoção do arquivo e recuperação de estados de erro.
- A ajuda contextual por tooltips é um elemento real da interface e faz sentido como exemplo para ajuda/documentação.
- A consolidação possui responsáveis definidos para as correções.
- A equipe diferencia inspeção individual da etapa posterior de consolidação no procedimento descrito.

## Correções prioritárias

### 1. Padronizar imediatamente a numeração de H5–H8

O documento utiliza duas convenções diferentes.

Na seção “Heurísticas adotadas”, vocês registram:

- H5 — Prevenção de erros;
- H6 — Reconhecimento em vez de memorização;
- H7 — Flexibilidade e eficiência de uso;
- H8 — Estética e design minimalista.

Entretanto, nas matrizes individuais vocês utilizam, na prática:

- H5 — Reconhecimento em vez de memorização;
- H6 — Flexibilidade e eficiência de uso;
- H7 — Estética e design minimalista;
- H8 — Prevenção de erros.

Isso aparece claramente em V04 e V06: o problema é permitir inserir duração acima de seis horas, que conceitualmente é um problema de **prevenção de erros**, mas foi registrado como H8 porque a matriz segue a segunda convenção.

O mesmo deslocamento aparece nas boas práticas.

Antes de qualquer outra revisão, escolham a convenção oficial adotada pela disciplina e mantenham o mesmo ID em:

- lista inicial;
- matrizes de cobertura;
- declarações de violação;
- boas práticas;
- consolidação;
- rastreabilidade.

Sugiro também registrar temporariamente **ID + nome da heurística** durante a revisão. Assim, um erro de numeração deixa de esconder o conceito.

### 2. A consolidação perdeu o achado V01 de A01

A01 registrou V01 como violação relacionada a termos pouco claros, incluindo:

- `IQR`;
- “texto introdutório”;
- outras expressões técnicas.

A02 registrou V03 e A03 registrou V05, ambos relacionados ao uso de `Q1`, `Q2`, `Q3` e `IQR`.

Na consolidação, HC01 reúne apenas:

> V03(A02), V05(A03)

V01(A01) desapareceu.

Isso viola a finalidade da consolidação, que deve preservar os achados individuais e decidir se eles:

- são o mesmo problema;
- são partes de um problema maior;
- ou devem permanecer como problemas distintos.

A equipe precisa revisar V01.

Se considerar que V01, V03 e V05 fazem parte do mesmo problema de terminologia técnica/ambiguidade na explicação de quartis, então HC01 deve preservar os três avaliadores.

Se “texto introdutório” constituir um problema diferente, criem outro achado consolidado.

O que não pode acontecer é um problema individual simplesmente desaparecer.

### 3. A interface possui problemas evidentes de linguagem técnica que não foram consolidados

As próprias imagens da entrega mostram mensagens como:

> “Network Error”

> “Erro ao inicializar o modelo BERT”

> “Erro ao inicializar o modelo RoBERTa”

Esses exemplos são particularmente importantes porque o usuário prioritário é o docente, e BERT/RoBERTa são detalhes internos da implementação.

Isso pode violar a **correspondência entre sistema e mundo real**, pois a interface está usando linguagem do sistema/desenvolvedor.

Também pode afetar a heurística de **reconhecimento, diagnóstico e recuperação de erros**, porque a mensagem deve explicar o problema em linguagem compreensível e orientar a recuperação.

A situação já havia sido identificada nas entregas anteriores e deveria ser um alvo natural da inspeção heurística.

No entanto, A01 utiliza imagens de BERT/RoBERTa dentro da argumentação de que o tratamento de erros atende à heurística.

A equipe precisa rever essa conclusão.

Uma mensagem pode ser visualmente bem destacada e ainda assim utilizar vocabulário inadequado.

### 4. “Network Error” não é uma boa mensagem para o usuário final

Na imagem de falha ao preparar a análise, o sistema apresenta literalmente:

> “Network Error”

Isso não explica ao professor:

- o que falhou;
- se o arquivo está correto;
- se a análise chegou a começar;
- se o problema é conexão, servidor ou processamento;
- o que “Tentar novamente” efetivamente fará.

Esse é um exemplo forte para discutir correspondência com o mundo real e recuperação de erro.

A inspeção deveria ter identificado esse problema, sobretudo porque o próprio material da disciplina destaca que mensagens de erro devem usar linguagem simples e construtiva.

### 5. A apresentação de JSON bruto deveria ter sido discutida na inspeção

Em um dos estados de erro da análise, a interface apresenta diretamente:

> “JSON da prova”

seguido da estrutura interna dos dados.

Para um docente, isso não corresponde à linguagem do domínio.

Além de correspondência com o mundo real, essa decisão pode gerar um problema de estética/minimalismo, pois ocupa grande espaço com informação técnica que provavelmente não é necessária à tarefa.

Se o JSON for apenas recurso de desenvolvimento/debug, ele não deveria aparecer na interface destinada ao professor.

A inspeção heurística é exatamente o momento de detectar esse tipo de vazamento da implementação para a interface.

### 6. Revisar V02/HC02: botões diferentes não são automaticamente inconsistência

A01 considera uma violação de consistência o fato de algumas mensagens de erro apresentarem:

> “Entendido”

e outras:

> “Tentar novamente”.

Antes de classificar isso como inconsistência, é necessário verificar se as ações realmente possuem a mesma semântica.

Nos prints:

- um arquivo com formato inválido não será corrigido apenas repetindo a mesma análise; o usuário precisa escolher outro arquivo;
- um erro de processamento pode permitir efetivamente tentar a mesma operação novamente.

Portanto, diferentes rótulos podem ser adequados quando representam **ações diferentes**.

A inconsistência existiria se duas ações equivalentes fossem nomeadas de formas diferentes, ou se o mesmo rótulo produzisse comportamentos diferentes.

A recomendação consolidada:

> “padronizar todos os botões de erro para ‘Tentar novamente’”

pode inclusive piorar a interface, pois “tentar novamente” não resolve um DOCX enviado no lugar de PDF ou um arquivo que excede o limite.

Revisem HC02 perguntando primeiro: **qual é a recuperação correta para cada tipo de erro?**

### 7. A classificação e justificativa de HC01 como severidade 3 precisa ser mais rigorosa

HC01 recebeu severidade 3 — problema maior, alta prioridade.

Essa classificação pode ser defensável se a ambiguidade comprometer realmente a interpretação das métricas e as decisões do docente.

Porém, a justificativa individual ainda está baseada principalmente em:

> “pode confundir”

e no fato de que acontece quando o tooltip é acessado.

Para severidade 3, é importante argumentar explicitamente:

- frequência;
- impacto;
- persistência.

Por exemplo, a equipe precisa discutir se o usuário consegue superar a dúvida lendo o restante da interface, se a interpretação errada altera uma decisão importante e se o problema reaparece repetidamente.

Não diminuam ou aumentem a severidade apenas pelo “quanto o problema parece feio”. A escala deve apoiar priorização.

### 8. A síntese afirma que não há problema “grave”, apesar de existir severidade 3

A seção 8 afirma:

> “Nenhum problema é classificado como crítico ou grave”.

Entretanto, HC01 possui severidade 3.

Na própria escala da entrega, severidade 3 significa:

> problema maior; alta prioridade.

Portanto, a síntese deveria dizer que:

- não houve problema de severidade 4/catastrófico;
- existe pelo menos um problema de severidade 3/alta prioridade.

Essa distinção importa porque severidade 3 é justamente um problema que merece correção prioritária.

### 9. A boa prática de prevenção de erros está misturando prevenção com tratamento de erro

Em uma das boas práticas, a equipe argumenta que a heurística de prevenção é atendida porque:

> “todos os possíveis erros são informados tanto visualmente quanto textualmente”.

Informar um erro **depois que ele ocorreu** está mais relacionado a reconhecimento/diagnóstico/recuperação.

Prevenção significa evitar que o erro aconteça quando isso for possível.

O próprio achado sobre duração acima de seis horas mostra a diferença:

- permitir 8 horas e depois mostrar erro = tratamento/validação;
- impedir ou limitar a entrada acima de 6 horas = prevenção.

A equipe precisa revisar os exemplos de prevenção para demonstrar mecanismos que realmente evitem situações inválidas antes de o usuário se comprometer com a ação.

### 10. As boas práticas de H5–H8 precisam ser revisadas depois da padronização dos IDs

Por causa da dupla numeração, vários exemplos estão associados ao ID errado quando comparados à seção 1 do próprio documento.

Conceitualmente, os exemplos são aproveitáveis:

- instruções e opções visíveis → reconhecimento em vez de memorização;
- teclado, setas e diferentes maneiras de entrada → flexibilidade/eficiência;
- apenas informações relevantes → estética/minimalismo;
- limites e validações → prevenção de erros.

O problema está no ID.

Corrijam as matrizes e as seções de boas práticas para que o leitor não precise descobrir qual convenção vocês estavam usando em cada linha.

### 11. H1 está sendo confundida parcialmente com ajuda e explicação de conteúdo

Em A01, a boa prática de H1 menciona:

> “Há informações das métricas em tooltips”

e

> “informação de como preencher um campo”.

Isso não é o núcleo de visibilidade do estado do sistema.

H1 pergunta principalmente se o sistema comunica **o que está acontecendo naquele momento**:

- upload aceito;
- análise em processamento;
- campo válido/inválido;
- operação concluída;
- resultado indisponível;
- filtro aplicado.

Tooltips explicativos pertencem mais naturalmente a reconhecimento/ajuda/documentação.

A seção de boas práticas posterior apresenta exemplos de H1 mais adequados, como carregamento, erros e estado dos dados. Utilizem esses exemplos e retirem justificativas que tratam qualquer explicação como “status do sistema”.

### 12. H3 não significa que literalmente “todas as ações” precisam ser desfeitas/refeitas

A01 afirma:

> “todas as ações do usuário podem ser refeitas/desfeitas”.

Além de ser uma afirmação difícil de sustentar apenas pelos exemplos, H3 não exige necessariamente um mecanismo universal de undo/redo.

A heurística enfatiza controle, liberdade e saída de estados indesejados.

Os exemplos de:

- remover o arquivo;
- retornar;
- cancelar;
- corrigir entrada;
- mudar filtro;

são suficientes e mais precisos.

Evitem transformar a heurística em uma promessa técnica absoluta que a interface pode não cumprir.

### 13. A02 classifica H4 como boa prática enquanto A01 encontra uma violação H4; a consolidação precisa deixar claro o julgamento final

Avaliações individuais podem — e devem — divergir. Isso é normal.

A02 não identificou violação de consistência e apresenta os erros como exemplo de padronização.

A01 identificou V02 justamente nos botões desses erros.

A equipe consolidou V02 como HC02, portanto houve uma decisão coletiva.

A documentação deveria deixar claro que:

- A02 originalmente julgou o comportamento consistente;
- após a consolidação, a equipe aceitou ou rejeitou o problema;
- o resultado consolidado prevalece como decisão final.

Isso ajuda a demonstrar a função da etapa de consolidação e evita manter duas conclusões conflitantes sem explicação.

### 14. Os IDs de telas e estados estão inconsistentes ao longo da entrega

Aparecem variantes como:

- `f04_3`;
- `F04.3`;
- `F04_3`;
- `F03.e1`;
- `f03e1`;
- `F02_E3`;
- `F2E1`.

Também existem referências provavelmente digitadas incorretamente como `f03e3`, `f04e4` e `f03)2`.

Esse problema já apareceu em entregas anteriores.

Em uma inspeção heurística, a localização do problema é parte essencial do relato. Portanto, o identificador da tela precisa ser inequívoco.

Padronizem os IDs exatamente como na Entrega 11 e usem a mesma convenção em:

- escopo;
- matriz individual;
- violação;
- boa prática;
- consolidação;
- rastreabilidade.

### 15. A coluna “IDs dos achados” está sendo usada para listar telas quando não existe violação

Nas matrizes individuais, quando a heurística não foi violada, a coluna “IDs dos achados” contém frequentemente uma lista de telas.

Exemplo: A01 em H1 lista vários IDs de telas, embora “Houve violação?” esteja marcado como “não”.

A finalidade daquela coluna é referenciar achados de violação, como V01, V02 etc.

Quando não houver violação:

- deixem “IDs dos achados” vazio ou com `—`;
- descrevam o exemplo positivo na coluna apropriada;
- utilizem a seção 6 para apresentar sua evidência.

Isso torna a matriz mais fácil de interpretar.

### 16. A consolidação precisa preservar a origem de todos os achados e explicar divergências de severidade

O material teórico prevê que, depois das inspeções individuais, os avaliadores compartilhem os problemas e possam **rejulgar a severidade** antes de chegar ao valor final.

Na consolidação atual, a severidade final aparece diretamente, mas não é explicado:

- se os avaliadores discutiram o valor;
- se alguém alterou sua avaliação;
- como decidiram o valor final.

Isso é especialmente relevante para HC01, onde dois avaliadores chegaram a problema semelhante e severidade 3.

Uma frase curta explicando o procedimento de consolidação já resolveria essa lacuna.

### 17. A afirmação “as devidas correções já foram aplicadas” precisa ser demonstrada

A síntese termina afirmando:

> “As devidas correções já foram aplicadas com base nessas diretrizes.”

Porém, a Entrega 13 apresenta como evidência justamente as telas com os problemas.

Se as correções realmente foram realizadas depois da inspeção, documentem:

- qual achado foi corrigido;
- qual tela/estado foi alterado;
- qual versão contém a correção;
- eventualmente um print posterior.

Não é necessário apagar a evidência original da violação — ela deve ser preservada como histórico.

O que precisa existir é rastreabilidade entre **problema encontrado → decisão → correção realizada**.

### 18. Atualizar a `RASTREABILIDADE.md` com os achados consolidados da Entrega 13

A matriz de rastreabilidade ainda não incorpora HC01, HC02 e HC03 na coluna destinada à heurística/problema.

Além disso, o cabeçalho da tabela continua desalinhado com o conteúdo: `UT01 e UT02` aparece onde deveria estar o problema heurístico.

A Entrega 13 é exatamente o momento de preencher essa ligação.

Depois da correção da consolidação, registrem:

- tela/estado;
- achado consolidado;
- tarefa afetada;
- decisão de correção;
- versão/tela alterada.

Isso preparará adequadamente a comparação com a observação de usuários da Entrega 14.

### 19. Não considerar H2/H9 plenamente atendidas enquanto a interface expuser linguagem interna

A interface ainda contém elementos como:

- `IQR`;
- BERT;
- RoBERTa;
- `Network Error`;
- JSON.

Alguns termos estatísticos podem ser necessários, desde que explicados.

BERT, RoBERTa, JSON e `Network Error`, porém, são exemplos claros de linguagem orientada à implementação.

Portanto, a conclusão de que o sistema sempre apresenta erros em “linguagem clara e compreensível” está forte demais.

A avaliação heurística deve justamente evitar esse tipo de afirmação absoluta.

### 20. Revisar o checklist após as correções

O checklist está totalmente marcado.

Entretanto:

- V01 não foi consolidado;
- existe dupla numeração de H5–H8;
- há problemas visuais relevantes não reconhecidos;
- IDs de telas estão inconsistentes;
- a rastreabilidade ainda não está atualizada;
- a afirmação de correções realizadas não está demonstrada.

Portanto, alguns itens precisam ser reavaliados antes de manter o status “Concluída”.

## Recomendações de melhoria

### 1. Utilizar sempre “ID + nome da heurística” durante a revisão

Enquanto houver risco de confusão de numeração, escrevam, por exemplo:

`H2 — Correspondência entre o sistema e o mundo real`

Isso evita que o número seja corrigido e o conceito permaneça errado — ou vice-versa.

### 2. Diferenciar três tipos de resultado

Na revisão, separem:

- **violação** — problema encontrado;
- **boa prática** — evidência didática de atendimento;
- **oportunidade de melhoria** — algo que poderia melhorar, mas não chega a constituir violação.

Isso evita forçar problemas apenas para preencher a tabela.

### 3. Revisar todos os estados de erro com duas perguntas

Para cada mensagem de erro:

1. O professor entende o que aconteceu sem conhecer a implementação?
2. A mensagem orienta uma ação de recuperação realmente possível?

Essa revisão provavelmente encontrará problemas mais importantes do que apenas a diferença entre “Entendido” e “Tentar novamente”.

### 4. Preservar as inspeções individuais mesmo quando o grupo discorda

Não apaguem as diferenças entre avaliadores.

A consolidação é valiosa justamente porque mostra:

- problema encontrado por um avaliador;
- problema encontrado por vários;
- discordância;
- decisão final da equipe.

Esse histórico ajuda a compreender a robustez do achado.

## Pontos que devem alimentar as próximas entregas

- **Entrega 14:** verificar se problemas de terminologia realmente aparecem durante o uso por docentes.
- **Entrega 14:** observar se `IQR`, quartis, correlação e demais termos exigem ajuda ou geram interpretações incorretas.
- **Entrega 14:** observar como participantes reagem a mensagens como BERT/RoBERTa e `Network Error`, caso ainda estejam presentes.
- **Entrega 14:** verificar se os usuários conseguem recuperar-se dos estados de erro sem intervenção do moderador.
- **Entrega 14:** comparar problemas encontrados pela inspeção com problemas efetivamente observados.
- **Interface:** substituir linguagem de implementação por linguagem orientada à tarefa do docente.
- **Interface:** rever a exposição de JSON bruto.
- **Rastreabilidade:** registrar HC01–HC03 e futuras correções.
- **Rastreabilidade:** manter o histórico mesmo quando um problema for corrigido.
- **Inspeção:** após corrigir a numeração, revisar novamente H5–H8 para garantir que nenhuma heurística tenha ficado sem avaliação real.

## Síntese das ações recomendadas

1. **Resolver a inconsistência de numeração H5–H8 em todo o documento.**
2. **Revisar V04/V06 e todas as boas práticas H5–H8 usando uma única convenção.**
3. **Incluir V01 na consolidação — junto de HC01 ou como problema consolidado separado.**
4. **Reavaliar as mensagens `Network Error`, BERT/RoBERTa e a exposição de JSON como possíveis violações.**
5. **Revisar HC02: “Entendido” e “Tentar novamente” podem representar ações diferentes e não necessariamente uma inconsistência.**
6. **Reformular a recomendação de HC02 conforme a recuperação correta para cada erro.**
7. **Justificar com mais rigor a severidade 3 de HC01.**
8. **Corrigir a síntese: existe problema de severidade 3/alta prioridade, embora não exista severidade 4.**
9. **Distinguir prevenção de erros de tratamento/recuperação após o erro.**
10. **Padronizar todos os IDs de telas e estados.**
11. **Deixar a coluna “IDs dos achados” apenas para V01, V02 etc., e não para listas de telas quando não há violação.**
12. **Documentar como a severidade final foi decidida na consolidação.**
13. **Se as correções já foram implementadas, registrar evidência da versão corrigida sem apagar o histórico da violação.**
14. **Atualizar a `RASTREABILIDADE.md` com os achados consolidados e decisões de melhoria.**
15. **Refazer o checklist depois dessas correções.**

A equipe realizou uma inspeção de verdade, com três avaliadores, prints e problemas concretos. O próximo passo é aumentar o rigor da classificação. Em avaliação heurística, não basta encontrar “algo estranho”: precisamos conseguir dizer **qual princípio foi violado, onde, por que isso prejudica o usuário e qual é a gravidade real**. E um detalhe importante: às vezes o problema mais sério não é o botão dizer “Entendido” em vez de “Tentar novamente”; é a interface estar conversando com um professor em BERT, RoBERTa, JSON e `Network Error`. 🙂
