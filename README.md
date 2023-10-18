const express = require('express');
const app = express();
const port = 8080;

// Middleware para permitir o uso de JSON nas requisições POST
app.use(express.json());

// Rota para lidar com requisições GET
app.get('/', (req, res) => {
  res.send('Rota GET: Olá, mundo!');
});

// Rota para lidar com requisições POST
app.post('/', (req, res) => {
  // Você pode acessar os dados do corpo da requisição POST assim: req.body
  console.log('Dados recebidos no POST:', req.body);
  res.send('Rota POST: Dados recebidos com sucesso!');
});

// Inicie o servidor na porta 8080
app.listen(port, () => {
  console.log(`Servidor rodando na porta ${port}`);
});
