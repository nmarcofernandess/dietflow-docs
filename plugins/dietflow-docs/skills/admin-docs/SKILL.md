---
name: admin-docs
description: "Cria, atualiza ou recenseia documentação de operação administrativa do DietFlow: conceito da área, alcance, permissão, confirmação, efeitos e recuperação. Investiga o funcionamento e as permissões reais da operação antes de escrever. Publica apenas em destino administrativo protegido já comprovado; se faltar, produz rascunho fora das coleções compiladas."
---

# Documentação de administrador do DietFlow

Seu público é o operador administrativo, não o desenvolvedor nem o nutricionista em sua rotina clínica. Não pergunte pelo público já determinado. Explique o conceito da área, responsabilidade, alcance sobre dados/usuários, permissão real da ação, confirmação, efeito durável e recuperação disponível. Ler o manual não concede permissão de executar operações. Para arquitetura interna, use dietflow-docs.

Leia as [receitas MDX por público](../../assets/playbooks/documentacao-mdx.md). Reuse a régua editorial e a composição que o projeto já adota. Não copie internals técnicos nem presuma que o termo admin dá todas as permissões. Confira o owner da operação e de autorização.

## Destino administrativo

Antes de escrever numa coleção publicada, confira coleção/loader, rota, árvore, busca e artefatos client/mídia pertinentes. Sidebar oculta, path com nome admin ou sessão comum não demonstram segregação. A skill não implementa uma infraestrutura de autorização por efeito de um pedido editorial.

Se houver destino administrativo protegido demonstrado e autorizado para o pedido, use-o. Se faltar, escreva rascunho em `specs/<entrega>/rascunhos-admin/`, fora de coleções compiladas e assets públicos. Sem pasta de entrega, use `docs/rascunhos-admin/` somente após confirmar que não é fonte compilada/publicada. Se nenhum desses destinos estiver fora da publicação, informe o impedimento e preserve o conteúdo em scratch privado. Declare publicação pendente. Não adicione MDX reservado à coleção de usuário, não altere source.config, rota ou guard para contornar a ausência.

Mesmo fora da coleção, um arquivo pode ir ao Git; não escreva segredos, credenciais ou dados pessoais reais. O pacote do plugin também é público e contém somente exemplos fictícios e fontes de descoberta, sem material interno copiado indiscriminadamente.

## Como trabalhar

Identifique o checkout consumidor, leia suas instruções e localize os owners pelo [mapa de fontes](../../assets/references/fontes-dietflow.md). Receitas do pacote ensinam a forma; código e contratos vivos determinam os fatos. Não é necessário ler documentos exemplares externos para aprender a escrever.

Quando precisar entender um módulo para documentá-lo, siga [descoberta do módulo](../../assets/playbooks/descoberta-do-modulo.md): parta da entrada real, reconstrua uso, regras, estados, dados e integrações, e transforme os achados em documentação para o leitor desta skill. Isso também vale sem docs anteriores ou delta Git. Reaproveite descoberta compatível com o recorte; não dependa de um agente externo nem peça novamente o público.

Do pedido e contexto, resolva criar, atualizar, consolidar ou recensear. Examine o delta integral pertinente, preserve WIP alheio e siga owners/consumidores; use [censo e impacto](../../assets/playbooks/censo-e-impacto.md) quando houver mudança ou recenso. Um match não prova cobertura, e contagem não demonstra frescor. Não crie um registro novo se o existente basta.

Escreva com propósito antes do mecanismo, prosa que conecta causa e efeito, vocabulário concreto, exemplos verificáveis e limites que mudem a compreensão. Confirme labels, números, fórmulas, APIs e comandos que citar. Diferencie intenção, implementação, observação e aceite humano. Pergunte somente por informação material que não puder recuperar; não reabra público já definido pela skill ou destino.

Para gráficos, carregue [receitas Mermaid](../../assets/playbooks/diagramas-mermaid.md). Escolha pela pergunta: mapa conceitual, fluxo de tarefa, camadas, ER, requisitos/evidência, sequence opcional e state opcional. Árvore de arquivos usa texto com responsabilidades. Não obrigue todo gráfico em toda doc nem converta PlantUML globalmente. Compatibilidade de sintaxe, renderização e legibilidade são verificações distintas.

Se houver ajuda contextual, carregue [extensão e diagnóstico](../../assets/playbooks/ajuda-contextual.md); autoria sozinha não autoriza implementar UI. Leia a composição e gramática dos renderizadores do checkout antes de ensinar ou alterar seu uso. Não invente wrappers, publicador, permissão, fonte de conteúdo ou gate paralelo.

Confira conteúdo, navegação e referências no menor nível adequado. Não suba stack ou rode CI amplo só para confirmar texto ou links. Alterações de comportamento e publicação seguem autorização, método e gates do consumidor. Relate o que foi criado/alterado, examinado sem mudança e não comprovado; diferencie arquivo local, commit, publicação, instalação e observação.
