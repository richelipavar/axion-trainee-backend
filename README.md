# Teste Técnico Axion/Dex - Backend (Strapi API)

Este é o projeto backend (API Strapi) fornecido e configurado para o teste técnico de trainee da Axion Company.

Ele serve dados para as listas de Pessoas, Comidas e Locais, e gerencia a autenticação de usuários.

## Collections Criadas

*   **People**: Campos `name` (string), `link` (string - URL da imagem)
*   **Food**: Campos `name` (string), `link` (string - URL da imagem)
*   **Places**: Campos `name` (string), `link` (string - URL da imagem)

## Credenciais de Usuário (para teste da API/Frontend)

*   **Usuário:** `axioner@axion.company`
*   **Senha:** `Axioner123`
    *(Este usuário é para login na aplicação frontend. Ele também funciona para o painel de admin do Strapi neste projeto específico).*

## Pré-requisitos

*   Node.js (v14.x ou superior, como especificado no teste. Testado com v18.x e v20.x usando `NODE_OPTIONS`).
*   npm ou yarn

## Configuração e Instalação (Backend)

1.  **Clone o repositório (se ainda não o fez, e se este for o SEU repositório forked/copiado):**
    ```bash
    git clone https://github.com/SEU_USUARIO/axion-trainee-backend-strapi.git
    cd axion-trainee-backend-strapi
    ```

2.  **Instale as dependências:**
    ```bash
    npm install
    ```
    (ou `yarn install`)

3.  **Construa o Painel de Administração (necessário antes do primeiro `develop` ou após certas alterações):**
    ```bash
    npm run build
    ```

4.  **Rodar a API em Modo de Desenvolvimento:**
    ```bash
    # Se estiver usando Node.js v17 ou superior, pode ser necessário:
    NODE_OPTIONS=--openssl-legacy-provider npm run develop

    # Se estiver usando Node.js v14-v16, apenas:
    # npm run develop
    ```
    A API estará disponível em `http://localhost:1337`.
    O painel de administração do Strapi estará em `http://localhost:1337/admin`.

## Estrutura e Configurações Importantes

*   As **definições das Collections** (schemas dos tipos de conteúdo "People", "Food", "Places") são salvas pelo Strapi como arquivos JSON dentro da estrutura de pastas da API. Exemplo: `api/food/models/food.settings.json`
*   As permissões de acesso foram configuradas via painel de admin para os roles "Public" e "Authenticated".
*   Os dados de exemplo (imagens) devem ser colocados na pasta `public/uploads/` deste projeto backend para que os links funcionem.
*   O banco de dados de desenvolvimento é SQLite (arquivo `.tmp/data.db`), que é automaticamente criado/gerenciado pelo Strapi e **não está versionado intencionalmente.**

## Autor (do Setup/Configuração para o Teste)

Richeli Pavarini Mascarenha Link linkdin: https://www.linkedin.com/in/richeli-pavarini/
