# DietFlow Docs

Plugin de documentação do DietFlow com três entradas: dietflow-docs para desenvolvimento, user-docs para nutricionistas e admin-docs para operadores administrativos. Cada skill cria, atualiza, consolida ou recenseia conforme o contexto. Receitas próprias ensinam escrita, seleção por impacto, árvores, arquitetura em camadas e Mermaid, sem exigir acesso a documentos exemplares externos.

## Instalar no Claude Code

```text
/plugin install dietflow-docs --marketplace nmarcofernandess/dietflow-docs
```

O [README do repositório](https://github.com/nmarcofernandess/dietflow-docs#readme) contém os procedimentos de Codex e Cursor, atualização e recuperação. Preserve o pacote inteiro: as skills carregam assets por caminhos relativos. Admin sem publicação protegida produz rascunho fora das coleções compiladas; aceitar MDX não comprova renderização Mermaid. O plugin não contém runtime, servidor MCP ou credenciais de acesso ao DietFlow.
