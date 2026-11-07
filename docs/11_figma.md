# Entrega 11 — Protótipo no Figma

**Data:** 05/11/2026  <br> 
**Status:** 🟨 Em andamento  <br> 
**Responsabilidade:** 1 protótipo integrado por equipe cobrindo os fluxos MoLIC. Se a turma exigir divisão individual, identifique o responsável por cada fluxo/tela.<br> 


## Objetivo da atividade

Materializar o modelo de interação em um protótipo navegável, preservando a lógica dos objetivos, tópicos, signos, feedbacks, alternativas e recuperações definidos anteriormente.

## Biblioteca de possibilidades para projetos técnicos

O protótipo deve materializar os fluxos definidos nas entregas anteriores. Dependendo do escopo, podem fazer sentido:

1. **Dashboard:** indicadores, alertas, estado, tendências e atalhos para tarefas frequentes.
2. **Configuração/parametrização:** escolhas, presets, validação e explicação de opções técnicas.
3. **Entrada de dados:** upload, conexão, seleção, pré-visualização e validação.
4. **Processamento:** fila, status, progresso, cancelamento, falha e reexecução.
5. **Relatório/resultados:** síntese, métricas, gráficos, explicação, exportação e compartilhamento.
6. **Histórico:** busca, filtros, ordenação, paginação, detalhes e repetição de execução.
7. **Comparação:** antes/depois, modelo A/B, execução A/B, baseline ou períodos.
8. **Explicabilidade:** confiança, fatores, evidências, limitações e correção/contestação.
9. **Administração:** usuários, grupos, perfis, permissões, integrações e políticas.
10. **CRUDs de domínio:** somente quando criar/consultar/editar/excluir representa tarefa real.
11. **Auditoria/logs:** histórico de alterações e eventos em linguagem adequada.
12. **Alertas/ocorrências:** severidade, impacto, ação, responsável e resolução.
13. **Ajuda/documentação:** apoio contextual a tarefas complexas.

### Estados que não podem ser esquecidos

Quando aplicável, considere: vazio/sem dados; carregamento/processamento; sucesso; erro de entrada; erro de processamento; filtro sem resultados; permissão insuficiente; confirmação de ação destrutiva; cancelamento/desfazer/recuperação; dados desatualizados/conflito.

> Esta lista é repertório de design, **não uma exigência de quantidade de telas**. A rastreabilidade deve explicar por que cada tela existe.

## Link do Figma 

