# lista-de-alunos
#Lista de Alunos
Esta aplicação permite que o usuário adicione alunos e suas notas em uma lista que é armazenada localmente usando a API Web Storage. A aplicação consiste em uma página web simples, que é adequada para execução em smartphones.

#Interfaces
A aplicação possui duas interfaces:

Formulário: O usuário pode adicionar um aluno à lista inserindo o nome do aluno e suas notas. O formulário inclui os seguintes campos:

Nome: campo de texto obrigatório para inserir o nome do aluno.
Nota 1: campo numérico obrigatório para inserir a primeira nota do aluno. Aceita valores entre 0 e 10 com incrementos de 0,1.
Nota 2: campo numérico obrigatório para inserir a segunda nota do aluno. Aceita valores entre 0 e 10 com incrementos de 0,1.
Adicionar Aluno: botão para adicionar o aluno à lista.
Lista: A lista de alunos adicionados é exibida abaixo do formulário. A lista é atualizada automaticamente quando um novo aluno é adicionado.

Armazenamento
Os dados da lista de alunos são armazenados localmente usando a API Web Storage. A aplicação não compartilha dados entre usuários e não requer um servidor com banco de dados.

Código Fonte
Segue abaixo o código fonte em HTML, CSS e JavaScript da aplicação:

HTML:
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>Lista de Alunos</title>
    <link rel="stylesheet" type="text/css" href="style.css">
  </head>
  <body>
    <div class="container">
      <h1>Lista de Alunos</h1>
      <form>
        <label for="nome">Nome:</label>
        <input type="text" id="nome" required>
        <br>
        <label for="nota1">Nota 1:</label>
        <input type="number" id="nota1" step="0.1" min="0" max="10" required>
        <br>
        <label for="nota2">Nota 2:</label>
        <input type="number" id="nota2" step="0.1" min="0" max="10" required>
        <br>
        <input type="submit" value="Adicionar Aluno">
      </form>
      <ul id="lista">
      </ul>
    </div>
    <script src="app.js"></script>
  </body>
</html>
CSS:
* {
  box-sizing: border-box;
  font-family: Arial, sans-serif;
  font-size: 16px;
}

.container {
  max-width: 600px;
  margin: 0 auto;
  padding: 20px;
}

h1 {
  text-align: center;
}

form {
  display: flex;
  flex-direction: column;
}

label {
  margin-bottom: 10px;
}

input[type="text"],
input[type="number"] {
  padding: 5px;
  margin-bottom: 20px;
}

input[type="submit"] {
  background-color: #4CAF50;
  color: white;
  padding: 10px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  margin-top: 10px;
}

input[type="submit"]:hover {
  background-color: #3e8e41
