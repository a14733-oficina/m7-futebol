# ⚽ Gestão de Futebol - Sistema de Inventário de Jogadores e Clubes

Site-->https://a14733-oficina.infinityfree.me/m7_futebol/index.php

Este projeto consiste numa aplicação web desenvolvida em **PHP** para a gestão de uma base de dados de futebol. O sistema permite listar, adicionar, editar e remover jogadores, bem como filtrar a informação por clubes e países.

O foco principal deste trabalho foi a transposição de dados reais do portal **ZeroZero** para uma estrutura de base de dados relacional, garantindo a integridade e a correta visualização da informação.

---

## 📋 Índice
- [Objetivos](#-objetivos)
- [Pesquisa e Dados (ZeroZero)](#-pesquisa-e-dados-zerozero)
- [Estrutura da Base de Dados](#-estrutura-da-base-de-dados)
- [Funcionalidades](#-funcionalidades)
- [Tecnologias Utilizadas](#-tecnologias-utilizadas)
- [Instalação e Configuração](#-instalação-e-configuração)

---

## 🎯 Objetivos
- Desenvolver uma aplicação CRUD (Create, Read, Update, Delete) funcional.
- Implementar uma ligação segura à base de dados utilizando **PDO (PHP Data Objects)**.
- Organizar a informação de forma intuitiva, permitindo filtros avançados por clube e nacionalidade.
- Garantir que a interface seja responsiva e amigável para o utilizador.

---

## 🔍 Pesquisa e Dados (ZeroZero)
A base de dados deste projeto foi populada com informações reais extraídas do [ZeroZero.pt](https://www.zerozero.pt). A pesquisa focou-se em:
- **Clubes**: Nome oficial, estádio e país de origem.
- **Jogadores**: Nome, idade, posição  e número.

A transposição destes dados exigiu um cuidado especial na normalização, garantindo que cada jogador estivesse corretamente associado ao seu respetivo clube através de chaves estrangeiras (`id_clube`).

---

## 🗄️ Estrutura da Base de Dados
A base de dados `if0_40156192_inventario` é composta por duas tabelas principais relacionadas:

### Tabela `Clube`
| Coluna | Tipo | Descrição |
| :--- | :--- | :--- |
| `id_clube` | INT (PK) | Identificador único do clube |
| `nomeclube` | VARCHAR | Nome oficial do clube |
| `estadio` | VARCHAR | Nome do estádio principal |
| `pais` | VARCHAR | País de origem do clube |

### Tabela `Jogador`
| Coluna | Tipo | Descrição |
| :--- | :--- | :--- |
| `id_jogador` | INT (PK) | Identificador único do jogador |
| `NumAtleta` | INT | Número oficial do atleta |
| `NomeJogador` | VARCHAR | Nome completo do jogador |
| `Idade` | INT | Idade do atleta |
| `Posicao` | VARCHAR | Posição (ex: GR, DC, MC, PL) |
| `id_clube` | INT (FK) | Ligação à tabela Clube |

---

## 🚀 Funcionalidades
- **Página Inicial**: Visão geral e menu de navegação.
- **Listagem Geral**: Visualização de todos os jogadores com indicação do clube atual.
- **Gestão de Jogadores**:
  - Adicionar novos atletas com validação de dados.
  - Atualizar informações de jogadores existentes.
  - Remover registos com confirmação de segurança.
- **Filtros Especializados**:
  - **Por Clube**: Lista jogadores de um clube específico, destacando o nome do estádio.
  - **Por País**: Agrupa a informação com base na nacionalidade dos clubes.

---

## 🛠️ Tecnologias Utilizadas
- **Frontend**: HTML5, CSS3 (estilização personalizada).
- **Backend**: PHP 8.x.
- **Base de Dados**: MySQL / MariaDB.
- **Segurança**: Utilização de `Prepared Statements` (PDO) para prevenir ataques de SQL Injection e `htmlspecialchars` para evitar XSS.

---

## ⚙️ Instalação e Configuração
1. Importe o ficheiro SQL para o seu servidor MySQL.
2. Configure as credenciais de acesso no ficheiro `db.php`:
   ```php
   $host = "seu_host";
   $dbname = "seu_nome_bd";
   $user = "seu_utilizador";
   $pass = "sua_senha";
   ```
3. Certifique-se de que todos os ficheiros (`header.php`, `footer.php`, etc.) estão na mesma diretoria.

---
*Trabalho realizado no âmbito do módulo de Gestão de Bases de Dados.*
