# Descobrir o módulo e transformar os achados em documentação

Use esta receita quando o pedido exigir entender como um módulo funciona para documentá-lo, mesmo sem documentação anterior ou delta Git. Ela é compartilhada pelas três skills: a investigação encontra os fatos; a skill selecionada determina o leitor, a linguagem e o destino. Não depende de agentes registrados, relatórios antigos ou acesso ao banco.

## Encontrar o módulo real

Parta do objetivo do leitor e do recorte pedido. Pelo [mapa de fontes](../references/fontes-dietflow.md), localize contrato, configuração, entrada de UI ou API, README do owner e documentação existente. Confira o caminho usado pelo consumidor; não presuma que todo módulo fica em `clinical/`, possui um `Main` ou segue a mesma estrutura de pastas.

Leia a entrada e a composição pertinente para entender o que é oferecido, a quem, em quais contextos e com quais dados. Siga os componentes, hooks, actions, serviços, repositories e readers que explicam esse comportamento. Nome de arquivo ajuda a localizar; presença de um componente ou action não comprova acesso, disponibilidade nem uso pelo consumidor.

Se já houver descoberta ou documentação, reutilize os fatos ainda compatíveis com o checkout atual e investigue as lacunas e mudanças. Um pedido focal não exige redescobrir o módulo inteiro. Ao documentar o módulo inteiro, cubra suas capacidades distintas, sem reduzir a descoberta à primeira tela encontrada.

## Reconstruir uso, regras e efeitos

Para cada capacidade relevante, conecte a intenção do usuário ao resultado. Investigue as questões que mudam a explicação:

- **Entrada e disponibilidade:** como acessar, labels reais, contexto necessário, variante da tela, flags e permissões que afetam o acesso. Uma ação existente no backend pode ser interna ou não estar exposta nesse contexto.
- **Caminho principal:** o que a pessoa vê, informa, escolhe e confirma; valores iniciais, critérios de seleção e resultado esperado. Diferencie estados vazios, itens existentes e modos de edição, quando alterarem a tarefa.
- **Regras e estados:** validações, limites, cálculos, transições e erros recuperáveis pertinentes. Siga o lifecycle da entidade em vez de deduzir uma regra apenas pelo botão ou pelo nome de um campo.
- **Dados e efeitos duráveis:** de onde vêm os dados e onde são escritos/lidos; o que salva, cancela, arquiva, oculta, publica ou remove de fato. Separe estado local, persistência e atualização das outras superfícies. Confira snapshot/referência, visibilidade e autoria quando afetarem o comportamento.
- **Integrações e recuperação:** o que vem de outros módulos, o que passa a ficar disponível para eles, efeitos sobre exportação/Care ou outros consumidores reais, falhas e retomadas implementadas. Documente somente as integrações pertinentes ao recorte.

Não trate todas as actions como comandos disponíveis ao leitor nem todos os campos do schema como recursos da interface. Para operação administrativa, confira separadamente autorização de leitura e escrita, alcance sobre registros/usuários e possibilidade real de recuperação. Para documentação técnica, preserve também as responsabilidades e contratos internos que explicam essas decisões.

## Explicar como funciona e por que tem essa forma

**Como:** escolha um caso representativo do recorte e percorra o caminho inteiro: gatilho, entrada, decisões, transformações, writer, reader e resultado para os consumidores pertinentes. Use valores fictícios compatíveis com os tipos e regras lidos, identificando-os como exemplo. Em cada passagem, mostre qual responsabilidade muda de owner, que dados atravessam a fronteira e onde ocorre a decisão; inclua falha ou cancelamento quando mudarem o resultado. Se uma etapa não existir, não a acrescente para completar o roteiro.

Reconstrua um modelo mental com os conceitos necessários, o fluxo central e onde ficam suas responsabilidades. Explique os pontos surpreendentes que mudam a compreensão; não transforme a narrativa em comentário de cada linha do código. Use uma árvore curta para localização e as receitas Mermaid para relações ou transformações que fiquem mais claras visualmente. Ao reunir achados sobre partes distintas, resolva sobreposições e contradições na fonte antes de redigir uma explicação única.

**Por quê:** diferencie a consequência verificável do mecanismo e a motivação de quem o escolheu. O código pode demonstrar que uma confirmação antecede uma gravação; isso não comprova por que essa confirmação foi introduzida, por que um limite tem certo valor ou quais alternativas foram consideradas.

Quando a justificativa for relevante para o pedido e ainda não estiver sustentada, parta dos arquivos e símbolos encontrados. Consulte o contrato e os comentários pertinentes; use o histórico do trecho para localizar a mudança de origem, seguindo renames quando necessário, e leia o PR, issue ou decisão vinculada. O último commit que tocou o arquivo pode não conter a decisão original. Fontes externas só entram quando houver relação concreta com a dúvida e acesso permitido; não é necessário pesquisar toda ferramenta conectada para escrever uma doc.

Calibre a conclusão conforme a evidência:

