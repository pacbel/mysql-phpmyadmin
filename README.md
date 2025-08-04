# MySQL Docker Setup

Configuração Docker para MySQL com PHPMyAdmin e usuários adicionais pré-configurados.

## 🚀 Quick Start

1. Clone o repositório:
```bash
git clone <seu-repo>
cd <nome-do-repo>
```

2. Copie o arquivo de ambiente:
```bash
cp .env.example .env
```

3. Edite o arquivo `.env` com suas configurações:
```bash
nano .env
```

4. Execute:
```bash
docker-compose up -d
```

## 📋 Serviços

- **MySQL**: Porta 3306
- **PHPMyAdmin**: http://localhost:8080

## 🔧 Configuração

### Variáveis de Ambiente (.env)
- `MYSQL_ROOT_PASSWORD`: Senha do usuário root
- `MYSQL_DATABASE`: Nome do banco principal
- `MYSQL_USER`: Usuário principal da aplicação
- `MYSQL_PASSWORD`: Senha do usuário principal

## 📁 Estrutura
```
.
├── docker-compose.yml      # Configuração dos serviços
├── .env.example           # Exemplo de variáveis
└── mysql-config/          # Configurações customizadas
```

## 🗄️ Dados Persistentes
Os dados do MySQL são salvos no volume `mysql_data`.

Para resetar completamente:
```bash
docker-compose down -v
docker-compose up -d
```

## 🔒 Segurança
- Altere todas as senhas antes de usar em produção
- Use senhas fortes
- Configure firewall adequadamente