# API de Autenticação com JWT em Laravel

Esta é uma API simples construída em Laravel 8 que permite registro de usuários, login e logout utilizando autenticação JWT (JSON Web Token).

## Funcionalidades

- Registro de usuários
- Login e geração de token JWT
- Logout (invalidação do token)
- Acesso a informações do usuário autenticado

## Pré-requisitos

Antes de começar, você precisa ter instalado:

- PHP (>= 7.3)
- Composer
- Laravel (>= 8.x)
- Um banco de dados (MySQL, SQLite, etc.)

## Instalação

### 1. Clonar o Repositório

Clone o repositório para sua máquina local:

```
git clone https://github.com/seuusuario/seurepositorio.git
cd seurepositorio
```

### 2. Instalar Dependências

```
composer install
```

### 3. Configurar o Ambiente

```
cp .env.example .env
```

Edite o arquivo .env para configurar o banco de dados e outras variáveis de ambiente:

```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=seubancodedados
DB_USERNAME=seuusuario
DB_PASSWORD=suasenha

APP_KEY=base64:gerar-uma-chave-aqui
APP_DEBUG=true
```

### 4. Gerar a Chave da Aplicação

```
php artisan key:generate
```

### 5. Migrar o Banco de Dados

```
php artisan migrate
```

### 6. Instalar o JWT Auth

```
composer require tymon/jwt-auth
```

Publique o arquivo de configuração:

```
php artisan vendor:publish --provider="Tymon\JWTAuth\JWTAuthServiceProvider"
```

### 7. Configurar o JWT

Adicione o JWT_SECRET ao seu arquivo .env

```
JWT_SECRET=geraruma-chave-aqui
```

Gere a chave do JWT:

```
php artisan jwt:secret
```

### 8. Iniciar o Servidor

```
php artisan serve
```