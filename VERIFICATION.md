# Verificação da distribuição 0.1.1

## Fonte e pacote

- Identidade/versão coerentes nos três catálogos e quatro manifests do pacote.
- Três skills com nome/frontmatter correspondentes ao diretório; assets e links relativos resolvidos.
- Blocos Markdown conferidos; nenhum path absoluto do Mac ou credencial no conteúdo distribuído.
- `claude plugin validate` aprovou marketplace e pacote. A verificação adicional de directory submission aponta ausência de ícone; o repo não foi submetido a diretório público de fornecedor.
- Sete exemplos Mermaid renderizados sem erro com Mermaid CLI 11.12.0 e Chrome local; as sete imagens foram abertas para inspeção. Fluxo, camadas, mapa, ER, sequence, state e requisitos apresentaram conteúdo sem corte no recorte inspecionado. Isso não prova renderização no MDX/drawer.

## Limites

O formato Cursor acompanha marketplace/manifest oficiais e o layout Superflow. Não houve execução no Cursor, que não está disponível como CLI neste host. Validação Claude de manifest não é exercício de suas skills em uma sessão Claude. Instalação/discovery Codex e migração são observações locais registradas nas notas da release; não presumir que outras máquinas já instalaram o plugin.

Uma passagem editorial seguindo as instruções é distinta de comprovar um comportamento determinístico em todos os modelos e hosts. Nenhuma stack do DietFlow, banco, alteração de dados reais ou suporte Mermaid/admin de produto faz parte desta verificação.

Patch 0.1.1: link de README externo ao pacote substituído pela URL pública; referências relativas também conferidas no ZIP isolado.

## Atualização 0.1.2 — descoberta do módulo

A receita compartilhada foi confrontada por leitura com o fluxo legado doc-module/doc-explorer e com as entradas e limites das três skills atuais. As rotas de descoberta incluem casos sem docs/delta e reaproveitamento de investigação compatível. Escrita por público preserva destinos, fonte única do quick e segregação administrativa. Não houve geração de documentação de produto nem exercício independente em sessão nova nesta atualização.

As três skills passaram no quick_validate do skill-creator (PyYAML vendorizado já instalado no Superflow, sem nova instalação). Os 30 links relativos do repo foram resolvidos e os sete manifests/catálogos concordam em 0.1.2. O validador nativo Claude aprovou marketplace e pacote; permanece o aviso de ícone de directory submission, fora desta atualização.

A seção de como/por quê foi elaborada após leitura das skills Pstack how/why v0.9.133, templates de exploração/explicação e guia de evidência. A receita incorpora os padrões com redação própria e referências de elaboração, sem depender desses arquivos ou adotar sua orquestração. A revisão por leitura distinguiu mecanismo, motivo histórico e orientação prática por público; não houve exercício de investigação histórica nem execução das skills Pstack.

A release v0.1.2 foi publicada a partir do commit 71ea334609f6f7faec33414ed6a617a4bda766db com ZIP, source.tar.gz e SHA256SUMS. O ZIP baixado da release conferiu com o checksum publicado. Os 22 links relativos do pacote isolado foram resolvidos. A instalação Codex local foi substituída pelo CLI suportado, mantendo o marketplace e avançando sua tag para v0.1.2; os 15 arquivos do cache coincidiram byte a byte com o ZIP da release. O plugin existente na conta pessoal foi atualizado para 0.1.2, preservando identidade, escopo privado, apresentação e prompts. Os 15 arquivos salvos foram lidos de volta e conferidos (JSON por equivalência estrutural, Markdown por conteúdo exato). Isso verifica distribuição e conteúdo recebido; não comprova execução editorial em sessão nova nem atualização automática da conta pelo Git.
