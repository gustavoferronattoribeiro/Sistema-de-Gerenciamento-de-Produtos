# Sistema de Gerenciamento de Produtos

Sistema web completo para gerenciamento de produtos (CRUD), desenvolvido com **React** no frontend, **Node.js + Express** no backend e **MySQL** como banco de dados.

**Desenvolvido por:** Gustavo

---

## Tecnologias Utilizadas

- **Frontend:** React 18, React Router DOM, Axios
- **Backend:** Node.js, Express, mysql2, CORS
- **Banco de Dados:** MySQL

---

## Como Rodar o Projeto

### Pré-requisitos

- [Node.js](https://nodejs.org/) instalado (versão 16 ou superior)
- [MySQL](https://dev.mysql.com/downloads/) instalado e rodando

### 1. Configurar o Banco de Dados

1. Abra o MySQL Workbench ou terminal do MySQL.
2. Execute o arquivo `database.sql` que está na raiz do projeto:

```sql
source caminho/para/database.sql;
```

Ou importe pelo MySQL Workbench: **Server > Data Import > Import from Self-Contained File**, selecione o arquivo `database.sql` e clique em **Start Import**.

### 2. Configurar o Backend

1. Acesse a pasta do backend:
```bash
cd backend
```

2. Instale as dependências:
```bash
npm install
```

3. **Importante:** Se necessário, ajuste as credenciais do banco de dados no arquivo `db.js`:
```javascript
const connection = mysql.createConnection({
  host: 'localhost',
  user: 'root',
  password: '',       // Altere para sua senha do MySQL
  database: 'sistema_produtos'
});
```

4. Inicie o servidor:
```bash
npm start
```

O backend rodará em `http://localhost:3001`.

### 3. Configurar o Frontend

1. Em outro terminal, acesse a pasta do frontend:
```bash
cd frontend
```

2. Instale as dependências:
```bash
npm install
```

3. Inicie a aplicação:
```bash
npm start
```

O frontend abrirá automaticamente em `http://localhost:3000`.

---

## Funcionalidades

- **Listagem de produtos** com paginação
- **Cadastro** de novos produtos
- **Edição** de produtos existentes
- **Exclusão** de produtos com confirmação
- **Visualização detalhada** de cada produto
- **Validação de dados** no frontend e backend
- **Mensagens de erro** e feedback visual para o usuário

---

## Estrutura do Projeto

```
├── backend/
│   ├── routes/
│   │   └── produtoRoutes.js    # Rotas da API (CRUD)
│   ├── db.js                    # Conexão com MySQL
│   ├── server.js                # Servidor Express
│   └── package.json
├── frontend/
│   ├── public/
│   │   └── index.html
│   ├── src/
│   │   ├── pages/
│   │   │   ├── ListaProdutos.js     # Tela de listagem
│   │   │   ├── CadastroProduto.js   # Tela de cadastro
│   │   │   ├── EditarProduto.js     # Tela de edição
│   │   │   └── DetalheProduto.js    # Tela de detalhes
│   │   ├── services/
│   │   │   └── api.js               # Configuração do Axios
│   │   ├── App.js                   # Componente principal
│   │   ├── index.js                 # Entrada da aplicação
│   │   └── index.css                # Estilos globais
│   └── package.json
├── database.sql                 # Script SQL do banco de dados
└── README.md
```
