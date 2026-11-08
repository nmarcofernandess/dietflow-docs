# DietFlow Docs

Plugin público de documentação do DietFlow para Codex, Claude Code e Cursor. Três skills distinguem o leitor; cada uma cria, atualiza, consolida ou recenseia conforme o pedido. Não há servidor MCP, conexão ao banco ou código de execução do aplicativo.

| Skill | Público | Exemplo de pedido |
|---|---|---|
| dietflow-docs | Desenvolvimento | Explique a arquitetura de importação deste módulo |
| user-docs | Nutricionista | Atualize quick e guia desta mudança |
| admin-docs | Operador administrativo | Documente alcance e recuperação desta operação |

As receitas próprias ensinam prosa causal, árvores de arquivos, camadas, fluxos, exemplos rastreáveis e Mermaid. Os contratos e o código do checkout consumidor determinam os fatos. Pedidos mistos podem produzir páginas para vários públicos, reaproveitando leitura sem misturar destinos. Perguntas só quando o contexto não resolver uma ambiguidade material.

## Instalação

Use uma versão publicada. A primeira é v0.1.0.

### Codex

```sh
codex plugin marketplace add nmarcofernandess/dietflow-docs --ref v0.1.0
codex plugin add dietflow-docs@dietflow-docs
codex plugin list --marketplace dietflow-docs --json
```

Inicie uma sessão nova para conferir descoberta das três skills. Ao migrar de uma skill global com o mesmo nome, selecione explicitamente a entrada do plugin e só desative a antiga depois de conferir a candidata.

### Claude Code

```text
/plugin marketplace add nmarcofernandess/dietflow-docs
/plugin install dietflow-docs@dietflow-docs
```

A distribuição usa o marketplace Claude na raiz e o manifest do pacote. Confira a versão instalada pelo host; cadastro de uma origem Git não prova qual versão está em uso.

### Cursor

Adicione o repositório `https://github.com/nmarcofernandess/dietflow-docs` ao fluxo de marketplace/plugin do Cursor e instale DietFlow Docs. O repo contém `.cursor-plugin/marketplace.json` e o pacote contém `.cursor-plugin/plugin.json`, no mesmo layout do Superflow. Confira descoberta e versão no host; não há teste de execução Cursor implícito na existência desses arquivos.

### Outros hosts

As skills estão em `plugins/dietflow-docs/skills`; os assets relativos também precisam acompanhar a instalação. Um manifest portátil Agent Plugins 1.0 está em `plugins/dietflow-docs/plugin.json`. Não copie apenas SKILL.md: cada skill usa `../../assets/`. Compatibilidade efetiva depende do formato suportado pelo host.

## Receitas e autoridade

- [Receitas técnicas](plugins/dietflow-docs/assets/playbooks/documentacao-tecnica.md): propósito, famílias, código, camadas, persistência, exemplos e limites.
- [Receitas MDX](plugins/dietflow-docs/assets/playbooks/documentacao-mdx.md): quick, guia, jornada e operação admin.
- [Censo e impacto](plugins/dietflow-docs/assets/playbooks/censo-e-impacto.md): seleção por tema/WIP/branch sem prometer cobertura automática.
- [Mermaid](plugins/dietflow-docs/assets/playbooks/diagramas-mermaid.md): mapa conceitual, fluxo, camadas, ER, requisitos, sequência e lifecycle opcionais.
- [Ajuda contextual](plugins/dietflow-docs/assets/playbooks/ajuda-contextual.md): extensão autorizada e diagnóstico no owner existente.
- [Mapa de fontes](plugins/dietflow-docs/assets/references/fontes-dietflow.md): entradas relativas ao checkout e tratamento de divergência.

Admin-docs só publica em destino protegido comprovado. Quando faltar infraestrutura, produz rascunho fora de coleções compiladas. Não implementa guard/rota por consequência de autoria. Mermaid no pacote não comprova suporte visual no MDX/drawer. Diagramas existentes corretos não são convertidos em massa.

## Atualização e recuperação

Registre origem, tag e versão consumida antes de atualizar. No Codex, remova somente `dietflow-docs@dietflow-docs` e o cadastro `dietflow-docs`, cadastre a nova tag e reinstale. Atualizar uma origem pinada a uma tag não equivale a escolher outra release. Se falhar, retire a candidata e reinstale a tag anterior. Preserve outros plugins.

Para substituir skills antigas, mantenha backup fora dos diretórios de descoberta, com inventário dos caminhos de origem. Depois da conferência da candidata, desative somente as substituídas. Em rollback, retire o plugin candidato antes de restaurar uma skill global homônima e confira a descoberta em sessão nova.

## Manutenção e distribuição

Versão inicial 0.1.0. Os três catálogos e quatro manifests do pacote devem manter identidade/versão coerentes. Preserve links relativos e empacote assets com as skills. Publique tag e arquivos da release após conferir o conteúdo. Source público e release não comprovam instalação, execução em cada host ou qualidade de todas as docs do consumidor. Resultados efetivamente observados ficam em [Verificação](VERIFICATION.md).

## Licença

MIT. Exemplos são fictícios. Não adicionar ao repo credenciais, dados pessoais, dumps ou arquivos internos sem recorte e autorização.