| Evidência encontrada | Como tratar na documentação |
|---|---|
| Justificativa explícita em contrato, comentário, decisão ou discussão atribuível | Explique o motivo com referência à fonte e preserve seu alcance. Confira se ainda é compatível com o comportamento atual. |
| Indícios que sustentam uma interpretação, sem declaração explícita | Identifique a inferência e a relação entre os indícios. Não a atribua ao autor ou à equipe como decisão confirmada. |
| Motivos concorrentes ou fontes contraditórias | Preserve a divergência relevante e identifique o que a resolveria; não escolha o relato mais conveniente para uma explicação elegante. |
| Nenhuma justificativa encontrada no recorte pesquisado | Declare que o motivo não foi determinado, com as fontes consultadas, e documente o funcionamento que conseguiu comprovar. |

Uma hipótese sugerida pelo usuário é uma pista a verificar. Cópias de uma mesma interpretação não são evidências independentes; ao afirmar uma decisão humana, procure sua fonte atribuível e não amplie uma orientação temporária para uma regra permanente. Não justifique retrospectivamente uma implementação só porque ela parece razoável hoje.

Na documentação técnica, razões, alternativas e limites sustentados ajudam a manter o módulo. Nas docs de usuário e admin, explique as consequências práticas comprovadas para a tarefa; mantenha hipóteses de implementação nas notas da investigação, sem apresentá-las como orientação ao operador. Essa distinção regula a precisão da prosa, sem impor rótulos de confiança ou seções de investigação a cada página.

## Sustentar a explicação

Associe os achados importantes aos arquivos e símbolos que os sustentam. Distinga comportamento lido no código, intenção de contrato, observação em execução e dúvida ainda não determinada. Specs e comentários ajudam a interpretar; uma implementação ausente não vira capacidade entregue porque está planejada.

A descoberta normalmente cabe nas notas da execução existente. Se for útil para continuidade ou para várias páginas, registre um resumo no destino de pesquisa já adotado pelo consumidor; use `content/research/<modulo>/discovery.md` somente se essa convenção estiver presente e o conteúdo puder ficar ali. Não crie relatório, pasta ou template obrigatório para toda edição. Preserve achados reservados fora das coleções e assets públicos.

Um resumo reutilizável contém propósito, caminhos de uso, regras/estados, dados/integrações, fontes e limites pertinentes. Ele precisa permitir explicar a tarefa e seu resultado sem inventar o que não foi encontrado. Busca sem resultado deve informar seu alcance; não prova ausência absoluta. Se uma dúvida material impedir ensinar a operação corretamente, delimite o que falta e continue a parte sustentada.

Encerre a investigação quando conseguir descrever as capacidades do recorte, suas condições e consequências, apontando seus owners. Execute uma verificação focal somente quando necessária para resolver uma dúvida que a leitura não responde; não suba uma stack por rotina nem anuncie execução que não ocorreu.

## Escrever para o leitor da skill

Transforme os achados em conteúdo útil, em vez de publicar o relatório de investigação como manual:

| Entrada | O que produzir com a descoberta |
|---|---|
| `dietflow-docs` | Propósito, arquitetura, responsabilidades, contratos, caminho de leitura/escrita, lifecycle, extensão e recuperação. Use fontes e símbolos reais; escolha árvores, camadas ou outros diagramas pelas relações encontradas. |
| `user-docs` | Conceito, acesso, tarefa, escolhas, resultado, limites e retomada em linguagem de nutricionista. O quick permite começar; o guia aprofunda as decisões. Internals usados para verificar os fatos não entram como jargão no manual. |
| `admin-docs` | Conceito da operação, responsabilidade, escopo, permissão, confirmação, efeitos e recuperação. Use somente destino protegido comprovado ou o rascunho previsto na skill; descobrir uma função administrativa não autoriza publicá-la na ajuda de usuário. |

Use as receitas técnicas ou MDX da skill para compor as páginas. Quando já houver conteúdo, aplique também [censo e impacto](censo-e-impacto.md) para selecionar quick, guia, jornadas, referências e índices que precisam mudar. A escolha entre criar e atualizar vem do conteúdo encontrado, sem exigir que o usuário decida o número de páginas ou confirme novamente o público.

**Exemplo fictício:** no módulo Propostas, a tela mostra “Salvar rascunho” e “Enviar”. A leitura revela que salvar persiste uma proposta ainda não publicada; enviar exige uma confirmação e um writer autorizado, e outro reader decide o que o destinatário recebe. A doc de usuário ensina preparar, salvar e enviar; a técnica explica writer, autorização, transição e reader; a de admin descreve a intervenção administrativa somente se ela existir. Não conclua que salvar já enviou nem invente um comando de admin equivalente.

Ao terminar, confronte a prosa com os achados: acesso, sequência, labels, condições, resultado e recuperação precisam concordar. Confira navegação e referências afetadas. Relate a documentação entregue e os limites de evidência, sem apresentar a descoberta por leitura como validação funcional do produto.

## Referências de elaboração

Receita própria que reaproveita a distinção entre percurso de execução e motivação investigada de [Pstack how](https://github.com/michael-denyer/pstack-claude/blob/v0.9.133/plugins/pstack/skills/how/SKILL.md) e [Pstack why](https://github.com/michael-denyer/pstack-claude/blob/v0.9.133/plugins/pstack/skills/why/SKILL.md). O procedimento necessário está neste arquivo; não exige instalar Pstack, ler esses prompts, adotar seus modelos ou executar sua orquestração de agentes.
