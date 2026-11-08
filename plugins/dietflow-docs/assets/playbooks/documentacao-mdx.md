# Receitas de documentação MDX por público

Exemplos fictícios de um sistema de propostas, não labels ou funcionalidades do DietFlow. Ao aplicar, leia os contratos do checkout e use seus componentes, navegação e linguagem reais.

## Entrada rápida: entender e começar

Entrada necessária: finalidade, primeira ação, ponto de entrada, resultado e limite essencial confirmados. Abra com o conceito em linguagem do operador, dê um primeiro percurso curto e conecte ao guia. Um quick compartilhado deve funcionar com a gramática comum aos seus dois consumidores. Não incluir explicação de hooks, schema ou APIs na prosa de usuário.

**Exemplo:** “Propostas reúne os valores que você prepara para enviar a um cliente. Abra Propostas, escolha Criar, informe o destinatário e adicione os itens. Salvar conserva seu rascunho; Enviar exige uma confirmação e cria a versão que o cliente receberá. Ajustes posteriores não alteram essa versão. Veja no guia como corrigir e reenviar.”

Conferir labels, efeito de cada ação, persistência e o link de aprofundamento. Não afirmar que o exemplo fictício está disponível no produto.

## Guia completo: dominar as escolhas

Entrada necessária: quick, conceitos, decisões e estados que afetam o trabalho. Explique por que cada opção existe, organize campos por tarefa e trate ausências, erros, correção e continuidade. O guia aprofunda o quick; não precisa repetir seu percurso inteiro.

**Exemplo:** “Rascunho é a oferta em preparação; versão enviada é o retrato confirmado no envio. Confira o destinatário antes de enviar porque ele pertence à versão que ficará no histórico. Para corrigir um preço, altere o rascunho e confirme um novo envio. O histórico permite comparar as duas versões.”

Conferir que as escolhas e a recuperação têm caminho real. Imagens e componentes avançados só entram quando o renderizador do destino os suportar.

## Jornada: resolver uma tarefa

Entrada necessária: situação inicial, objetivo concreto e resultado. Nomeie a jornada pelo objetivo; mantenha o percurso centrado na tarefa. Linke conceitos ou opções raras ao guia, evitando uma terceira cópia completa dele.

**Exemplo:** “Para corrigir uma proposta enviada, abra a proposta e consulte a versão no histórico. Edite o rascunho, confira os valores e envie novamente. Ao terminar, confira se a nova versão aparece no histórico; a anterior permanece disponível.”

Conferir pré-condições, permissão, resultado observável e falhas pertinentes. Uma jornada que atravessa módulos pode precisar atualizar referências de ambos.

## Operação administrativa: conceito, alcance e recuperação

Entrada necessária: responsabilidade da área, identidade do operador, permissão da ação, alcance da mudança, confirmação, efeito durável e recuperação possível. O público já é administrativo; não perguntar isso novamente. Permissão de ler um manual não concede permissão de executar as operações documentadas.

**Exemplo:** “O catálogo central oferece modelos para novas propostas. Somente operadores com permissão de manter o catálogo podem arquivar um modelo. Arquivar impede sua seleção em novas propostas e preserva as versões já enviadas. Antes de confirmar, confira qual modelo será afetado. Se precisar disponibilizá-lo novamente, use Restaurar.”

Esse exemplo é fictício e não estabelece política do DietFlow. Conferir o owner real das permissões, o efeito em leitores e a existência da restauração antes de escrever.

## A mesma operação em três públicos

| Público | Explicação fictícia |
|---|---|
| Desenvolvimento | O comando autentica o writer, valida a revisão recebida e persiste uma versão; o reader do histórico não recalcula essa versão |
| Usuário | Confira os dados e confirme o envio; o histórico preserva o que foi enviado mesmo se você editar o rascunho depois |
| Admin | Alterar o catálogo afeta novos usos; versões já enviadas conservam seu conteúdo. A operação exige a permissão administrativa pertinente |

## Destino e composição

Leia coleção, loader, rota e meta.json reais antes de escrever. Preserve o par quick/guia e sua navegação quando o módulo tiver ajuda contextual. Confira links locais e ancestrais. Se o destino for reservado e não houver capacidade protegida demonstrada, escreva somente no rascunho da entrega fora de coleções compiladas e assets públicos. Não mude código de rota ou autorização em nome de uma tarefa apenas editorial.

Autoria cria conteúdo; publicação depende da capacidade e da autorização do destino. O plugin deve declarar exatamente o que ficou como rascunho. Arquivo fora da coleção não é proteção do Git: não inserir segredos nem dados pessoais reais.
