# 🎬 Disney+ Clone - Frontend Landing Page

![Status](https://img.shields.io/badge/Status-Finalizado-green)
![HTML5](https://img.shields.io/badge/Markup-HTML5-E34F26?logo=html5&logoColor=white)
![SASS](https://img.shields.io/badge/Style-SASS-CC6699?logo=sass&logoColor=white)
![JavaScript](https://img.shields.io/badge/Code-JavaScript-F7DF1E?logo=javascript&logoColor=black)
![Gulp](https://img.shields.io/badge/Task_Runner-Gulp-CF4647?logo=gulp&logoColor=white)

> Recriação *Pixel-Perfect* da interface da página de destino (Landing Page) do Disney+, focada em performance, design responsivo e interatividade nativa.

## 🎯 Motivação e Propósito

Construir interfaces de plataformas de streaming exige atenção rigorosa a detalhes visuais e ao peso dos arquivos, pois são páginas com alta carga de imagens de fundo (backgrounds) e elementos sobrepostos. O propósito deste projeto foi consolidar conhecimentos em **Arquitetura de Estilos** e **Automação de Tarefas (Build)**.

Este repositório resolve o problema de estruturar páginas complexas sem frameworks pesados, provando a capacidade de construir interfaces modernas e responsivas utilizando a tríade fundamental da web (HTML, CSS e JS) potencializada por ferramentas de desenvolvimento.

> **Resultados de Performance:** "O workflow automatizado lidou eficientemente com a alta carga de imagens de fundo (backgrounds) e elementos sobrepostos. A compressão otimizou drasticamente o Largest Contentful Paint (LCP) das imagens de alta resolução (Hero e sessões de filmes), deixando o carregamento da aplicação 3x mais rápido."
 
## 🖼️ Demonstração Visual



## 🛠️ Tecnologias Utilizadas

A stack baseia-se em performance e otimização de código estático:

* **[HTML5](https://developer.mozilla.org/pt-BR/docs/Web/HTML):** Estrutura semântica e acessível da página.
* **[SASS (SCSS)](https://sass-lang.com/):** Pré-processador CSS utilizado para criar variáveis, aninhamentos e modularizar a estilização (Metodologia BEM).
* **[JavaScript (Vanilla)](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript):** Lógica de interatividade sem dependência de bibliotecas externas.
* **[Gulp](https://gulpjs.com/):** Task Runner configurado para compilar o SASS, minificar o CSS, ofuscar o JavaScript e comprimir as imagens para o diretório de distribuição (`/dist`).

## ✨ Funcionalidades

A aplicação possui interatividades chaves replicadas da plataforma original:

1.  **Header Dinâmico:** O menu de navegação altera sua opacidade/cor de fundo ao detectar o evento de *scroll* do usuário.
2.  **Sistema de Abas (Tabs):** Alternância fluida entre as seções de filmes, séries e exclusividades sem recarregar a página.
3.  **FAQ Interativo (Accordion):** Seção de Perguntas Frequentes expansível utilizando manipulação direta de classes no DOM.
4.  **Layout Responsivo:** Adaptação total para dispositivos móveis, tablets e telas Ultrawide utilizando Media Queries e Flexbox/Grid.

## 📂 Estrutura de Arquivos

A arquitetura do projeto separa claramente o ambiente de desenvolvimento (arquivos brutos) do ambiente de produção (arquivos minificados):

```text
clone_disneyplus/
├── src/                 # Código-fonte (Ambiente de Desenvolvimento)
│   ├── images/          # Imagens em alta resolução
│   ├── scripts/         # Lógica JavaScript (main.js)
│   └── styles/          # Arquivos SASS modularizados
│       ├── _variables.scss
│       ├── _header.scss
│       └── main.scss
├── dist/                # Arquivos otimizados para Produção (Gerados pelo Gulp)
│   ├── images/          # Imagens comprimidas
│   ├── scripts/         # JS minificado/ofuscado
│   └── styles/          # CSS final compilado e minificado
├── index.html           # Marcação principal estruturada
├── gulpfile.js          # Configuração e tarefas do Gulp
├── package.json         # Dependências do Node.js
└── README.md            # Documentação do Projeto
