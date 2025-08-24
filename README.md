# Projeto de Gestão de Doações e Realocações

Este é um sistema full-stack projetado para gerenciar doações e realocações de recursos para uma prefeitura. A aplicação é totalmente containerizada usando Docker, facilitando a configuração e a execução em diferentes ambientes.

## Tecnologias Utilizadas

- **Frontend:** React (com Vite)
- **Backend:** Node.js com Express.js
- **Banco de Dados:** PostgreSQL (via Supabase)
- **ORM:** Prisma
- **Containerização:** Docker e Docker Compose
- **Servidor de Produção (Frontend):** Nginx

## Pré-requisitos

Antes de começar, certifique-se de ter as seguintes ferramentas instaladas em sua máquina:

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/) (geralmente vem com o Docker Desktop)
- [Git](https://git-scm.com/)

## Como Executar o Projeto

1.  **Clone o repositório para sua máquina local:**
    ```bash
    git clone <URL_DO_SEU_REPOSITORIO>
    cd <NOME_DA_PASTA_RAIZ>
    ```

2.  **Navegue até a pasta `Integracao`:**
    ```bash
    cd Integracao
    ```

3.  **Crie o arquivo de variáveis de ambiente:**
    Crie um arquivo chamado `.env` na pasta `Integracao`. 

4.  **Preencha o arquivo `.env` com as credenciais válidas:** 

5.  **Suba os containers com Docker Compose:**
    No terminal, dentro da pasta `Integracao`, execute o seguinte comando. O `--build` é importante na primeira vez para construir as imagens do zero.

    ```bash
    docker compose up --build -d
    ```

6.  **Acesse a aplicação:**
    - O **Frontend** estará disponível em: `http://localhost:8004`
    - O **Backend** estará disponível em: `http://localhost:3004`

## Estrutura do Projeto

O projeto está organizado em três diretórios principais no mesmo nível:

-   **/Projetoprefeitura**: Contém todo o código-fonte do frontend em React.
-   **/projeto-prefeitura-backend**: Contém todo o código-fonte do backend em Node.js/Express.
-   **/Integracao**: Contém o arquivo de orquestração `docker-compose.yml` e o arquivo de ambiente `.env`.

## Comandos Úteis do Docker

-   **Parar os containers:**
    ```bash
    docker compose down
    ```

-   **Verificar os logs de um serviço (ex: backend):**
    ```bash
    docker logs projeto-prefeitura-backend
    ```

-   **Verificar os logs do frontend:**
    ```bash
    docker logs projetoprefeitura
    ```

-   **Verificar o status dos containers:**
    ```bash
    docker compose ps
    ```
