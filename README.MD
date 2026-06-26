# ⚽ Gestor de Clubes e Jogadores

Este projeto consiste numa aplicação web desenvolvida em **HTML, CSS e JavaScript**, utilizando **Supabase** como base de dados. O sistema permite gerir jogadores e clubes através de uma interface simples e intuitiva, possibilitando adicionar, editar, visualizar e remover jogadores.

---

# 📋 Índice

* Objetivos
* Estrutura da Base de Dados
* Funcionalidades
* Tecnologias Utilizadas
* Instalação e Configuração

---

# 🎯 Objetivos

* Desenvolver uma aplicação CRUD (Create, Read, Update e Delete).
* Criar uma interface simples e responsiva para gestão de jogadores.
* Integrar uma base de dados remota através do Supabase.
* Facilitar a organização da informação dos clubes e respetivos jogadores.

---

# 🗄️ Estrutura da Base de Dados

A aplicação utiliza duas tabelas relacionadas.

## Tabela `Clube`

| Coluna    | Tipo     | Descrição              |
| :-------- | :------- | :--------------------- |
| id_clube  | INT (PK) | Identificador do clube |
| nomeclube | VARCHAR  | Nome do clube          |
| pais      | VARCHAR  | País do clube          |

## Tabela `Jogador`

| Coluna      | Tipo     | Descrição                |
| :---------- | :------- | :----------------------- |
| id_jogador  | INT (PK) | Identificador do jogador |
| NomeJogador | VARCHAR  | Nome do jogador          |
| Pais        | VARCHAR  | Nacionalidade            |
| Idade       | INT      | Idade                    |
| Posicao     | VARCHAR  | Posição em campo         |
| id_clube    | INT (FK) | Clube ao qual pertence   |

---

# 🚀 Funcionalidades

* Página principal com listagem de clubes e jogadores.
* Adicionar novos jogadores.
* Editar informações dos jogadores através de uma janela modal.
* Eliminar jogadores da base de dados.
* Atualização automática da informação apresentada.
* Interface organizada para facilitar a gestão dos dados.

---

# 🛠️ Tecnologias Utilizadas

* **Frontend:** HTML5, CSS3 e JavaScript.
* **Base de Dados:** Supabase (PostgreSQL).
* **Biblioteca:** Supabase JavaScript SDK.

---

# ⚙️ Instalação e Configuração

1. Faça download do projeto.
2. Crie um projeto no Supabase.
3. Importe os ficheiros SQL fornecidos:

   * `clube_rows.sql`
   * `jogador_rows.sql`
4. Configure no ficheiro `script.js`:

   * URL do projeto Supabase.
   * Chave pública (Anon Key).
5. Abra o ficheiro `index.html` no navegador ou publique-o num servidor web.

---

# 📂 Estrutura do Projeto

```text
m7/
│── index.html
│── style.css
│── script.js
│── clube_rows.sql
│── jogador_rows.sql
│── if0_40156192_futebol_bd.sql
```

---

# 📖 Descrição

Esta aplicação permite gerir uma pequena base de dados de futebol de forma simples e rápida. Através da integração com o Supabase, todas as operações de inserção, edição, consulta e eliminação são realizadas em tempo real, permitindo uma gestão eficiente dos jogadores e respetivos clubes.

---

*Trabalho realizado no âmbito do módulo de Redes e Bases de Dados.*