Como alinhado em aula, devido ao projeto de IHC ser do nosso TCC e já termos a prototipação de alta fidelidade (a própria aplicação do TCC), utilizaremos prints da aplicação, porém, para rodá-la basta clonar o repositório [ Repositório do TCC](https://github.com/beatrizmanaia26/TCC-DesempenhoEnem) abrir 2 terminais:
1- cd aplicacao, cd MVP, cd frontend e rodar "npm run dev"
3- cd aplicacao, cd MVP, cd backend e rodar "npm run dev"

<!--
**Protótipo:** {{URL}}  
**Arquivo editável:** {{URL}}  
**Última verificação de permissão:** {{dd/mm/aaaa}} -->

> Teste o link em janela anônima. O avaliador deve conseguir abrir o protótipo sem solicitar permissão.

## Cobertura MoLIC → Figma

| MoLIC | Objetivo | Fluxo/telas no Figma | Estados de erro/recuperação | Responsável |
|---|---|---|---|---|
| M01 | O01 | `F01 → F02 → F03` | `F02E, F03R` | {{...}} |
| M02 | O01 | `F01 → F02 → F03` | `F02E, F03R` | {{...}} |
| M03 | O01 | `F01 → F02 → F03` | `F02E, F03R` | {{...}} |

## Catálogo de telas/estados

### F01 — Tela principal 

![F01](../assets/11_figma/f01.jpeg)

**Objetivo do usuário:** Anexar um arquivo na tela<br> 
**Signos principais:** Prova, Área tracejada, ícone de upload (seta), texto instrucional, texto de restrição, botão "Escolher arquivo"<br> 
**Origem no MoLIC:** M02/Enviar avaliação  <br> 

### F02 — Arquivo no formato válido enviado (fluxo feliz)

![F02](../assets/11_figma/f02.jpeg)

**Objetivo do usuário:** Trocar a prova anexada <br> 
**Signos principais:** Informações do arquivo (nome e tamanho), botão "cancelar" <br> 
**Origem no MoLIC:** M02/Carregar arquivo <br> 

### F03 — Arquivo com formato inválido

![F03](../assets/11_figma/f03.jpeg)

**Objetivo do usuário:** Enviar arquivo em formato válido  <br> 
**Signos principais:** Erro1: Formato inválido  <br> 
**Origem no MoLIC:** M02/cena de erro<br> 


### F04 — Erro ao extrir questões do PDF

![F04](../assets/11_figma/f04.jpeg)

**Objetivo do usuário:** Enviar arquivo no qual questões consigam ser dientificadas <br> 
**Signos principais:** Erro2: Erro ao preparar a análise <br> 
**Origem no MoLIC:** M02/cena de erro<br> 


### F05 — Tamanho do arquivo excede limite 

![F05](../assets/11_figma/f05.jpeg)

**Objetivo do usuário:** Enviar um arquivo dentro das limitações específicas para seguir o fluxo feliz de analisar sua avaliação <br> 
**Signos principais:** Erro3: Arquivo excede tamanho <br> 
**Origem no MoLIC:** M02/cena de erro<br> 

### F06 — Erro interno

![F06](../assets/11_figma/f06.jpeg)

**Objetivo do usuário:** Conseguir prosseguir para a tela de informar os dados de sua prova <br> 
**Signos principais:** Erro4: Server Error <br> 
**Origem no MoLIC:** M02/cena de erro<br> 

> Documente também estados que muitas equipes esquecem: carregamento, vazio, confirmação, sucesso, erro, permissão negada, cancelamento, desfazer/voltar quando aplicável.


### F0x —   xxxxxx 

![F0xx](../assets/11_figma/f06.jpeg)

**Objetivo do usuário:** <br> 
**Signos principais:**  <br> 
**Origem no MoLIC:** <br> 


<!--NAO SEI se dividi os topicos corretamente --> 


## Sistema visual e consistência

| Elemento | Regra adotada | Justificativa |
|---|---|---|
| Tipografia | {{...}} | {{legibilidade/contexto}} |
| Cores | {{...}} | {{hierarquia/contraste/semântica}} |
| Componentes | {{...}} | {{consistência}} |
| Feedback | {{...}} | {{status}} |

## Verificação de acessibilidade básica

Para produto Web, considere critérios pertinentes da WCAG vigente (por exemplo, contraste, foco, tamanho de alvo, texto alternativo e navegação por teclado quando aplicáveis). Para outras plataformas, use as recomendações adequadas ao contexto.

## Checklist

- [ ] Link do Figma está acessível.
- [ ] Há screenshots representativos no repositório.
- [ ] Todos os MoLIC relevantes estão cobertos.
- [ ] Estados de erro, feedback e recuperação foram prototipados.
- [ ] Terminologia/signos são consistentes com Entrega 9.
- [ ] Componentes equivalentes se comportam de forma consistente.
- [ ] Fluxos críticos são clicáveis do início ao fim.
- [ ] O protótipo está pronto para inspeção e testes, sem “links mortos” nas tarefas avaliadas.
- [ ] Dashboards, relatórios, históricos, filtros, administração e CRUDs presentes possuem justificativa rastreável.
- [ ] Estados de vazio, processamento, erro e recuperação foram considerados quando pertinentes.
- [ ] Resultados técnicos são apresentados de forma interpretável para o perfil de usuário.
- [ ] A equipe distingue no protótipo o que é interação simulada e o que é funcionalidade técnica realmente integrada, quando necessário.
