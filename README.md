# 📱 Mobile Product Manager (Desafio Técnico)

> Aplicativo de gerenciamento de produtos e clientes desenvolvido com **React Native (Expo)** e **SQLite**, focado em arquitetura *Offline-first*.

![Badge em Desenvolvimento](http://img.shields.io/static/v1?label=STATUS&message=EM%20DESENVOLVIMENTO&color=GREEN&style=for-the-badge)
![Badge React Native](https://img.shields.io/badge/React_Native-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Badge TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![Badge SQLite](https://img.shields.io/badge/SQLite-07405E?style=for-the-badge&logo=sqlite&logoColor=white)

---

## 💻 Sobre o Projeto

Este projeto foi desenvolvido como parte de um teste técnico para demonstrar competências em desenvolvimento mobile moderno. O objetivo principal é criar uma aplicação capaz de gerenciar **Clientes** e **Produtos** de forma relacional, persistindo os dados localmente no dispositivo do usuário.

A aplicação utiliza uma abordagem **Offline-first**, garantindo que o usuário possa cadastrar e visualizar dados mesmo sem conexão com a internet, utilizando o poder do banco de dados SQLite embarcado.

---

## 🚀 Tecnologias Utilizadas

O projeto foi construído utilizando as seguintes tecnologias e bibliotecas:

- **[React Native](https://reactnative.dev/)** (via **[Expo SDK](https://expo.dev/)**): Framework principal.
- **[TypeScript](https://www.typescriptlang.org/)**: Para tipagem estática e segurança do código.
- **[Drizzle ORM](https://orm.drizzle.team/)**: ORM moderno para gerenciamento do banco de dados e queries type-safe.
- **[Expo SQLite](https://docs.expo.dev/versions/latest/sdk/sqlite/)**: Driver nativo para banco de dados local.
- **[Expo Router](https://docs.expo.dev/router/introduction/)**: Sistema de navegação baseado em arquivos (File-based routing).
- **[React Native Safe Area Context](https://docs.expo.dev/versions/latest/sdk/safe-area-context/)**: Para lidar com entalhes e áreas seguras de diferentes dispositivos.

---

## ✨ Funcionalidades

- [x] **Listagem de Clientes:** Visualização de clientes cadastrados (carregados via banco de dados).
- [x] **Cadastro de Produtos:** Formulário para inserção de novos produtos.
- [x] **Relacionamento de Dados:** Vínculo obrigatório entre um Produto e um Cliente existente.
- [x] **Persistência Local:** Todos os dados são salvos em um arquivo `.db` local via SQLite.
- [x] **Interface Responsiva:** Layout adaptado para diferentes tamanhos de tela.

---

## 📂 Estrutura do Projeto

A organização de pastas segue os padrões recomendados para projetos Expo Router e Drizzle:

src/ ├── app/ # Telas e Rotas (Expo Router) │ ├── (tabs)/ # Navegação em abas │ └── _layout.tsx # Layout global ├── components/ # Componentes reutilizáveis (UI) │ └── TelaProdutos.tsx # Tela principal de cadastro ├── database/ # Camada de Dados │ ├── schemas/ # Definição das tabelas (Drizzle) │ └── index.ts # Conexão com o banco └── drizzle/ # Arquivos de migração SQL
---

## 🔧 Como rodar o projeto localmente

Para rodar este projeto, você precisará ter o **Node.js** instalado e o ambiente móvel configurado (Android Studio ou Xcode).

### 1. Clone o repositório
```bash
git clone [https://github.com/SEU-USUARIO/NOME-DO-REPO.git](https://github.com/rlxrcao/mobile-product-manager.git)
cd NOME-DO-REPO

2. Instale as dependências
Bash

npm install
3. Gere o build nativo (Prebuild)
Como este projeto utiliza código nativo (SQLite), é necessário rodar o comando de prebuild antes de iniciar:

Bash

npx expo prebuild
4. Execute a aplicação
Bash

# Para Android
npx expo run:android

# Para iOS (apenas Mac)
npx expo run:ios
🗄️ Banco de Dados (Drizzle)
O projeto utiliza Drizzle ORM para gerenciar o esquema do banco.

As tabelas estão definidas em src/database/schemas/.

As migrações (.sql) estão na pasta drizzle/.

Caso precise gerar novas migrações após alterar o esquema:

Bash

npx drizzle-kit generate