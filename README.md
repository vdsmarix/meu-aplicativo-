<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Aplicativo Simples</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
    }
    
    .container {
      max-width: 800px;
      margin: 40px auto;
      padding: 20px;
      background-color: #f9f9f9;
      border: 1px solid #ddd;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    }
    
    .titulo {
      text-align: center;
      margin-bottom: 20px;
    }
    
    .formulario {
      display: flex;
      flex-direction: column;
      align-items: center;
    }
    
    .formulario input[type="text"] {
      width: 100%;
      height: 30px;
      font-size: 18px;
      padding: 10px;
      border: 1px solid #ccc;
      margin-bottom: 20px;
    }
    
    .formulario button {
      width: 200px;
      height: 30px;
      font-size: 18px;
      background-color: #4CAF50;
      color: #fff;
      border: none;
      cursor: pointer;
    }
    
    .formulario button:hover {
      background-color: #3e8e41;
    }
    
    @media (max-width: 600px) {
      .container {
        margin: 20px;
      }
      .formulario input[type="text"] {
        width: 90%;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <h1 class="titulo">Bem-vindo!</h1>
    <div class="formulario">
      <input type="text" id="nome" placeholder="Digite seu nome">
      <button id="botao">Enviar</button>
      <p id="mensagem"></p>
    </div>
  </div>
  
  <script>
    document.getElementById("botao").addEventListener("click", function() {
      var nome = document.getElementById("nome").value;
      if (nome !== "") {
        document.querySelector(".titulo").textContent = `Olá, ${nome}!`;
        document.getElementById("mensagem").textContent = "Seja bem-vindo!";
      } else {
        alert("Por favor, insira seu nome.");
      }
    });
  </script>
</body>
</html>
