# 🎬 Disney+ Clone - Frontend Landing Page

![Status](https://img.shields.io/badge/Status-Finalizado-green)
![SASS](https://img.shields.io/badge/Style-SASS%2FSCSS-hotpink?logo=sass&logoColor=white)
![Gulp](https://img.shields.io/badge/Build-Gulp.js-red?logo=gulp&logoColor=white)
![JavaScript](https://img.shields.io/badge/Logic-Vanilla_JS-yellow?logo=javascript&logoColor=white)
![Responsive](https://img.shields.io/badge/Design-Responsive-blue)

> Uma réplica de alta fidelidade (Pixel Perfect) da interface de apresentação do Disney+, demonstrando domínio sobre estruturação de layout complexo e arquitetura de estilos.

## 🎯 Motivação e Propósito

A capacidade de replicar interfaces complexas "pixel por pixel" é uma habilidade valiosa no mercado. O propósito deste projeto foi criar uma **Landing Page completa**, saindo da teoria e enfrentando desafios reais de CSS e layout.

O projeto resolve o desafio de estruturar uma página com múltiplas seções interativas (Abas, Accordions, Grids) mantendo o código limpo, modular e performático através de um pipeline de build automatizado.

## 🖼️ Demonstração Visual

https://clone-disneyplus-ruby-kappa.vercel.app


## 🛠️ Tecnologias Utilizadas

A stack foi escolhida para simular um ambiente de desenvolvimento profissional:

* **[HTML5 Semântico](https://developer.mozilla.org/pt-BR/docs/Web/HTML):** Estruturação de conteúdo focada em SEO e acessibilidade.
* **[SASS (SCSS)](https://sass-lang.com/):** Pré-processador CSS utilizado para:
    * **Arquitetura:** Separação de arquivos por componentes (`_header.scss`, `_hero.scss`, `_faq.scss`).
    * **Variáveis:** Gestão de paleta de cores e tipografia.
    * **Mixins:** Automação de media queries para responsividade.
* **[JavaScript (ES6+)](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript):** Lógica *Vanilla* (sem frameworks) para manipulação de classes e eventos do DOM.
* **[Gulp.js](https://gulpjs.com/):** Task Runner para:
    * Compilação do SASS.
    * Compressão de Imagens.
    * Minificação de Scripts (Uglify).
    * Watch mode para desenvolvimento.

## ✨ Funcionalidades

O projeto vai além do visual estático, implementando interações essenciais:

1.  **Header Dinâmico:** A barra de navegação torna-se visível/transparente baseado no scroll da página (manipulação de evento `window.onscroll`).
2.  **Sistema de Abas (Tabs):** Seção "Assista do seu jeito" com alternância de conteúdo e classes ativas via JS.
3.  **FAQ Interativo (Accordion):** Seção de perguntas frequentes com lógica de abrir/fechar respostas.
4.  **Layout Responsivo:** Adaptação fluida desde dispositivos móveis até telas ultrawide.

## 📦 Instalação e Configuração

O projeto utiliza Node.js para gerenciar as dependências de automação.

### Pré-requisitos
* **Node.js** e **NPM** instalados.
* **Git** instalado.

### Passo a Passo

1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/DouglassenG/clone_disneyplus.git](https://github.com/DouglassenG/clone_disneyplus.git)
    ```

2.  **Acesse o diretório:**
    ```bash
    cd clone_disneyplus
    ```

3.  **Instale as dependências:**
    ```bash
    npm install
    ```

4.  **Execute o Build (Dev Mode):**
    Para iniciar o projeto e assistir alterações:
    ```bash
    npm run build
    # ou
    gulp
    ```

## 💻 Uso e Exemplos

### Estrutura do Código
A organização reflete a separação entre código fonte e distribuição:

```text
clone_disneyplus/
├── src/
│   ├── styles
