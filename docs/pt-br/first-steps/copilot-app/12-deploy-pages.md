---
title: "Lição 12 - Publique o site com o GitHub Pages"
description: "Use o aplicativo GitHub Copilot para configurar um fluxo de trabalho do Pages, revisar a pull request e verificar o Space Quiz publicado."
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Publique o Space Quiz com o GitHub Pages para que qualquer pessoa possa acessá-lo. O Copilot pode preparar o fluxo de trabalho e orientar a implantação, mas você é responsável por revisar as alterações e confirmar que o site está no ar.

Nesta lição, você vai:

- pedir ao Copilot que configure a publicação no GitHub Pages.
- revisar o fluxo de trabalho e a pull request antes de fazer o merge.
- acompanhar a implantação e verificar o site publicado.

## Cenário

O Space Quiz já está em um repositório do GitHub, mas ainda falta uma maneira simples de experimentá-lo. Publicar o site de arquivo único com o GitHub Pages disponibiliza uma URL pública sem adicionar um servidor ou uma dependência de runtime.

## Peça ao Copilot para publicar o site

Na sessão do aplicativo Copilot para `space-quiz`, envie este prompt:

```plaintext
Habilite o GitHub Pages para este repositório. Crie um fluxo de trabalho do GitHub Actions que compile o site, se necessário, e o publique no GitHub Pages. Adicione um README que descreva o aplicativo e como executá-lo localmente, caso ainda não exista. Crie uma pull request com essas alterações e faça o merge depois que as verificações obrigatórias forem aprovadas. Acompanhe a implantação até ela ser concluída e, em seguida, informe a URL final do site publicado. Se você não tiver permissão para habilitar o Pages ou fazer o merge, diga exatamente o que preciso aprovar ou fazer; não informe que houve sucesso até o site estar no ar.
```

![Diagrama em três etapas: pull request do space-quiz mesclada; execução Deploy website do GitHub Actions concluída com as etapas Build website, Upload artifact e Deploy to Pages; e Space Quiz publicado em yourname.github.io/space-quiz/.](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> Este prompt pede ao agente que crie e faça o merge de uma pull request e altere as configurações do Pages do repositório. Antes de continuar, revise o diff, as permissões de implantação e qualquer solicitação de aprovação do GitHub.

## Revise o fluxo de trabalho e verifique a implantação

1. Confirme que o README só foi adicionado se ainda não havia um no repositório.
2. Revise as alterações da pull request, incluindo as etapas de compilação e implantação do fluxo de trabalho.
3. Faça o merge somente depois que as verificações obrigatórias da pull request forem aprovadas.
4. Acompanhe a execução de implantação do GitHub Actions até a conclusão.
5. Abra a URL informada e confirme que o Space Quiz é carregado.

Se o agente não puder habilitar o Pages ou fazer o merge da pull request, siga as instruções específicas fornecidas. Não considere a tarefa concluída até a implantação terminar e o site publicado carregar.

## Resumo e próximos passos

O Space Quiz agora está disponível como um site publicado, e você verificou a implantação em vez de confiar no relatório do agente. Continue para a [Lição 13: revisão e próximos passos][next-lesson].

[next-lesson]: ../13-review/
