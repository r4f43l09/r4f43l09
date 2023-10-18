import React, { useState } from 'react';

function MeuComponente() {
  // Defina um estado usando o hook useState
  const [valor, setValor] = useState(0);

  // Função para aumentar o valor
  const aumentarValor = () => {
    setValor(valor + 1);
  };

  return (
    <div>
      <p>Valor: {valor}</p>
      <button onClick={aumentarValor}>Aumentar Valor</button>
    </div>
  );
}

export default MeuComponente;
