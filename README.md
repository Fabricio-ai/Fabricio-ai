<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Vamos viajar o mundo e casar na Roma</title>
  <style>
    body {
      text-align: center;
    }

    .title {
      font-size: 24px;
      margin-top: 20px;
    }

    .box {
      border: 2px solid #000;
      padding: 10px;
      text-align: center;
      width: 300px;
      margin: 10px;
      cursor: pointer;
      position: absolute;
    }

    #sim {
      top: 100px;
      left: 50px;
    }

    #nao {
      top: 200px;
      left: 50px;
    }

    #mensagem2 {
      top: 200px;
      left: 50px;
      display: none;
    }

    #mensagem3 {
      top: 200px;
      left: 50px;
      display: none;
    }
  </style>
</head>
<body>
  <div class="title">Vamos viajar o mundo e casar na Roma</div>
  <div class="box" id="sim" onclick="redirecionar()">
    <p>Sim</p>
  </div>
  <div class="box" id="nao" onclick="mostrarMensagem()">
    <p>Não</p>
  </div>
  <div class="box" id="mensagem2" onclick="mostrarMensagem3()">
    <p>Tem certeza?</p>
  </div>
  <div class="box" id="mensagem3" onclick="escaparCaixa()">
    <p>Então me pegue!</p>
  </div>

  <script>
    function redirecionar() {
      window.location.href = "https://i.pinimg.com/originals/25/6a/31/256a319f34cfc8afa1ff27e181b27a0d.gif";
    }

    function mostrarMensagem() {
      var naoCaixa = document.getElementById('nao');
      var mensagem2Caixa = document.getElementById('mensagem2');

      naoCaixa.style.display = 'none';
      mensagem2Caixa.style.display = 'block';
    }

    function mostrarMensagem3() {
      var caixa = document.getElementById('mensagem2');
      var maxX = window.innerWidth - caixa.clientWidth;
      var maxY = window.innerHeight - caixa.clientHeight;
      var newX = Math.random() * maxX;
      var newY = Math.random() * maxY;

      caixa.style.left = newX + 'px';
      caixa.style.top = newY + 'px';

      caixa.style.display = 'block';
    }

    function escaparCaixa() {
      var caixa = document.getElementById('mensagem3');
      var maxX = window.innerWidth - caixa.clientWidth;
      var maxY = window.innerHeight - caixa.clientHeight;
      var newX = Math.random() * maxX;
      var newY = Math.random() * maxY;

      caixa.style.left = newX + 'px';
      caixa.style.top = newY + 'px';
    }
  </script>
</body>
</html>

