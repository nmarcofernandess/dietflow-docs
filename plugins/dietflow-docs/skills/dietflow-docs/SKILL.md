---
name: dietflow-docs
description: "Cria, atualiza, consolida ou recenseia documentação técnica do DietFlow para desenvolvedores. Use para arquitetura, código, dados, contratos, fluxos internos e READMEs; para ensinar uso ao nutricionista use user-docs, e operação administrativa use admin-docs."
---

# Documentação técnica do DietFlow

Você escreve para quem precisa entender, reproduzir e manter o sistema. Comece explicando o problema e o resultado; conduza do domínio à arquitetura e ao detalhe necessário. Preserve a voz fluida e causal, sem inventário de componentes desconectado do porquê.

Leia as [receitas técnicas](../../assets/playbooks/documentacao-tecnica.md). Escolha as pertinentes: orientar, comparar famílias, localizar e conectar código, seguir ação até persistência, acompanhar exemplo, ensinar extensão/recuperação e declarar disponibilidade. Use árvores por responsabilidade e mapas de front/domínio/dados apenas quando responderem uma dúvida. As fontes e âncoras reais do checkout sustentam claims; não copie exemplos históricos como comportamento vigente.

Docs canônicas ficam no owner documental do projeto; README explica seu pacote; `.context` conserva os contratos no formato adotado. SPEC/PLAN seguem o método atual, sem impor pasta ignorada. Consolidação atualiza os índices e consumidores dos links antes de retirar o que foi absorvido. Não transformar uma doc canônica em diário de campanha.

## Como trabalhar

Identifique o checkout consumidor, leia suas instruções e localize os owners pelo [mapa de fontes](../../assets/references/fontes-dietflow.md). Receitas do pacote ensinam a forma; código e contratos vivos determinam os fatos. Não é necessário ler documentos exemplares externos para aprender a escrever.

Do pedido e contexto, resolva criar, atualizar, consolidar ou recensear. Examine o delta integral pertinente, preserve WIP alheio e siga owners/consumidores; use [censo e impacto](../../assets/playbooks/censo-e-impacto.md) quando houver mudança ou recenso. Um match não prova cobertura, e contagem não demonstra frescor. Não crie um registro novo se o existente basta.

Escreva com propósito antes do mecanismo, prosa que conecta causa e efeito, vocabulário concreto, exemplos verificáveis e limites que mudem a compreensão. Confirme labels, números, fórmulas, APIs e comandos que citar. Diferencie intenção, implementação, observação e aceite humano. Pergunte somente por informação material que não puder recuperar; não reabra público já definido pela skill ou destino.

Para gráficos, carregue [receitas Mermaid](../../assets/playbooks/diagramas-mermaid.md). Escolha pela pergunta: mapa conceitual, fluxo de tarefa, camadas, ER, requisitos/evidência, sequence opcional e state opcional. Árvore de arquivos usa texto com responsabilidades. Não obrigue todo gráfico em toda doc nem converta PlantUML globalmente. Compatibilidade de sintaxe, renderização e legibilidade são verificações distintas.

Se houver ajuda contextual, carregue [extensão e diagnóstico](../../assets/playbooks/ajuda-contextual.md); autoria sozinha não autoriza implementar UI. Leia a composição e gramática dos renderizadores do checkout antes de ensinar ou alterar seu uso. Não invente wrappers, publicador, permissão, fonte de conteúdo ou gate paralelo.

Confira conteúdo, navegação e referências no menor nível adequado. Não suba stack ou rode CI amplo só para confirmar texto ou links. Alterações de comportamento e publicação seguem autorização, método e gates do consumidor. Relate o que foi criado/alterado, examinado sem mudança e não comprovado; diferencie arquivo local, commit, publicação, instalação e observação.
