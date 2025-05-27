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
bash
Copiar
Editar
npm install
3. Configure suas credenciais do Supabase
No arquivo app.js, substitua a URL e a chave anon do seu projeto Supabase:

js
Copiar
Editar
const supabase = createClient(
  'https://SUA-URL.supabase.co',
  'SUA-CHAVE-ANON'
);
4. Rode o servidor
bash
Copiar
Editar
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
Copiar
Editar
{
  "name": "Teclado Gamer",
  "description": "Teclado mecânico RGB",
  "price": 299.90
}
✅ Testando com Insomnia
Baixe o Insomnia: https://insomnia.rest/download

Crie requisições para as rotas acima

Use o método correto e envie o JSON no corpo (para POST/PUT)

👨‍🏫 Professor
Américo Sampaio

📚 Disciplina
Desenvolvimento de Software em Nuvem 

🧑‍💻 Autor
[Carlos Alberto]
RA: [2422750]

---

### Quer que eu crie esse arquivo real no seu projeto?
Posso gerar o conteúdo direto para você salvar no seu projeto como `README.md`.

Quer que eu faça isso agora? Se quiser, me diga o seu nome e RA para completar o rodapé.
