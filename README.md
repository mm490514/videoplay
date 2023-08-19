# README do Projeto

Este repositório contém o código-fonte de um projeto em PHP baseado na arquitetura MVC (Model-View-Controller) que gerencia vídeos. O projeto utiliza o framework Slim para roteamento e injeção de dependências, e foi projetado para lidar com operações relacionadas a vídeos, como criar, editar, excluir e listar vídeos.

## Como Começar

Para começar com este projeto, siga os passos abaixo:

### Pré-requisitos

- PHP 7.2 ou posterior
- Extensão SQLite para PHP
- Composer (Gerenciador de Dependências para PHP)

### Instalação

1. Clone este repositório para a sua máquina local:

   ```bash
   git clone https://github.com/seu-nome-de-usuário/seu-projeto.git
   ```

2. Navegue até o diretório do projeto:

   ```bash
   cd seu-projeto
   ```

3. Instale as dependências do projeto usando o Composer:

   ```bash
   composer install
   ```

4. Configure o caminho do banco de dados:

   Abra o arquivo `index.php` e defina o caminho correto para o banco de dados SQLite:

   ```php
   $dbPath = __DIR__ . '/../banco.sqlite';
   $pdo = new PDO("sqlite:$dbPath");
   ```

5. Configure as rotas:

   Defina as rotas no arquivo `config/routes.php` para mapear os métodos HTTP e os caminhos para as classes de controladores correspondentes.

6. Inicie a aplicação:

   Você pode usar um servidor local (como o servidor embutido do PHP) para executar a aplicação:

   ```bash
   php -S localhost:8000
   ```

## Uso

Depois que a aplicação estiver em execução, você pode acessar as diferentes funcionalidades por meio de suas respectivas rotas:

- Criar um novo vídeo: `/videos/novo`
- Editar um vídeo: `/videos/editar/{id}`
- Excluir um vídeo: `/videos/excluir/{id}`
- Listar todos os vídeos: `/videos`
- Detalhes do vídeo: `/videos/{id}`

### Autenticação

A aplicação utiliza um mecanismo simples de autenticação baseado em sessões. Se um usuário não estiver logado, ele será redirecionado para a página de login (`/login`) antes de acessar outras rotas.

## Contribuições

Contribuições para este projeto são bem-vindas! Se encontrar problemas ou tiver sugestões para melhorias, por favor, crie uma nova issue ou envie um pull request.
