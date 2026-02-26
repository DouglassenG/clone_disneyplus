# 🎬 Clone Interface - Disney+

> Recriação *pixel-perfect* da Landing Page do Disney+, arquitetada com foco em semântica HTML, modularidade de estilos via pré-processadores e automação do fluxo de build para otimização de performance front-end.

## 🎯 Motivação e Propósito

Interfaces de plataformas de streaming são inerentemente pesadas devido ao grande volume de imagens em alta resolução e seções interativas. O propósito deste projeto foi aplicar os conceitos de **Automação de Tarefas (Task Runners)** e **Arquitetura CSS** para construir uma aplicação estática limpa, manutenível e performática.

Este repositório resolve o problema da entrega de *assets* pesados ao cliente final. Em vez de enviar imagens brutas e arquivos CSS extensos, o código fonte passa por um processo automatizado de compressão antes de ser servido no navegador, simulando o pipeline de um ambiente de produção real.

> **Resultados de Otimização e Performance:** "A implementação do **Gulp** aliado aos plugins de minificação (`gulp-uglify` e `gulp-sass`) e compressão de imagens (`gulp-imagemin`) reduziu significativamente o tamanho final da pasta de distribuição (`/dist`), diminuindo o tempo de requisição dos assets estáticos e otimizando a métrica de *First Contentful Paint (FCP)* no carregamento da interface."

## 🛠️ Tecnologias Utilizadas

A stack baseia-se na tríade fundamental da web, potencializada por ferramentas de compilação:

* **[HTML5](https://developer.mozilla.org/pt-BR/docs/Web/HTML):** Estruturação semântica da página.
* **[SASS / SCSS](https://sass-lang.com/):** Pré-processador CSS. Utilizado em conjunto com a **Metodologia BEM (Block, Element, Modifier)** para criar um CSS escalável, evitando conflitos de especificidade.
* **[JavaScript (Vanilla)](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript):** Controle de manipulação do DOM e eventos.
* **[Gulp](https://gulpjs.com/):** Automatizador de tarefas em Node.js para processar os arquivos da pasta `/src` e gerar os binários na pasta `/dist`.

## ✨ Funcionalidades

A aplicação possui interatividades chaves replicadas nativamente, sem uso de bibliotecas de terceiros:

1.  **Header Dinâmico:** Alteração da transparência e *background-color* do menu de navegação baseada no evento de *scroll* da janela.
2.  **Sistema de Abas (Tabs):** Navegação assíncrona visual entre as seções de categorias (Filmes, Séries, Exclusivos) através de manipulação de classes CSS ativas.
3.  **FAQ Interativo (Accordion):** Seção expansível para perguntas frequentes.
4.  **Layout Responsivo:** Breakpoints configurados via Media Queries para adaptação perfeita em dispositivos móveis, tablets e telas Desktop.

## 📂 Estrutura de Arquivos

A organização do projeto isola o ambiente de desenvolvimento do código de produção gerado dinamicamente:

```text
clone_disneyplus/
├── src/                 # Código-fonte bruto (Ambiente de Dev)
│   ├── images/          # Imagens originais (Backgrounds, Posters)
│   ├── scripts/         # Lógica JavaScript (main.js)
│   └── styles/          # Arquivos SCSS componentizados
│       ├── _variables.scss
│       ├── _header.scss
│       └── main.scss
├── dist/                # Código de Produção (Gerado pelo Gulp)
│   ├── images/          # Imagens comprimidas
│   ├── scripts/         # JS ofuscado e minificado
│   └── styles/          # CSS final compilado
├── gulpfile.js          # Arquivo de configuração das tarefas do Gulp
├── package.json         # Gestão de dependências (Node.js)
└── index.html           # Ponto de entrada estrutural
