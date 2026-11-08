# Verificação da distribuição 0.1.0

## Fonte e pacote

- Identidade/versão coerentes nos três catálogos e quatro manifests do pacote.
- Três skills com nome/frontmatter correspondentes ao diretório; assets e links relativos resolvidos.
- Blocos Markdown conferidos; nenhum path absoluto do Mac ou credencial no conteúdo distribuído.
- `claude plugin validate` aprovou marketplace e pacote. A verificação adicional de directory submission aponta ausência de ícone; o repo não foi submetido a diretório público de fornecedor.
- Sete exemplos Mermaid renderizados sem erro com Mermaid CLI 11.12.0 e Chrome local; as sete imagens foram abertas para inspeção. Fluxo, camadas, mapa, ER, sequence, state e requisitos apresentaram conteúdo sem corte no recorte inspecionado. Isso não prova renderização no MDX/drawer.

## Limites

O formato Cursor acompanha marketplace/manifest oficiais e o layout Superflow. Não houve execução no Cursor, que não está disponível como CLI neste host. Validação Claude de manifest não é exercício de suas skills em uma sessão Claude. Instalação/discovery Codex e migração são observações locais registradas nas notas da release; não presumir que outras máquinas já instalaram o plugin.

Uma passagem editorial seguindo as instruções é distinta de comprovar um comportamento determinístico em todos os modelos e hosts. Nenhuma stack do DietFlow, banco, alteração de dados reais ou suporte Mermaid/admin de produto faz parte desta verificação.
