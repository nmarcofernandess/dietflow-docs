# Encontrar a verdade no checkout consumidor

O plugin contém a receita editorial; o projeto contém seus contratos e comportamento. Resolva os caminhos abaixo no checkout do DietFlow em que está trabalhando. Não os resolva contra o diretório instalado do plugin. Leia AGENTS.md antes de editar. Use docs/README.md e .context/domains/manifest.yaml para localizar o owner pertinente e siga só as dependências que mudam a resposta.

| Pergunta | Entradas relativas ao checkout |
|---|---|
| Doc técnica e localização de owners | docs/README.md, .context/domains/manifest.yaml e README do módulo/lib |
| Organização de docs por público | docs/documentacao/README.md |
| Coleções compiladas e geração | source.config.ts, package.json, src/lib/docs/source.ts |
| Site, navegação e componentes MDX | src/app/(docs)/, content/docs/meta.json, metas ancestrais, src/components/docs/ |
| Quick, guia e drawer | docs/module-help/SISTEMA-AJUDA-CONTEXTUAL-DRAWER.md, src/components/features/module-help/README.md e implementação |
| Módulo com ajuda | src/lib/constants/modules-config.ts e consumidores de ModuleHelpButton/ModuleHelpDrawer |
| Estrutura executável da ajuda | scripts/check-module-help-docs.ts e comando declarado em package.json |
| Público admin e permissões | manifest, src/lib/auth/role.ts, permission-helpers.ts e owner da operação, sem confundir leitura com escrita |
| SPEC/PLAN e entrega | Contrato atual do método/pacote e instruções do projeto; não impor pasta local ignorada |
| Publicação e integração | Instruções e owners CI atuais do consumidor; não embutir uma receita paralela de push/deploy |

Para MDX, conferir coleção, loader, navegação, links, gramática e autorização reais. O quick pode ser usado por dois renderizadores: não presumir paridade de componentes. Ler a configuração efetiva antes de afirmar que admin tem destino protegido ou Mermaid renderiza. Censo histórico, nome de pasta, sidebar oculta e dependência instalada não demonstram essas capacidades.

Os paths são entradas de descoberta, não garantia de presença eterna. Se uma referência faltar, procure o owner pelo índice/manifest do projeto e siga seus consumidores pertinentes. Registre a divergência e corrija este mapa quando a manutenção do pacote estiver no pedido. Não recrie um componente nem escolha destino de publicação inseguro por fallback silencioso. Pare a leitura quando souber contrato, consumidores e verificação da mudança.

O repositório do plugin é público. Inclua somente receitas e exemplos fictícios, sem dados pessoais, credenciais, configuração privada, dumps ou arquivos internos copiados por rotina. Artefatos técnicos do consumidor conservam seus próprios destinos e regras de acesso.
