# Plano de implementação — Portfólio NAPED Afya Ipatinga

**Estado:** proposta para alinhamento · **Data:** 15/09/2026 · **Destino previsto:** [JeffersonNetto/portifolio-naped-afya-ipatinga](https://github.com/JeffersonNetto/portifolio-naped-afya-ipatinga) · **Período de lançamento:** 2026.

## 1. Objetivo e decisões já alinhadas

Criar um portfólio público das ações e dos resultados do **Núcleo de Apoio Pedagógico e Experiência Docente (NAPED) da Afya Ipatinga, MG**. O site deve ser mais refinado visualmente que a referência, fácil de atualizar e publicado no GitHub Pages do repositório já existente. O usuário fornecerá e aprovará textos, imagens, números e documentos finais. A identidade deve seguir o guia de marca Afya.

O produto é um **site do NAPED**, com contexto breve da unidade. Não deve reproduzir o portal institucional inteiro, apresentar ações de São João del-Rei como se fossem de Ipatinga, nem mostrar métricas inventadas. A primeira versão cobre 2026. A estrutura técnica deverá aceitar 2027 sem refazer a arquitetura. **Entrega imediata:** esqueleto navegável, arquivos-molde, guia de materiais e workflow preparado; o acervo real será acrescentado em breve.

**Decisões ainda abertas:** disponibilidade do guia de marca, direitos dos arquivos, lista de eixos, nome institucional exato e conteúdo inicial. A primeira versão deve reproduzir a **estrutura central** do exemplo, adaptada a Ipatinga: vitrine, meses, projetos, equipe, painel, recortes “Em Números” e comprovações. Páginas sem materiais locais aprovados devem usar um estado editorial honesto durante a preparação e só entrar no menu público quando tiverem conteúdo útil. O cadastro será por arquivos em **editor local**; a escolha do editor ainda está em alinhamento.

## 2. O que foi inspecionado

| Fonte | Papel no projeto | Observações verificadas |
| --- | --- | --- |
| [Portal Afya Ipatinga](https://ipatinga.afya.com.br/) | Contexto da unidade | Navegação institucional extensa; NAPED aparece como seção própria. Endereço da unidade no rodapé. |
| [Página NAPED Ipatinga](https://ipatinga.afya.com.br/institucional/naped) | Terminologia e escopo local | Descreve missão, apoio pedagógico, formação docente, equipe, atribuições, guias, GREMAÇO e contato. Contém dados históricos e trechos “Em construção”; tudo que for publicado em 2026 precisa de conferência editorial. |
| [Receita do Portfólio](https://bergohellen-hub.github.io/portfolionaped2026/receita.html) | Explicação da arquitetura | Propõe Quarto, arquivos `.qmd`, `listing`, curinga para novas ações e publicação via GitHub Pages. |
| [Manual do Portfólio](https://bergohellen-hub.github.io/portfolionaped2026/manual.html) | Fluxo editorial | Uma ação por arquivo em `acoes/`, fotos em `fotos/`, metadados no cabeçalho, conferência antes da publicação e atualização automática dos índices. |
| [Repositório de referência](https://github.com/bergohellen-hub/portfolionaped2026) | Implementação verificável | Quarto + SCSS + scripts R. `pre-render` valida e cria páginas mensais; workflow gera `_site` e usa GitHub Actions/Pages. |
| [Vitrine](https://bergohellen-hub.github.io/portfolionaped2026/), [Meses](https://bergohellen-hub.github.io/portfolionaped2026/meses.html), [Painel](https://bergohellen-hub.github.io/portfolionaped2026/dashboard.html) | Experiência do visitante | Busca e filtros, cartões, navegação mensal, métricas e tabela de ações. O painel explica a cobertura parcial dos dados de alcance. |

**Transferência de ideia, não de conteúdo:** replicar a organização e o ciclo editorial; redesenhar apresentação, componentes e texto para Ipatinga. Não copiar fotografias, logotipos do repositório, resultados, perfis ou documentos de São João del-Rei.

## 3. Proposta de experiência

### Públicos e tarefas

- **Gestão e docentes:** localizar uma ação por tema ou mês, consultar resultado e evidência, obter visão anual.
- **Comunidade institucional:** compreender o papel do NAPED em Ipatinga e conhecer a equipe e iniciativas.
- **Editor responsável:** cadastrar uma ação e imagens uma vez; conferir erros em português e verificar a publicação.

### Navegação proposta

1. **Início:** apresentação curta do NAPED, foto autorizada, destaques editoriais, números com fonte e cobertura, ações recentes e acesso ao acervo.
2. **Ações:** vitrine 2026 com busca textual, filtros de mês e eixo, ordenação por data e estado vazio.
3. **Meses:** lista de meses com ações; página de cada mês gerada automaticamente; ano visível em cada contexto.
4. **Projetos:** seção e páginas permanentes dos programas confirmados de Ipatinga; mapa de projetos antes de criar páginas.
5. **Equipe:** perfis atuais aprovados, papel, foto e contato institucional quando autorizado.
6. **Resultados:** painel derivado dos metadados; totais e gráficos explicam denominador e dados ausentes. Recortes “Em Números” por semestre de 2026 reproduzem a dimensão narrativa do exemplo sem duplicar números manualmente.
7. **Comprovações:** índice público de evidências autorizadas e instrução de solicitação para materiais internos.
8. **Sobre/Contato:** atribuições e canais oficiais confirmados.
9. **Documentação editorial:** arquivos internos do repositório explicam a atualização por editor local e a manutenção técnica do portfólio, adaptados ao fluxo real de Ipatinga.

Menu enxuto no celular; acessos principais acima da dobra. Evitar menus com itens vazios e esconder módulos sem conteúdo aprovado.

### Direção visual premium, subordinada ao guia Afya

- Marca Afya aplicada nas versões e áreas de respiro oficiais. O usuário ainda não possui o guia nem logo autorizado: a aparência do esqueleto é **provisória**, com referência cromática do portal oficial; paleta, tipografia e regras finais vêm do guia ou de validação institucional posterior. Tokens centralizados em SCSS.
- Layout editorial com mais espaço em branco, hierarquia tipográfica forte, largura de leitura confortável, contraste alto e cartões de proporção estável.
- Hero com imagem real de Ipatinga autorizada, recorte cuidadoso e mensagem específica. Sem mosaico de fotos repetitivo quando a qualidade do acervo não sustentar isso.
- Números integrados à narrativa, com legenda de período e cobertura; evitar “placar” de dados incompletos.
- Fotografias com tratamento consistente de enquadramento; miniaturas responsivas, legenda e texto alternativo.
- Interação discreta: estados de foco e hover claros, movimento reduzido quando solicitado pelo sistema, filtros visíveis e navegação por teclado.
- Componentes reutilizáveis: cabeçalho, rodapé, cartões, etiquetas, blocos de métrica, linha do tempo, galerias, callouts e tabelas.

Antes de codificar, entregar **moodboard + wireframes mobile/desktop + protótipo visual** para aprovação. Não assumir cores ou fontes do guia sem vê-lo.

## 4. Arquitetura e fluxo de dados

**Escolha proposta: Quarto**, porque os links fornecidos explicam precisamente esse fluxo e ele permite publicar uma ação criando um `.qmd`. A camada de apresentação pode usar SCSS e fragmentos HTML/JS pequenos. O site final é estático e compatível com GitHub Pages. O repositório de destino está público e vazio no momento desta inspeção; há remoto local configurado, mas sem commits. Quarto e R não estão instalados neste ambiente local; a implementação pode usar a CI ou preparar um ambiente de desenvolvimento antes de testar a renderização. A equipe usará **VS Code** no fluxo editorial.

```text
acao .qmd + fotos/documentos autorizados
          ↓
validação de campos, arquivos, datas, taxonomia e regras editoriais
          ↓
renderização Quarto → vitrine + ação + mês + painel + busca
          ↓
artifact _site → GitHub Actions → GitHub Pages
```

Estrutura inicial prevista:

```text
.
├── .github/workflows/publicar.yml
├── _quarto.yml
├── index.qmd
├── acoes.qmd
├── meses.qmd
├── resultados.qmd
├── equipe.qmd
├── sobre.qmd
├── acoes/
│   ├── _modelo.qmd
│   └── 2026-MM-slug.qmd
├── meses/                  # páginas geradas por ano-mês
├── projetos/               # somente programas locais confirmados
├── em-numeros/              # recortes de 2026.1 e 2026.2
├── comprovacoes.qmd
├── fotos/                  # somente imagens autorizadas
├── assets/                 # CSS, scripts pequenos, ícones próprios
├── scripts/                # validação, leitura de metadados, geração
├── docs/                   # orientações editoriais e decisões
└── PLANO_IMPLEMENTACAO.md
```

### Contrato de uma ação

| Campo | Regra proposta | Uso |
| --- | --- | --- |
| `title`, `description`, `date` | Obrigatórios; data ISO válida | Página, cartão, busca, ordenação |
| `categories` ou `eixos` | Eixos da taxonomia local, 1–2 por ação | Filtros e gráfico por tema |
| `image` e `image-alt` | Imagem opcional; se declarada, arquivo e descrição obrigatórios | Cartão e compartilhamento |
| `participantes`, `horas` | Numéricos, opcionais, não negativos, com unidade clara | Indicadores de alcance |
| `publico`, `cursos`, `local` | Opcionais, vocabulário controlado quando houver agrupamento | Contexto e recortes |
| `resultados`, `evidencias` | Texto/links aprovados; evidências públicas ou acessíveis por pedido | Credibilidade |
| `status` | Rascunho/publicado, para evitar exposição prematura | Publicação |
| `ordem` | Opcional, somente para curadoria dentro do mês | Ordenação em empate |

O mês e o ano são **derivados da data**, e o nome `AAAA-MM-slug.qmd` deve concordar com ela. Não confiar somente na etiqueta “Agosto”, pois misturaria 2026 e 2027. A validação deve indicar arquivo, campo e correção em português. O modelo ignorado pelo build deve impedir que `acoes/_modelo.qmd` entre em qualquer contagem.

### Semântica das métricas

- **Ações:** quantidade de arquivos publicados e válidos, sem contar modelo, rascunhos ou programas descritos em páginas permanentes.
- **Meses cobertos:** pares ano-mês com ao menos uma ação publicada.
- **Eixos:** valores distintos da taxonomia, sem contar etiqueta de mês.
- **Participantes:** soma **apenas** dos arquivos com `participantes` informado. Exibir “X de Y ações com esse dado”; evitar tratar ausência como zero. Registrar se os mesmos indivíduos podem aparecer em ações diferentes, para não chamar a soma de “pessoas únicas”.
- **Horas:** definir com o usuário se representa carga horária do evento ou horas de formação oferecidas; nunca multiplicar por participantes sem campo e regra específicos.
- **Gráfico por eixo:** uma ação pode contar em dois eixos; explicar que a soma das barras pode exceder o total de ações.
- **Fotografias:** quantidade no acervo somente se for métrica útil e houver curadoria; não priorizar esse número na home.

## 5. Publicação e operação

Usar **GitHub Actions como origem do Pages**. A workflow fará checkout, instalará Quarto e a runtime necessária, validará conteúdo, renderizará `_site`, enviará artifact e publicará em `github-pages`. As ações terão permissões mínimas para leitura do repositório e escrita do Pages. O endereço esperado, conforme a documentação de [tipos de sites GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages), é `https://jeffersonnetto.github.io/portifolio-naped-afya-ipatinga/`, sujeito à configuração real do repositório. Toda URL, `site-url`, imagem e link interno deve funcionar sob esse prefixo; conferir também maiúsculas/minúsculas nos nomes de arquivo.

Antes de publicar, executar `quarto render`, validação de metadados, inspeção de links e QA visual. Após push, observar Actions e URL publicada. A documentação atual de [workflows personalizados do Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/using-custom-workflows-with-github-pages) exige habilitar a origem por GitHub Actions e usa `configure-pages`, `upload-pages-artifact` e `deploy-pages`. Não expor credenciais, evidências internas ou dados pessoais no repositório público.

O `gh auth status` local indica token inválido nesta sessão. Esse ponto **não impede planejar ou criar os arquivos locais**; autenticação válida será necessária apenas no ticket de envio/publicação. O destino no GitHub foi verificado como repositório público ainda vazio.

## 6. Conteúdo e aprovações

Receber do usuário: guia de marca; variante de logotipo autorizada; fotos com permissão de publicação e legenda; textos institucionais revisados; nomes/cargos atuais da equipe; lista de ações 2026 com data, objetivo, atividades, resultado, público e evidências; regra de divulgação de documentos; canais de contato; lista de projetos; nomenclatura dos eixos; definição das métricas. Registrar em planilha/Markdown de inventário com estado “recebido → revisado → aprovado → publicado”.

A página institucional de Ipatinga é boa fonte para missão e atribuições, mas seus dados de equipe, telefones, cronogramas e documentos devem ser reconfirmados. O portfólio não deve publicar os dados de São João del-Rei. Se o acervo inicial estiver incompleto, lançar somente as seções com conteúdo aprovado e mostrar o período/cobertura dos indicadores de forma honesta.

## 7. Fases, dependências e critérios de lançamento

| Fase | Resultado | Tickets | Condição para avançar |
| --- | --- | --- | --- |
| 0. Alinhamento | Escopo, inventário e identidade | NAPED-01 a 03 | Guia e amostra de conteúdo recebidos; mapa aprovado |
| 1. Fundação | Quarto, modelo, validação e dados derivados | NAPED-04 a 06 | Arquivo de ação de teste gera página, mês e métricas corretas |
| 2. Experiência | Layout, vitrine, detalhe, meses, equipe, resultados, projetos e comprovações | NAPED-07 a 11 | Fluxos desktop/mobile e teclado verificados |
| 3. Conteúdo | Cadastro, recortes semestrais e documentação editorial | NAPED-12 e 13 | Material 2026 aprovado; nenhuma ação ou número atribuído indevidamente |
| 4. Entrega | CI, Pages, QA e revisão final | NAPED-14 a 16 | Render e workflow verdes, URL real conferida, aceite editorial |

**Definição de pronto geral:** todos os links e imagens funcionam no prefixo do Pages; há somente conteúdo de Ipatinga aprovado; página e painel concordam com os arquivos; mobile, teclado e contraste estão adequados; Open Graph, título e descrição representam o NAPED; o editor consegue seguir a documentação editorial; uma ação nova não exige editar índices; publicação mantém a última versão válida se um build falhar.

**Riscos concretos e respostas:**

| Risco | Tratamento |
| --- | --- |
| Guia de marca ou fotos indisponíveis | Projetar componentes sem marca aplicada; não concluir identidade/publicação final antes do material aprovado. |
| Dados incompletos de alcance | Ocultar total sem cobertura ou mostrar “dados informados em X/Y ações”, sem imputar zero. |
| Fotos/documentos com restrição | Manter fora do repositório público; link ou pedido de acesso somente após aprovação. |
| Divergência entre data, arquivo e filtro mensal | Validação bloqueante antes do render. |
| Falha de autenticação GitHub | Preparar site e workflow localmente; resolver login no ticket de publicação. |
| Dependências R/Quarto elevarem manutenção | Centralizar scripts, fixar versões, documentar execução e avaliar implementação leve se o escopo do painel for simples. |

## 8. Tickets

Os tickets independentes estão em [`tickets/`](tickets/README.md). Cada um define entrega, dependências, tarefas, critérios de aceite e verificação. As prioridades e sequência são propostas; perguntas pendentes podem ajustar o escopo antes da implementação.
