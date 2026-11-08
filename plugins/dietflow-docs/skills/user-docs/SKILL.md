---
name: user-docs
description: "Cria, atualiza ou recenseia docs MDX de usuário do DietFlow para nutricionistas: início rápido, guia completo, jornadas, referências e ajuda contextual. Investiga o funcionamento do módulo no código antes de ensinar seu uso. Use quando o pedido ensinar o uso do produto ou atualizar páginas após mudança de módulo."
---

# Documentação de usuário do DietFlow

Seu público é o nutricionista que usa o produto. Não pergunte por esse público novamente. Explique conceito, tarefa, resultado e limites com os labels reais da tela, sem expor hooks, schema ou API na prosa. Para arquitetura técnica, use dietflow-docs.

Leia as [receitas MDX](../../assets/playbooks/documentacao-mdx.md). O quick orienta a primeira tarefa; o guia explica escolhas e aprofundamento; jornadas resolvem objetivos específicos; referências guardam fatos transversais. Se um módulo mudou, confronte essas entradas e os consumidores pertinentes. Não crie uma página para cada operação só para preencher estrutura.

Confira coleção, rota, metas locais/ancestrais e links. Preserve a fonte única do quick usado por site/drawer e a gramática comum dos dois renderizadores. Um componente aceito pelo guia não está automaticamente permitido no quick. Fenced Mermaid não comprova gráfico visual; use representação compatível com o destino e declare o limite quando pertinente. Não publique informação administrativa reservada na coleção de usuário.

## Como trabalhar

Identifique o checkout consumidor, leia suas instruções e localize os owners pelo [mapa de fontes](../../assets/references/fontes-dietflow.md). Receitas do pacote ensinam a forma; código e contratos vivos determinam os fatos. Não é necessário ler documentos exemplares externos para aprender a escrever.

Quando precisar entender um módulo para documentá-lo, siga [descoberta do módulo](../../assets/playbooks/descoberta-do-modulo.md): parta da entrada real, reconstrua uso, regras, estados, dados e integrações, e transforme os achados em documentação para o leitor desta skill. Siga um caso concreto e diferencie mecanismo comprovado de justificativa documentada, inferência ou motivo desconhecido. Isso também vale sem docs anteriores ou delta Git. Reaproveite descoberta compatível com o recorte; não dependa de um agente externo nem peça novamente o público.

Do pedido e contexto, resolva criar, atualizar, consolidar ou recensear. Examine o delta integral pertinente, preserve WIP alheio e siga owners/consumidores; use [censo e impacto](../../assets/playbooks/censo-e-impacto.md) quando houver mudança ou recenso. Um match não prova cobertura, e contagem não demonstra frescor. Não crie um registro novo se o existente basta.

Escreva com propósito antes do mecanismo, prosa que conecta causa e efeito, vocabulário concreto, exemplos verificáveis e limites que mudem a compreensão. Confirme labels, números, fórmulas, APIs e comandos que citar. Diferencie intenção, implementação, observação e aceite humano. Pergunte somente por informação material que não puder recuperar; não reabra público já definido pela skill ou destino.

Para gráficos, carregue [receitas Mermaid](../../assets/playbooks/diagramas-mermaid.md). Escolha pela pergunta: mapa conceitual, fluxo de tarefa, camadas, ER, requisitos/evidência, sequence opcional e state opcional. Árvore de arquivos usa texto com responsabilidades. Não obrigue todo gráfico em toda doc nem converta PlantUML globalmente. Compatibilidade de sintaxe, renderização e legibilidade são verificações distintas.

Se houver ajuda contextual, carregue [extensão e diagnóstico](../../assets/playbooks/ajuda-contextual.md); autoria sozinha não autoriza implementar UI. Leia a composição e gramática dos renderizadores do checkout antes de ensinar ou alterar seu uso. Não invente wrappers, publicador, permissão, fonte de conteúdo ou gate paralelo.

Confira conteúdo, navegação e referências no menor nível adequado. Não suba stack ou rode CI amplo só para confirmar texto ou links. Alterações de comportamento e publicação seguem autorização, método e gates do consumidor. Relate o que foi criado/alterado, examinado sem mudança e não comprovado; diferencie arquivo local, commit, publicação, instalação e observação.
