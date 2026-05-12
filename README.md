<div align="center">

# ⚓ Anchor Desk

**🇧🇷 Português** | **🇺🇸 English**

---

> 🇧🇷 Remodificação de um site de iates com sistema de mensagens e painel administrativo, desenvolvido com TypeScript, SCSS e Docker.

> 🇺🇸 A yacht website redesign featuring a contact messaging system and admin panel, built with TypeScript, SCSS and Docker.

---

![GitHub Actions](https://img.shields.io/github/actions/workflow/status/CarlosNeto-dev/anchor-desk/deploy.yml?branch=main&label=deploy&style=flat-square)
![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-deployed-brightgreen?style=flat-square)
![TypeScript](https://img.shields.io/badge/TypeScript-5.x-blue?style=flat-square&logo=typescript)
![SCSS](https://img.shields.io/badge/SCSS-compiled-pink?style=flat-square&logo=sass)
![Docker](https://img.shields.io/badge/Docker-ready-2496ED?style=flat-square&logo=docker)

</div>

---

## 🇧🇷 Português

### 📋 Sumário

- [Sobre o Projeto](#-sobre-o-projeto)
- [Funcionalidades](#-funcionalidades)
- [Tecnologias](#-tecnologias)
- [Estrutura de Pastas](#-estrutura-de-pastas)
- [Pré-requisitos](#-pré-requisitos)
- [Como Rodar](#-como-rodar)
- [CI/CD e Deploy](#-cicd-e-deploy)
- [Páginas](#-páginas)

---

### 🚢 Sobre o Projeto

O **Anchor Desk** é uma remodificação de um site de iates existente, com a adição de funcionalidades JavaScript para gerenciamento de mensagens. O projeto permite que visitantes enviem mensagens pelo formulário de contato, e que administradores autorizados visualizem todas as mensagens recebidas em um painel protegido.

---

### ✨ Funcionalidades

- 📬 **Formulário de contato** — visitantes podem enviar mensagens com nome, e-mail e texto
- 🔐 **Painel administrativo** — área protegida com autenticação por e-mail e senha
- 📋 **Listagem de mensagens** — tabela dinâmica com todas as mensagens recebidas
- 🚀 **Deploy automático** — GitHub Actions compila e publica no GitHub Pages a cada push

---

### 🛠 Tecnologias

| Tecnologia | Uso |
|------------|-----|
| **TypeScript** | Lógica e interatividade das páginas |
| **SCSS** | Estilização com variáveis e aninhamento |
| **Docker** | Ambiente de desenvolvimento isolado |
| **GitHub Actions** | Pipeline de CI/CD |
| **GitHub Pages** | Hospedagem do site |
| **live-server** | Servidor local com live reload |
| **Node.js** | Compilação de SCSS e TypeScript |

---

### 📁 Estrutura de Pastas

```
anchor-desk/
│
├── 📁 .github/
│   └── 📁 workflows/
│       └── 📄 deploy.yml          # Pipeline de CI/CD
│
├── 📁 src/                        # Código fonte (editável)
│   ├── 📁 scss/                   # Arquivos de estilo
│   │   └── 📄 style.scss
│   └── 📁 ts/                     # Arquivos TypeScript
│       └── 📄 main.ts
│
├── 📁 dist/                       # Arquivos compilados (gerado automaticamente)
│   ├── 📁 css/                    # CSS compilado do SCSS
│   ├── 📁 js/                     # JS compilado do TypeScript
│   └── 📁 pages/                  # Páginas HTML
│       ├── 📄 index.html
│       ├── 📄 contato.html
│       ├── 📄 admin.html
│       └── 📄 mensagens.html
│
├── 📄 Dockerfile                  # Imagem Node para build e servidor
├── 📄 docker-compose.yml          # Orquestração dos containers
├── 📄 package.json                # Dependências e scripts
├── 📄 tsconfig.json               # Configuração do TypeScript
├── 📄 .gitignore
└── 📄 .dockerignore
```

> 💡 A pasta `src/` é onde você edita o código. A pasta `dist/` é gerada automaticamente pelo processo de build — nunca edite ela manualmente.

---

### ✅ Pré-requisitos

Você só precisa ter instalado na sua máquina:

- [Docker Desktop](https://www.docker.com/products/docker-desktop/)
- [VS Code](https://code.visualstudio.com/)

Não é necessário ter Node.js, npm, ou qualquer outra ferramenta instalada localmente.

---

### 🚀 Como Rodar

**1. Clone o repositório**

```bash
git clone https://github.com/CarlosNeto-dev/anchor-desk.git
cd anchor-desk
```

**2. Suba os containers**

```bash
docker compose up --build
```

**3. Acesse no navegador**

```
http://localhost:8080
```

> O **live-server** recarrega o navegador automaticamente sempre que você salvar um arquivo em `src/`.

**Para parar os containers:**

```bash
docker compose down
```

---

### ⚙️ Scripts disponíveis

| Script | O que faz |
|--------|-----------|
| `npm run dev` | Compila SCSS + TypeScript em watch mode e sobe o servidor |
| `npm run build` | Compila SCSS + TypeScript uma única vez (usado no CI/CD) |
| `npm run watch:scss` | Compila apenas o SCSS em watch mode |
| `npm run watch:ts` | Compila apenas o TypeScript em watch mode |
| `npm run server` | Sobe apenas o live-server |

---

### 🔄 CI/CD e Deploy

O projeto usa **GitHub Actions** para automatizar o deploy. O fluxo funciona assim:

```
Você faz push na branch main
          ↓
GitHub Actions é disparado automaticamente
          ↓
Instala as dependências (npm install)
          ↓
Compila SCSS → CSS e TypeScript → JS (npm run build)
          ↓
Publica o conteúdo de dist/ na branch gh-pages
          ↓
GitHub Pages serve o site automaticamente
```

O arquivo de configuração está em [`.github/workflows/deploy.yml`](.github/workflows/deploy.yml).

> ⚠️ A pasta `dist/` **não é versionada** no repositório. Ela é gerada automaticamente pelo GitHub Actions a cada push.

---

### 📄 Páginas

| Página | Caminho | Descrição |
|--------|---------|-----------|
| 🏠 Home | `index.html` | Página principal do site de iates |
| 📬 Contato | `contato.html` | Formulário para envio de mensagens |
| 🔐 Admin | `admin.html` | Login para área administrativa |
| 📋 Mensagens | `mensagens.html` | Listagem de mensagens recebidas |

---

---

## 🇺🇸 English

### 📋 Table of Contents

- [About the Project](#-about-the-project)
- [Features](#-features)
- [Technologies](#-technologies)
- [Folder Structure](#-folder-structure)
- [Prerequisites](#-prerequisites)
- [How to Run](#-how-to-run)
- [CI/CD and Deploy](#-cicd-and-deploy)
- [Pages](#-pages)

---

### 🚢 About the Project

**Anchor Desk** is a redesign of an existing yacht website, enhanced with JavaScript features for message management. Visitors can send messages through the contact form, and authorized administrators can view all received messages in a protected panel.

---

### ✨ Features

- 📬 **Contact form** — visitors can send messages with name, email and text
- 🔐 **Admin panel** — protected area with email and password authentication
- 📋 **Message listing** — dynamic table with all received messages
- 🚀 **Automatic deploy** — GitHub Actions compiles and publishes to GitHub Pages on every push

---

### 🛠 Technologies

| Technology | Usage |
|------------|-------|
| **TypeScript** | Page logic and interactivity |
| **SCSS** | Styling with variables and nesting |
| **Docker** | Isolated development environment |
| **GitHub Actions** | CI/CD pipeline |
| **GitHub Pages** | Site hosting |
| **live-server** | Local server with live reload |
| **Node.js** | SCSS and TypeScript compilation |

---

### 📁 Folder Structure

```
anchor-desk/
│
├── 📁 .github/
│   └── 📁 workflows/
│       └── 📄 deploy.yml          # CI/CD pipeline
│
├── 📁 src/                        # Source code (editable)
│   ├── 📁 scss/                   # Style files
│   │   └── 📄 style.scss
│   └── 📁 ts/                     # TypeScript files
│       └── 📄 main.ts
│
├── 📁 dist/                       # Compiled files (auto-generated)
│   ├── 📁 css/                    # CSS compiled from SCSS
│   ├── 📁 js/                     # JS compiled from TypeScript
│   └── 📁 pages/                  # HTML pages
│       ├── 📄 index.html
│       ├── 📄 contato.html
│       ├── 📄 admin.html
│       └── 📄 mensagens.html
│
├── 📄 Dockerfile                  # Node image for build and server
├── 📄 docker-compose.yml          # Container orchestration
├── 📄 package.json                # Dependencies and scripts
├── 📄 tsconfig.json               # TypeScript configuration
├── 📄 .gitignore
└── 📄 .dockerignore
```

> 💡 The `src/` folder is where you edit your code. The `dist/` folder is auto-generated by the build process — never edit it manually.

---

### ✅ Prerequisites

You only need to have installed on your machine:

- [Docker Desktop](https://www.docker.com/products/docker-desktop/)
- [VS Code](https://code.visualstudio.com/)

No need to have Node.js, npm, or any other tool installed locally.

---

### 🚀 How to Run

**1. Clone the repository**

```bash
git clone https://github.com/CarlosNeto-dev/anchor-desk.git
cd anchor-desk
```

**2. Start the containers**

```bash
docker compose up --build
```

**3. Open in your browser**

```
http://localhost:8080
```

> The **live-server** automatically reloads the browser whenever you save a file in `src/`.

**To stop the containers:**

```bash
docker compose down
```

---

### ⚙️ Available Scripts

| Script | What it does |
|--------|--------------|
| `npm run dev` | Compiles SCSS + TypeScript in watch mode and starts the server |
| `npm run build` | Compiles SCSS + TypeScript once (used in CI/CD) |
| `npm run watch:scss` | Compiles only SCSS in watch mode |
| `npm run watch:ts` | Compiles only TypeScript in watch mode |
| `npm run server` | Starts only the live-server |

---

### 🔄 CI/CD and Deploy

The project uses **GitHub Actions** to automate deployment. The flow works like this:

```
You push to the main branch
          ↓
GitHub Actions is triggered automatically
          ↓
Installs dependencies (npm install)
          ↓
Compiles SCSS → CSS and TypeScript → JS (npm run build)
          ↓
Publishes dist/ content to the gh-pages branch
          ↓
GitHub Pages serves the site automatically
```

The configuration file is at [`.github/workflows/deploy.yml`](.github/workflows/deploy.yml).

> ⚠️ The `dist/` folder is **not versioned** in the repository. It is automatically generated by GitHub Actions on every push.

---

### 📄 Pages

| Page | Path | Description |
|------|------|-------------|
| 🏠 Home | `index.html` | Main yacht website page |
| 📬 Contact | `contato.html` | Form for sending messages |
| 🔐 Admin | `admin.html` | Login for the admin area |
| 📋 Messages | `mensagens.html` | Listing of received messages |

---

<div align="center">

Made with ❤️ by [CarlosNeto-dev](https://github.com/CarlosNeto-dev)

</div>