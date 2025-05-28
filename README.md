# 🧩 Supabase + Node.js API

Projeto criado para fins educacionais na disciplina **Desenvolvimento de Software em Nuvem**, com o objetivo de integrar um banco de dados Supabase com uma aplicação back-end em Node.js.

---

## 📌 Objetivo

- Criar uma tabela de produtos no Supabase
- Desenvolver uma API REST com Node.js usando Express
- Implementar as rotas GET, POST, PUT e DELETE

---

## ⚙️ Tecnologias

- [Node.js]
- [Express]
- [Supabase]
- [Insomnia] – para testar a API
- Middleware: `cors`, `morgan`, `body-parser`

---

## 🏗️ Configuração do Projeto

### 1. Clone o repositório

```bash
git clone https://github.com/americosampaio-dev/supabaseBack.git
cd supabaseBack
2. Instale as dependências

npm install
3. Configure suas credenciais do Supabase
No arquivo app.js, substitua a URL e a chave anon do seu projeto Supabase:

js
const supabase = createClient(
  'https://SUA-URL.supabase.co',
  'SUA-CHAVE-ANON'
);
4. Rode o servidor
node app.js

🔌 Rotas da API
Método	Rota	Ação
GET	/products	Lista todos os produtos
GET	/products/:id	Busca produto por ID
POST	/products	Cria um novo produto
PUT	/products/:id	Atualiza um produto existente
DELETE	/products/:id	Deleta um produto

📝 Exemplo de corpo (POST/PUT):
json
{
  "name": "Teclado Gamer",
  "description": "Teclado mecânico RGB",
  "price": 299.90
}
✅ Testando com Insomnia
Baixe o Insomnia: https://insomnia.rest/download

Crie requisições para as rotas acima

Use o método correto e envie o JSON no corpo (para POST/PUT)```

---

´´´bash

# Deploy Backend Node.js na AWS EC2

Este guia descreve como configurar e rodar um backend Node.js utilizando o Express e Supabase em uma instância EC2 da AWS.

---

## Pré-requisitos

- Conta AWS com instância EC2 configurada
- Par de chaves (.pem) para acesso SSH
- IAM Role já criado (opcional)
- Repositório backend no GitHub
- O backend deve ter um `app.js` como ponto de entrada

---

## 1. Criar Instância EC2

- Tipo: Amazon Linux 2 ou Ubuntu Server
- Tipo de instância: t2.micro (free tier)
- Associar par de chaves existente
- Associar IAM Role (se necessário)
- Configurar o grupo de segurança com:
  - Porta **22** (SSH)
  - Porta **3000** (HTTP da sua aplicação)

---

## 2. Acessar a Instância via SSH

No terminal AWS:
```bash
3. Instalar NVM (Node Version Manager)
sudo su
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
. ~/.nvm/nvm.sh

4. Instalar Node.js (versão LTS)
nvm install --lts

5. Instalar Git
sudo yum install -y git  Amazon Linux

sudo apt install git -y  Para Ubuntu

Verifique a instalação:
git --version

6. Clonar o Repositório do Projeto
git clone https://github.com/seuusuario/seurepositorio.git
cd "seurepositorio"

7. Inicializar e Instalar Dependências
npm init -y
npm install express@4
npm install @supabase/supabase-js
npm install cors
npm install morgan

8. Iniciar a Aplicação
node app.js
A aplicação deve estar rodando na porta 3000.

Acesse no navegador:
http://<IP-PÚBLICO-DA-EC2>:3000

---
Dica Extra: Executar o servidor em segundo plano
Para manter sua aplicação rodando após fechar o terminal:

npm install -g pm2
pm2 start app.js

---
