# NAPED-13 — Manual e Receita adaptados a VS Code

**Prioridade:** P1 · **Estimativa:** 2–3 dias úteis · **Dependências:** NAPED-05/06/14.

## Resultado esperado

Manual explica à equipe de Ipatinga como cadastrar ações pelo **VS Code local**; Receita documenta como o projeto é montado e mantido. Ambos acompanham o fluxo real do repositório e integram a estrutura completa solicitada.

## Trabalho

- Manual: abrir pasta do repo no VS Code, atualizar `main`, copiar `_modelo.qmd`, adicionar/otimizar fotos, preencher campos, executar validação e preview, revisar, commit/push e acompanhar Actions.
- Explicar campos e taxonomia com exemplos **sintéticos** claramente identificados, sem sugerir que ocorreram em Ipatinga.
- Documentar mensagens de erro comuns: data/nome divergentes, foto faltante, YAML inválido, métrica textual, categoria errada e build vermelho.
- Explicar como corrigir/retirar uma ação, abrir um mês novo e inserir projeto/evidência; mudanças de menu permanecem tarefa de implementação.
- Receita: arquitetura Quarto, diretórios, scripts, decisão sobre metrics e publicação GitHub Pages; incluir passos de desenvolvimento em VS Code.
- Deixar manual como página do site e Markdown/arquivo-fonte no repo; se PDF for necessário, gerar da mesma fonte e verificar visualmente.
- Atualizar os exemplos sempre que o contrato ou workflow mudar.

## Critérios de aceite

- Um editor que não criou o projeto consegue adicionar uma ação válida seguindo o manual.
- Comando, pastas, campos e telas descritos correspondem ao repo implementado.
- Manual/Receita não dependem de Positron e não reproduzem conteúdos da outra unidade.
- Qualquer exemplo fictício está rotulado como tal.

## Verificação

Ensaio com uma ação de teste no VS Code, sem instrução oral; corrigir trechos ambíguos.
