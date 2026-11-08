# Selecionar páginas a partir da mudança

## Receber o recorte

Identifique o checkout e o pedido antes da busca. Se o usuário indicar um tema sem delta Git, trate como investigação daquele comportamento. Se pedir mudanças locais, examine o delta relevante staged, unstaged e arquivos novos pertinentes; preserve WIP alheio. Se indicar uma branch, PR ou entrega, use o recorte completo contra a base pertinente, não apenas o último commit. Registre o que foi comparado. Não incorpore mudanças por Git nem altere arquivos alheios só para fazer um censo.

## Seguir o comportamento

Se o funcionamento do módulo ainda não estiver explicado pelas fontes lidas, use [descoberta do módulo](descoberta-do-modulo.md) antes de decidir o conteúdo das páginas. Esta receita seleciona o impacto documental; a descoberta reconstrói o comportamento que será explicado.

Mapeie promessa, owner, writers/readers e consumidores afetados. Localize quick, guia, jornadas, referências e documentação técnica que expliquem esse comportamento. Confira arquivos, índices, slugs e links. Nomes e matches selecionam candidatos, mas não provam cobertura; siga dependências que mudem a resposta e pare quando o alcance estiver explicado.

## Registrar a conclusão

Distinga páginas examinadas sem necessidade de edição, páginas que precisam mudar, páginas atualizadas e dúvida material com informação faltante. “Não encontrado” informa alcance da busca, não ausência absoluta. Censo estrutural, correção semântica e comportamento observado são evidências diferentes.

**Exemplo fictício:** uma mudança no comando Enviar altera confirmação e cria um estado de falha recuperável. Candidatos: quick de Propostas, guia de envio e jornada de correção. Após ler, o quick requer nova frase sobre a confirmação; o guia explica o erro e a retomada; a jornada permanece correta. Registre essa seleção sem reescrever a jornada nem declarar toda a coleção auditada.

## Fonte viva prevalece

O pacote ensina o procedimento e aponta entradas relativas do projeto. APIs, permissões, gramática e paths vêm do checkout atual. Se um ponteiro do plugin estiver ausente, localize o owner pelos índices do projeto e confirme seus consumidores. Corrija o mapa do pacote quando ele estiver sob sua responsabilidade; caso contrário, registre a referência quebrada e a fonte encontrada. Não recrie um componente ou publique conteúdo em outro universo por fallback silencioso.
