# Portfólio de Desenvolvedor JavaScript

Este é um projeto de portfólio de desenvolvedor JavaScript, criado para exibir informações profissionais como habilidades, idiomas, projetos de portfólio e experiência profissional. O conteúdo do portfólio é dinâmico, carregado a partir de um arquivo JSON.

## Funcionalidades

*   Exibição de informações de perfil (foto, nome, cargo, localização, contato).
*   Seção de Habilidades (Soft Skills e Hard Skills com logos).
*   Seção de Idiomas.
*   Seção de Portfólio com links para projetos.
*   Seção de Experiência Profissional.
*   Design responsivo (via CSS).

## Tecnologias Utilizadas

*   **HTML5**: Estrutura da página.
*   **CSS3**: Estilização (incluindo `normalize.css` para reset de CSS e Google Fonts).
*   **JavaScript ES6+**: Lógica para carregamento e manipulação de dados, e funcionalidade de acordeão.

## Estrutura do Projeto

*   `index.html`: A página principal do portfólio.
*   `assets/css/`: Contém todos os arquivos de estilo CSS.
*   `assets/fonts/`: Contém fontes customizadas.
*   `assets/img/`: Contém imagens e ícones utilizados no site.
*   `assets/js/`:
    *   `acordeon.js`: Lógica para a funcionalidade de acordeão das seções.
    *   `api.js`: Responsável por buscar os dados do perfil de um arquivo JSON remoto.
    *   `main.js`: Lógica principal para processar os dados do perfil e injetá-los no HTML.
*   `data/profile.json`: Arquivo JSON que serve como fonte de dados para o portfólio.

## Como Configurar e Rodar Localmente

Para configurar e rodar este projeto em sua máquina local, siga os passos abaixo:

1.  **Clone o repositório:**
    ```bash
    git clone https://github.com/cristian-souza/js-developer-portfolio.git
    ```
2.  **Navegue até o diretório do projeto:**
    ```bash
    cd js-developer-portfolio
    ```
3.  **Abra o arquivo `index.html` em seu navegador:**
    Você pode simplesmente clicar duas vezes no arquivo `index.html` ou usar uma extensão de servidor local (como "Live Server" para VS Code) para ter um ambiente de desenvolvimento mais robusto.

## Personalização

Os dados do portfólio são carregados a partir de um arquivo JSON remoto, atualmente configurado em `assets/js/api.js`. Se você deseja usar um arquivo `profile.json` local ou de outra URL, você precisará editar o `api.js`:

1.  **Edite `assets/js/api.js`:**
    Altere a variável `url` para apontar para o seu próprio arquivo `profile.json` (seja local ou remoto).

    ```javascript
    async function fetchProfileData() {
        const url = "SEU_CAMINHO_PARA_PROFILE.JSON"; // Ex: "./data/profile.json" para local
        const response = await fetch(url);
        const profileData = await response.json();
        return profileData;
    }
    ```

2.  **Atualize `data/profile.json`:**
    Certifique-se de que a estrutura do seu arquivo `profile.json` siga o formato esperado (verifique o `data/profile.json` existente como exemplo) para que o `main.js` possa renderizar as informações corretamente.

## Créditos

*   Projeto baseado no template de portfólio da Digital Innovation One (DIO).
*   Desenvolvido por Cristian Souza.
