📌 To-Do List (PHP + MySQL + AJAX + Bootstrap)

Este é um sistema simples de lista de tarefas que permite:

✅ Cadastrar novas tarefas (título e descrição)

📋 Listar todas as tarefas

🔄 Alterar status (Em andamento / Concluído)

❌ Excluir tarefas

O sistema utiliza PHP + PDO, MySQL/MariaDB, AJAX (fetch) e Bootstrap 5.
Layout inspirado no AdminLTE.

🚀 Tecnologias

PHP 7.4+ ou 8.x

MySQL/MariaDB

Bootstrap 5

JavaScript (AJAX via Fetch API)

📂 Estrutura do Projeto
todo-php-mysql/
├── index.php          # Página principal (UI + endpoints AJAX)
├── db.php             # Conexão PDO e criação automática do banco/tabela
├── .gitignore
├── assets/
│   ├── css/
│   │   └── custom.css # Estilos adicionais
│   └── js/
│       └── app.js     # Lógica AJAX (criar/listar/atualizar/excluir)
└── todo_app.sql       # Script SQL para importar banco/tabela manualmente

🗄️ Banco de Dados

O projeto cria automaticamente o banco todo_app e a tabela tasks caso não existam.
Mas também fornecemos o script SQL (todo_app.sql) caso queira importar manualmente pelo phpMyAdmin.

CREATE TABLE `tasks` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `title` varchar(255) NOT NULL,
  `description` text DEFAULT NULL,
  `is_done` tinyint(1) NOT NULL DEFAULT 0,
  `created_at` timestamp NOT NULL DEFAULT current_timestamp(),
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

⚙️ Instalação

Extraia a pasta todo-php-mysql no diretório do seu servidor local:

XAMPP → htdocs/

Wamp → www/

Laragon → www/

Configure as credenciais do banco no arquivo db.php:

$dbHost = '127.0.0.1';
$dbUser = 'root';
$dbPass = '';
$dbName = 'todo_app';


Importe o arquivo todo_app.sql via phpMyAdmin (opcional, se não quiser deixar o PHP criar automaticamente).

Inicie o servidor Apache/MySQL.

Acesse no navegador:

http://localhost/todo-php-mysql/index.php

🎯 Funcionalidades

Nova Tarefa → formulário para título + descrição.

Minhas Tarefas → lista com ID, título, descrição, data de criação e status.

Status:

Em andamento → quando criada.

Concluído → ao clicar em Concluir ou via seletor.

Ações:

🔄 Alterar status (botão ou seletor).

❌ Excluir tarefa.

📸 Demonstração (prints sugeridos)

Formulário de criação

Lista de tarefas com status

Alteração de status

Exclusão de tarefas

📦 Entrega

Suba este projeto para um repositório público no GitHub.

Poste o link do repositório no comentário particular da atividade.

Prepare a apresentação mostrando:

Estrutura do código

Fluxo do sistema

Prints ou vídeo do funcionamento
