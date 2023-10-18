// minhaFuncao.js
function retornaMensagem() {
  return "Olá, esta é a mensagem da minha função!";
}

export default retornaMensagem;

import React from 'react';
import retornaMensagem from './minhapasta/minhaFuncao';

function App() {
  const mensagem = retornaMensagem();

  return (
    <div>
      <h1>{mensagem}</h1>
    </div>
  );
}

export default App;
