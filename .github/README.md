# CollabHubBR - Poll/Enquete System

![GitHub License](https://img.shields.io/github/license/CollabHubBR/poll-system?labelColor=101010)

<!-- ![GitHub Actions Workflow Status](https://img.shields.io/github/actions/workflow/status/CollabHubBR/poll-system/testing.yml?style=flat&labelColor=101010) -->

Este repositório contém o código-fonte do **Microsserviço de Enquetes** do **CollabHubBR**, a plataforma brasileira de coordenação e organização de projetos de código-aberto. Desenvolvido em **PHP** com o framework **Laravel**, este serviço é responsável por permitir a criação de enquetes por parte dos administradores e garantir que cada usuário possa votar apenas uma vez por enquete.

A persistência dos dados é realizada com o **PostgreSQL**, e o serviço é executado com **Docker Compose** para facilitar o desenvolvimento e a implantação.

---

## 🔧 Stack Utilizada

![PHP](https://img.shields.io/badge/PHP-777BB4.svg?style=for-the-badge&logo=php&logoColor=white)

![Laravel](https://img.shields.io/badge/Laravel-FF2D20.svg?style=for-the-badge&logo=laravel&logoColor=white)

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

![Composer](https://img.shields.io/badge/Composer-885630.svg?style=for-the-badge&logo=composer&logoColor=white)

![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088ff?style=for-the-badge&logo=github-actions&logoColor=fff)

---

## 🧠 Funcionalidades

-   Criação de enquetes por administradores de projetos
-   Voto único por usuário
-   Relacionamento entre projetos e enquetes
-   Integração com microsserviços de usuários para validação de identidade
-   Baseado em autenticação com tokens JWT (via middleware Laravel)

---

## 📁 Estrutura de Pastas

```bash
.
├── app/
│   ├── Http/
│   ├── Models/
│   ├── Services/
│   └── ...
├── database/
│   └── migrations/
├── routes/
│   └── api.php
├── docker/
│   └── postgres/  # scripts e init do banco
├── .env
├── docker-compose.yml
├── composer.json
└── README.md
```

---

## ▶️ Instruções para Rodar Localmente

### 1. Clone o repositório

```bash
git clone https://github.com/CollabHubBR/poll-system.git
cd poll-system
```

### 2. Configure o arquivo `.env`

Copie o exemplo e edite com suas credenciais:

```bash
cp .env.example .env
```

### 3. Suba o ambiente com Docker Compose

```bash
docker-compose up -d --build
```

### 4. Acesse o container e instale as dependências

```bash
docker exec -it poll-system-app bash
composer install
php artisan key:generate
php artisan migrate
```

---

## 🧪 Executando os Testes

```bash
php artisan test
```

---

## ✅ To-Do List

Confira a [To-Do List aqui](https://github.com/CollabHubBR/poll-system/blob/main/.github/TODO.md)

---

## 🤝 Contribuindo

Antes de contribuir, é **altamente recomendado** ler os seguintes documentos:

-   [Código de Conduta](https://github.com/CollabHubBR/.github/blob/main/CODE_OF_CONDUCT.md)
-   [Guia de Contribuição](https://github.com/CollabHubBR/.github/blob/main/CONTRIBUTING.md)
-   [Política de Segurança](https://github.com/CollabHubBR/.github/blob/main/SECURITY.md)
-   [Suporte](https://github.com/CollabHubBR/.github/blob/main/SUPPORT.md)

---

## 📄 Licença

Distribuído sob a licença [MIT](https://choosealicense.com/licenses/mit/). Consulte o arquivo `LICENSE` para mais informações.
