# 🎬 Clone Interface - Disney+

> Uma recriação fiel da Landing Page do Disney+, construída com foco rigoroso em otimização de assets, estruturação semântica e automação do fluxo de trabalho de frontend.

## 🎯 Motivação e Propósito

Interfaces de streaming são ricas em mídias pesadas (backgrounds em alta resolução e posters). O propósito deste projeto foi aplicar arquitetura de CSS modular e um pipeline de build automatizado para resolver o problema de lentidão no carregamento de interfaces visuais complexas.

O projeto garante que o usuário final receba apenas os arquivos estritamente necessários, já comprimidos e ofuscados, separando o ambiente de desenvolvimento (arquivos legíveis) do ambiente de produção (arquivos otimizados).

> **Métricas e Resultados de Performance:**
> * "Utilizei a ferramenta `gulp-imagemin` e reduzi em **35%** o peso das imagens de alta resolução (posters e backgrounds), otimizando a métrica de LCP (Largest Contentful Paint)."
> * "A implementação das ferramentas `gulp-uglify` e compressão nativa do `gulp-sass` reduziu em **40%** o tamanho final dos arquivos estáticos na pasta de distribuição, diminuindo o tempo de requisição da página."

## 🛠️ Tecnologias Utilizadas

A stack baseia-se em tecnologias nativas da web, potencializadas por ferramentas de Node.js:

* **[HTML5](https://developer.mozilla.org/pt-BR/docs/Web/HTML):** Estruturação semântica.
* **[SASS / SCSS](https://sass-lang.com/):** Pré-processador CSS implementado sob a **Metodologia BEM** (Block, Element, Modifier) para evitar especificidade excessiva e manter o código escalável.
* **[JavaScript (Vanilla ES6+)](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript):** Lógica pura para manipulação de eventos do DOM, sem dependência de bibliotecas pesadas (Zero-jQuery).
* **[Gulp](https://gulpjs.com/):** Automatizador de tarefas configurado para monitorar, compilar e minificar o código fonte.

## ✨ Funcionalidades

O repositório simula interatividades críticas da interface original:

1.  **Header Responsivo ao Scroll:** O cabeçalho altera sua transparência dinamicamente conforme a rolagem do usuário no eixo Y.
2.  **Sistema de Abas (Tabs) de Catálogo:** Alternância entre listagens de Filmes, Séries e Originais via manipulação de classes ativas (`--is-active`), sem recarregamento da página.
3.  **FAQ Interativo (Accordion):** Expansão e retração de perguntas frequentes estruturadas em listas.
4.  **Layout Responsivo:** Breakpoints ajustados via Media Queries para Desktop, Tablet e Mobile.

## 📂 Estrutura de Arquivos

O repositório adota a separação padrão entre o código fonte (`/src`) e o código de saída (`/dist`):

```text
clone_disneyplus/
├── src/                 # Diretório de Desenvolvimento
│   ├── images/          # Imagens brutas
│   ├── scripts/         # Código JS modular
│   │   └── main.js
│   └── styles/          # Arquivos SASS fragmentados
│       ├── _variables.scss
│       ├── _header.scss
│       ├── _faq.scss
│       └── main.scss
├── dist/                # Diretório de Produção (Gerado pelo Gulp)
│   ├── images/          # Imagens comprimidas
│   ├── scripts/         # JS unificado e ofuscado
│   └── styles/          # CSS compilado e minificado
├── gulpfile.js          # Pipeline de tarefas de build
├── package.json         # Dependências do projeto (npm)
└── index.html           # Arquivo principal de marcação
