# Adicionar ou diagnosticar ajuda contextual

Use este playbook quando o pedido envolver o vínculo entre conteúdo e superfície. Autoria de texto não concede autorização para implementar UI. Quando o pedido incluir implementação, siga os patterns e o método do projeto.

## Extensão autorizada

1. Identifique propósito da página, público e owner. Leia o contrato atual da família de ajuda e seus consumidores.
2. Localize a coleção e o padrão de quick/guia/meta. Prepare conteúdo verdadeiro e a navegação local/ancestral antes de declarar um destino de ajuda.
3. No DietFlow, uma superfície pode receber ajuda pela configuração de MainGenericEditor (MGE, shell de editor) ou por ModuleHelpButton em uma superfície independente. Confira o mecanismo, props e posições atuais no owner; não copie API congelada deste exemplo.
4. Preserve um conteúdo quick compartilhado entre site e drawer e a interseção real de sua gramática. Leia os dois mapas e o gate. Não crie uma cópia em TypeScript nem reconstrua o shell.
5. Confira slug, arquivos, metas, links e efeito do comando existente mais restrito que observa a propriedade. Conteúdo e aparência exigem evidências diferentes; inspecione renderização representativa se alterar composição.

Exemplo fictício: uma página de Propostas passa a ter ajuda. O pacote editorial prepara quick/guia e entrada de navegação. Uma tarefa que também autorize implementação conecta o trigger ao slug pelo shell já usado pela página. O resultado esperado é ler o mesmo quick no drawer e no site e abrir o aprofundamento correto, sem cópia paralela. Esse exemplo não declara a existência de Propostas no DietFlow.

## Diagnóstico finito

Identifique ambiente, checkout e slug antes de editar. Distinga: arquivo/geração ausente; construção incompatível com o mapa do drawer; link/meta incorreto; ou falha de carregamento do chunk. Leia o ponto que falhou e o consumidor real. O gate estrutural não prova conteúdo clínico, navegação inteira ou fidelidade visual.

No owner atual de ajuda, confira a boundary local, diagnóstico com docPath, retry do loader e link para o guia antes de presumir que o texto está ausente. Repetir rede ou mexer no MDX sem causa confirmada pode esconder o erro. Registre ação, resultado e limite no relato existente. Não crie telemetria, harness ou fallback novo por rotina.
