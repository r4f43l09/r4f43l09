const express = require('express');
const app = express();
const port = 8080;

// Rota estática
app.get('/', (req, res) => {
  res.send('Rota estática: Página inicial');
});

// Rota dinâmica com placeholder
app.get('/user/:id', (req, res) => {
  const userId = req.params.id;
  res.send(`Rota dinâmica: Exibindo informações do usuário com ID ${userId}`);
});

// Rota com query parameter
app.get('/search', (req, res) => {
  const query = req.query.q;
  res.send(`Rota com query parameter: Pesquisando por "${query}"`);
});

// Rota 404 para lidar com rotas não definidas
app.use((req, res) => {
  res.status(404).send('Página não encontrada');
});

app.listen(port, () => {
  console.log(`Servidor rodando na porta ${port}`);
});
