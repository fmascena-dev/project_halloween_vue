# Halloween Party 2025 🎃

Este é um projeto de landing page para uma festa de Halloween, desenvolvido com Vue.js 3, Vite e Tailwind CSS. A página apresenta informações sobre o evento, inspirações de fantasias, e um formulário para confirmação de presença.

- Link do Figma:
  - [Figma do Halloween](figma.com/design/65ZsiKa1v6k7uUukIy89H7/halloween?node-id=1-2&p=f&t=nyt3cMlSngYrCbFw-0)

## ✨ Features

- **Header dinâmico:** Apresenta o título da festa e botões de ação.
- **Detalhes do Evento:** Seção com informações sobre data, hora, local e atrações.
- **Inspirações de Fantasias:** Mostra uma galeria de fantasias para inspirar os convidados.
- **Concurso de Fantasias:** Informa sobre um concurso de fantasias com premiação.
- **Formulário de Confirmação de Presença:** Permite que os convidados confirmem presença, informem o número de acompanhantes e a fantasia que irão usar.
- **Design Temático:** Interface com tema de Halloween, utilizando cores e imagens personalizadas.

## 🚀 Tecnologias Utilizadas

- **Vue.js 3:** Framework progressivo para construção de interfaces de usuário.
- **Vite:** Ferramenta de build moderna e rápida para desenvolvimento web.
- **TypeScript:** Superset de JavaScript que adiciona tipagem estática.
- **Tailwind CSS:** Framework CSS utilitário para estilização rápida e customizável.
- **VeeValidate & Zod:** Para validação de formulários.
- **Lucide Vue Next:** Ícones para a interface.
- **Sass:** Pré-processador CSS para estilização avançada.

## 🏁 Getting Started

Siga as instruções abaixo para configurar e executar o projeto em seu ambiente de desenvolvimento local.

### Pré-requisitos

- [Node.js](https://nodejs.org/en/) (versão ^20.19.0 || >=22.12.0)
- [npm](https://www.npmjs.com/) (geralmente vem com o Node.js)

### Instalação

1. Clone o repositório:

    ```bash
    git clone https://github.com/seu-usuario/halloween_vue.git
    ```

2. Navegue até o diretório do projeto:

    ```bash
    cd project_halloween_vue
    ```

3. Instale as dependências:

    ```bash
    npm install
    ```

### Executando o Projeto

Para iniciar o servidor de desenvolvimento com hot-reload, execute:

```bash
npm run dev
```

O projeto estará disponível em `http://localhost:5173`.

## 📜 Available Scripts

- `npm run dev`: Inicia o servidor de desenvolvimento.
- `npm run build`: Compila e minifica o projeto para produção.
- `npm run preview`: Inicia um servidor local para visualizar a build de produção.
- `npm run type-check`: Realiza a checagem de tipos do TypeScript.
- `npm run format`: Formata o código com o Prettier.

## 📂 Estrutura do Projeto

```bash
.
├── public/               # Arquivos estáticos
├── src/
│   ├── assets/           # Imagens, fontes, etc.
│   ├── components/       # Componentes Vue
│   │   ├── Cards/
│   │   ├── models/
│   │   └── ui/
│   ├── lib/              # Funções utilitárias
│   ├── styles/           # Estilos globais
│   ├── App.vue           # Componente principal
│   └── main.ts           # Ponto de entrada da aplicação
├── .gitignore
├── index.html
├── package.json
├── README.md
└── vite.config.ts
```
