# PDV-3 - Sistema de Ponto de Venda Empresarial

Sistema de Ponto de Venda (PDV) avançado desenvolvido para empresas, com foco em desempenho, segurança e escalabilidade. Versão 3.0 com melhorias significativas de arquitetura e funcionalidades.

![Versão](https://img.shields.io/badge/versão-3.0.0-blue)
![Licença](https://img.shields.io/badge/licença-MIT-green)
![Status](https://img.shields.io/badge/status-produção-brightgreen)

## Funcionalidades

- **Dashboard Analítico**: Visualização em tempo real de vendas e métricas
- **Gestão Empresarial**: Produtos, estoque, clientes e fornecedores
- **Vendas Avançadas**: Promoções, descontos e múltiplas formas de pagamento
- **Relatórios Customizados**: Exportação em diversos formatos
- **Segurança Reforçada**: Proteção contra ataques e validação de dados
- **Desempenho Otimizado**: Compressão e cache para operação mais rápida

## Melhorias na Versão 3.0

- Arquitetura modular com routers Express para melhor organização
- Implementação de middlewares de segurança (helmet, rate limiting)
- Compressão de resposta para melhor desempenho
- Tratamento global de erros
- Logging estruturado de requisições
- CI/CD com GitHub Actions
- ESLint para qualidade de código
- Atualizações de dependências e otimização de segurança

## Tecnologias Utilizadas

- **Frontend**: HTML5, CSS3, JavaScript ES6+
- **Backend**: Node.js, Express 4
- **Banco de Dados**: PostgreSQL 14+
- **Segurança**: Helmet, bcryptjs, JWT, Express Rate Limit
- **DevOps**: GitHub Actions, Render Blueprint

## Início Rápido

### Pré-requisitos

- Node.js 14.x ou superior
- PostgreSQL 14.x ou superior
- Git

### Instalação Local

1. Clone o repositório:
   ```bash
   git clone https://github.com/jesusmjunior/pdv-3.git
   cd pdv-3
   ```

2. Instale as dependências:
   ```bash
   npm ci
   ```

3. Configure as variáveis de ambiente:
   ```bash
   cp .env.example .env
   # Edite o arquivo .env com suas configurações
   ```

4. Inicialize o banco de dados:
   ```bash
   npm run setup-db
   ```

5. Inicie o servidor em modo desenvolvimento:
   ```bash
   npm run dev
   ```

6. Acesse a aplicação em [http://localhost:3000](http://localhost:3000)

### Credenciais padrão:
- **Usuário**: admin
- **Senha**: admin

## Estrutura do Projeto

```
/
├── .github/                # Configurações do GitHub
│   ├── workflows/          # GitHub Actions para CI/CD
│   └── ISSUE_TEMPLATE/     # Templates para issues
├── api/                    # Backend API
│   ├── controllers/        # Controladores da API
│   ├── models/             # Modelos de dados
│   └── index.js            # Configuração Express
├── scripts/                # Scripts utilitários
│   └── setup-db.js         # Configuração do banco de dados
├── src/                    # Frontend
│   ├── css/                # Estilos CSS
│   ├── img/                # Imagens e ícones
│   ├── js/                 # JavaScript
│   │   ├── components/     # Componentes reutilizáveis
│   │   ├── core/           # Funções principais
│   │   └── modules/        # Módulos específicos
│   └── pages/              # Páginas HTML
├── .eslintrc.json         # Configuração do ESLint
├── .npmrc                 # Configuração do npm
├── .gitignore             # Arquivos ignorados pelo Git
├── package.json           # Dependências e scripts
└── render.yaml            # Configuração do Render
```

## Segurança

Esta versão inclui múltiplas camadas de segurança:

- **Helmet**: Proteção contra ataques web comuns
- **Rate Limiting**: Proteção contra força bruta e DDoS
- **bcryptjs**: Hashing seguro de senhas
- **JWT**: Autenticação com tempo de expiração
- **Sanitização de Entrada**: Validação e escape de dados
- **CORS Configurado**: Controle de acesso cross-origin

## Deploy

O projeto está configurado para deploy automático na Render.com usando o arquivo `render.yaml` e GitHub Actions para CI/CD.

1. As alterações no branch `main` são automaticamente testadas
2. O linting é executado para garantir qualidade do código
3. O deploy é acionado automaticamente após a aprovação de CI

## Contribuindo

Contribuições são bem-vindas! Para contribuir:

1. Fork este repositório
2. Crie uma branch para sua feature (`git checkout -b feature/nova-funcionalidade`)
3. Commit suas mudanças (`git commit -m 'Add: nova funcionalidade'`)
4. Push para a branch (`git push origin feature/nova-funcionalidade`)
5. Abra um Pull Request

## Licença

Este projeto é licenciado sob a [MIT License](LICENSE).