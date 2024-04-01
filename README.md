# calculadora-web
uma calculadora feita em html, css e js com referencia em um tutorial do youtuber gustavo neitzke.
### Aqui está o código completo em uma pagina só:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora</title>
    <style>
      * {
  margin: 0;
  padding: 0;
  font-family: Arial, Helvetica, sans-serif;
}
.fundo {
  background-image: #fff;
  color: #fff;
  text-align: center;
}
.calculadora {
  position: relative;
  background-color: rgba(0, 0, 0, 0.8);
  width: 12.2%;
  border-radius: 15px;
  padding: 15px;
  margin: 182px;
  left:650px;
}
.botao {
  width: 50px;
  height: 50px;
  font-size: 25px;
  cursor: pointer;
  margin: 3px;
  background-color: rgb(31, 31, 31);
  border: none;
  color: #fff;
  border-radius: 5px;
}
.botao:hover {
  background-color: black;
}
header {
  background-color: black;
  color: white;
  padding: 30px;
  display: flex;
  justify-content: space-between;
  align-items: center; 
}
footer {
  background-color: black;
  color: white;
  text-align: center;
  padding: 30px 0;
}
#resultado {
  background-color: white;
  width: 214px;
  height: 30px;
  margin: 5px;
  font-size: 25px;
  color: black;
  text-align: right;
  padding: 5px;
  border-radius: 5px;
}
    </style>
    <script>
      function insert(num) {
  var numero = document.getElementById("resultado").innerHTML;
  document.getElementById("resultado").innerHTML = numero + num;
}
function clean() {
  document.getElementById("resultado").innerHTML = "";
}
function back() {
  var resultado = document.getElementById("resultado").innerHTML;
  document.getElementById("resultado").innerHTML = resultado.substring(
    0,
    resultado.length - 1
  );
}
function calcular() {
  var resultado = document.getElementById("resultado").innerHTML;
  if (resultado) {
    document.getElementById("resultado").innerHTML = eval(resultado);
  } else {
    document.getElementById("resultado").innerHTML = "Nada...";
  }
}
    </script>
</head>
<body>
  <header>
    <h1>Calculadora</h1>
  </header>
  <main>
    <div class="fundo">
        <div class="calculadora">
            <p id="resultado"></p>
            <table>
                <tr>
                    <td><button class="botao" onclick="clean()">C</button></td>
                    <td><button class="botao" onclick="back()"><</button></td>
                    <td><button class="botao" onclick="insert('/')">/</button></td>
                    <td><button class="botao" onclick="insert('*')">X</button></td>
                </tr>
                <tr>
                    <td><button class="botao" onclick="insert('7')">7</button></td>
                    <td><button class="botao" onclick="insert('8')">8</button></td>
                    <td><button class="botao" onclick="insert('9')">9</button></td>
                    <td><button class="botao" onclick="insert('-')">-</button></td>
                </tr>
                <tr>
                    <td><button class="botao" onclick="insert('4')">4</button></td>
                    <td><button class="botao" onclick="insert('5')">5</button></td>
                    <td><button class="botao" onclick="insert('6')">6</button></td>
                    <td><button class="botao" onclick="insert('+')">+</button></td>
                </tr>
                <tr>
                    <td><button class="botao" onclick="insert('1')">1</button></td>
                    <td><button class="botao" onclick="insert('2')">2</button></td>
                    <td><button class="botao" onclick="insert('3')">3</button></td>
                    <td rowspan="2"><button class="botao" style="height: 106px;" onclick="calcular()">=</button></td>
                </tr>
                <tr>
                    <td colspan="2"><button class="botao" style="width: 106px;" onclick="insert('0')">0</button></td>
                    <td><button class="botao" onclick="insert('.')">.</button></td>
                </tr>
            </table>
        </div>
    </div>
  </main>
    <footer>
      <p>Feito por Tiago Raulino - 552899</p>
    </footer>
</body>
</html>
```
