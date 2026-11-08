# Receitas de documentação técnica

Receitas autocontidas para ensinar a escrever. Os exemplos abaixo são didáticos e fictícios; ao aplicar, substituir pelos dados e contratos reais da entrega.

## Escolher a receita

Uma documentação de visão geral precisa orientar; uma explicação arquitetural precisa mostrar responsabilidades; uma rotina operacional precisa permitir agir e recuperar. Use as receitas pertinentes ao pedido. Elas podem compor uma mesma página, sem obrigar todas as seções ou todos os gráficos em todo documento.

## 1. Orientar quem chegou agora

**Quando:** apresentar um domínio, sistema ou capacidade.

Abra com o problema concreto, quem o enfrenta, o que entra e qual resultado sai. Depois explique o princípio organizador. Só então apresente os nomes técnicos necessários. Em documentos longos, dê um roteiro navegável; estime leitura sem prometer precisão artificial.

**Exemplo de abertura:** “O módulo de propostas guarda o trabalho em preparação e a versão que já foi enviada. Assim, ajustar um preço permite preparar uma nova oferta sem alterar o que o cliente recebeu. O sistema organiza isso em rascunho, versão enviada e histórico.”

**Conferir:** alguém consegue explicar a finalidade antes de conhecer classes, hooks ou tabelas? O roteiro acompanha a ordem das dependências conceituais?

## 2. Explicar famílias e escolhas

**Quando:** existem soluções próximas, variantes ou owners que parecem redundantes.

Apresente a diferença de semântica antes da diferença de componentes. Compare pelas mesmas dimensões: dono, persistência, ciclo de vida, operação e consumidor. Explique por que uma composição compartilhada resolve parte da necessidade e onde as variantes precisam divergir. Termine com critérios observáveis de escolha.

| Pergunta | Família A | Família B |
|---|---|---|
| Qual é a unidade de trabalho? | Documento de uma pessoa | Modelo reutilizável |
| O que uma edição modifica? | O registro aberto | O modelo para novos usos |
| Como se relacionam? | Recebe uma cópia explícita | Oferece a origem dessa cópia |

**Conferir:** a tabela compara propriedades equivalentes? As justificativas estão verificadas ou claramente apresentadas como inferência? O leitor sabe escolher sem decorar nomes de componentes?

## 3. Localizar e conectar o código

**Quando:** o leitor precisa encontrar implementação e compreender camadas.

Mostre uma árvore curta com responsabilidade por caminho. Depois explique os owners e as dependências entre eles num mapa separado, se essa relação não estiver clara na prosa. Uma seta precisa significar uma coisa: chamada, dado, composição ou dependência. Não misture todos esses sentidos sem rótulo.

```text
src/propostas/
├── PropostaMain.tsx    # compõe a superfície
├── useProposta.ts      # integra comandos e estado de edição
├── actions.ts          # autentica, valida e persiste
└── repository.ts       # executa consultas e escrita
```

Essa árvore é fictícia. Uma árvore real não deve inventar simetria entre módulos. No mapa, identifique limites client/server, autorização e persistência quando existirem. Não coloque todas as regras no frontend apenas porque a explicação começa na tela.

**Conferir:** cada caminho existe? A responsabilidade corresponde ao símbolo lido? A ordem do desenho representa uma dependência real? Leitura, escrita e projeção têm owners identificáveis?

## 4. Seguir uma ação até seu resultado

**Quando:** documentar jornada ou operação que atravessa camadas.

Escolha um caso concreto: situação inicial → ação → validação → transformação → escrita → releitura → resultado. Inclua o caminho de falha que muda a compreensão do leitor. Use sequência somente se atores, chamadas e ordem forem a dúvida; para escolhas de processo, prefira fluxo de decisões.

**Exemplo didático:** editar o preço muda o rascunho; confirmar o envio cria uma versão; reabrir mostra o preço enviado e preserva o rascunho posterior separadamente. A documentação deve deixar claro em que ação o dado passa a ser durável e o que o leitor recebe ao reabrir.

**Conferir:** ação, efeito e persistência estão distinguidos? O diagrama preserva quem autentica, quem grava e quem lê? Uma projeção na tela não foi descrita como dado já salvo?

## 5. Acompanhar um exemplo verificável

**Quando:** explicar regra, cálculo, transformação ou derivação.

Declare entradas, unidades e premissas; mostre cada transformação e o resultado. Continue com o mesmo caso até o consumidor final. Para regras não numéricas, acompanhe um identificador e suas mudanças em vez de fabricar números.

```text
Quantidade: 3 unidades
Preço unitário: R$ 20,00
Subtotal: 3 × 20 = R$ 60,00
Desconto confirmado: R$ 5,00
Total da versão enviada: R$ 55,00
```

**Conferir:** as contas fecham? Arredondamento e ausência seguem o contrato real? O exemplo usa dados suficientes e não depende de um valor omitido? Conferir a regra no código é distinto de validar sua adequação científica ou comercial.

## 6. Ensinar a extensão e a recuperação

**Quando:** orientar adição de uma variante, integração, componente ou operação.

Dê pré-condições, owner a alterar, menor exemplo completo, consumidores a reconciliar e condição observável de término. Mostre uma variação legítima quando ela muda a estratégia. Para recuperação, descreva sinal, causa confirmada ou hipótese, ação segura e resultado esperado; não transforme um incidente histórico em procedimento universal.

**Exemplo fictício:** “Para adicionar um formato de proposta, declare sua identidade no catálogo de formatos, implemente a conversão no owner da exportação e atualize os leitores que exibem a versão enviada. Confirme que uma proposta existente continua legível. Se a conversão falhar, preserve a versão anterior e informe qual formato falhou; repetir o envio só faz sentido depois de corrigir a causa.” A localização e a API concretas devem ser preenchidas com o código real do tema.

**Conferir:** quem seguir a receita entrega comportamento completo, incluindo leitores e persistência pertinentes? Exemplos de código são compatíveis com o contrato vigente? Nenhum exemplo antigo concede autorização de deploy, banco ou integração por si.

## 7. Explicitar disponibilidade e aprofundamento

**Quando:** há comportamento parcial, proposta aprovada sem implementação ou evidência limitada.

Descreva a capacidade disponível e o limite que afeta o uso. Distinga contrato planejado, código presente, comportamento observado e aceite humano. Direcione o leitor ao owner pertinente para aprofundar. Não transporte cronologia de tentativas ou status de campanha para a doc canônica.

**Exemplo fictício:** “O envio por e-mail está disponível. O envio por mensagem foi desenhado, mas ainda não tem implementação; por isso esta página ensina apenas e-mail. A confirmação registra que a solicitação foi recebida, sem comprovar que o destinatário abriu a mensagem.”

**Conferir:** a página informa uma limitação relevante sem parecer que toda a funcionalidade está entregue? As referências complementam o texto em vez de substituí-lo? Números, paths e APIs são conferidos no checkout atual.

## Aplicação por público

Estas receitas descrevem a escrita técnica. Em documentação de usuário, traduza mecanismo em conceito, tarefa, resultado e limite com labels de tela; em admin, acrescente responsabilidade, alcance da ação, permissão e recuperação. As receitas editoriais podem ser compartilhadas; árvores de implementação, nomes de banco e diagramas internos não são automaticamente conteúdo para o usuário.
