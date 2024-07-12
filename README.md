# Containerizando uma Aplicação Node.js

## Pré-requisitos

- [Docker Desktop](https://www.docker.com/products/docker-desktop)
- Cliente git (linha de comando ou GUI)

## Passo a Passo

### 1. Obtenha a Aplicação de Exemplo

Clone o repositório de exemplo:

```sh
git clone https://github.com/docker/docker-nodejs-sample
```

### 2. Inicialize os Recursos Docker

No diretório `docker-nodejs-sample`, execute:

```sh
docker init
```

Responda aos prompts:

- Plataforma: Node
- Versão do Node: 18.0.0
- Gerenciador de pacotes: npm
- Comando para iniciar: node src/index.js
- Porta: 3000

### 3. Estrutura do Projeto

Você deverá ver os seguintes arquivos e diretórios:

```
├── docker-nodejs-sample/
│   ├── spec/
│   ├── src/
│   ├── .dockerignore
│   ├── .gitignore
│   ├── compose.yaml
│   ├── Dockerfile
│   ├── package-lock.json
│   ├── package.json
│   └── README.md
```

### 4. Execute a Aplicação

No diretório `docker-nodejs-sample`, execute:

```sh
docker compose up --build
```

Abra o navegador em `http://localhost:3000` para ver a aplicação.

Para parar a aplicação, pressione `ctrl+c` no terminal.