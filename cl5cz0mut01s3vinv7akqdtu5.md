---
title: "Gitflow - Facilitando o flow de branches"
datePublished: Fri Jul 08 2022 21:29:27 GMT+0000 (Coordinated Universal Time)
cuid: cl5cz0mut01s3vinv7akqdtu5
slug: gitflow-facilitando-o-flow-de-branches
cover: https://cdn.hashnode.com/res/hashnode/image/unsplash/842ofHC6MaI/upload/v1657315939875/ggXrAyNv0.jpeg
tags: git, gitflow

---

Olá pessoal, quando comecei a trabalhar com Git, sempre achei a ferramenta fantástica, pois com ela é possível trabalhar em diversas versões do código em paralelo, ter backup do seu código, voltar versões, acompanhar modificações e etc, porém uma coisa que sempre tive dificuldade era na padronização das minhas branches, de ter um fluxo para publicação e acompanhamento bacana das evoluções do que estava trabalhando, foi então que fui apresentado ao Gitflow ([Artigo Atlassian](https://www.atlassian.com/br/git/tutorials/comparing-workflows/gitflow-workflow)), o que vou trazer então nesse artigo é uma mistura de boas práticas do Gitflow com commits semânticos.

O GitFlow é um modelo de ramificação que ajuda os desenvolvedores a organizar e gerenciar suas branches de forma mais eficiente. Ele define um conjunto padrão de branches para diferentes propósitos, como `feature`, `release`, `develop`, e `master`. Cada uma dessas branches serve a um propósito específico e ajuda a manter o repositório organizado e previsível.

Por exemplo, a branch `feature` é usada para desenvolver novas funcionalidades de forma isolada, em locais que trabalhei era muito comum utilizar `feature/card-number-in-jira`, por exemplo: `feature/BAS-23`. Uma vez que a funcionalidade está pronta e testada, ela é mesclada de volta à branch `develop`, onde todas as funcionalidades se encontram antes de serem lançadas. Isso facilita a integração contínua e a entrega contínua (CI/CD), pois permite que várias funcionalidades sejam desenvolvidas em paralelo sem interferir umas nas outras.

Além disso, o GitFlow sugere a criação de branches `release` para preparar, finalizar e ajustar as versões que serão lançadas. Essas branches são criadas a partir da `develop` e são destinadas a receber apenas correções de bugs e ajustes finais antes de serem mescladas à `master` e à `develop`, garantindo que a `master` sempre reflita uma versão estável do produto. Uma estratégia muito boa no que se refere aos cortes de release é utilizar *tags* no seu repositório de git preferido.

Agora, combinando o GitFlow com commits semânticos, temos uma poderosa ferramenta de comunicação. Commits semânticos são mensagens de commit que seguem um padrão predefinido e que transmitem o propósito do commit de forma clara. Por exemplo, commits que começam com `feat:` indicam a adição de uma nova funcionalidade, enquanto `fix:` indica a correção de um bug, veja abaixo uma relação de prefixos que podem ser utilizados em commites semânticos:

Essa padronização nas mensagens de commit não só melhora a legibilidade do histórico do repositório, mas também facilita a geração automática de logs de mudanças (changelogs) e a identificação rápida do tipo de alteração realizada. Isso é especialmente útil em equipes grandes, onde a comunicação clara e eficiente é fundamental para o sucesso do projeto.