# Post-Get-com-comentarios
aula de Met. Científica

´´´
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Comentários</title>
</head>
<style>
    body{
        background-image: linear-gradient(125deg, blue, purple);
        background-size:auto;
        background-repeat: no-repeat;
        text-align: center;

        width: 100vw;
        height: 100vh;
    }

    h1{
        color: white;
        text-align: center;
        font-family: Arial, Helvetica, sans-serif;
    }

    h2{
        font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
        color: white;
        margin-left: 2%;
    }

    form{
        margin-left: 40%;
        max-width: 500px;
        display: flex;
        flex-flow: column;
        text-align: center;
    }

    .nome{
        background-color: rgba(0, 0, 0, 0);
        border: none;
        color: white;
        border-bottom: 1px solid white;
    }

    .comentario{
        background-color: rgba(0, 0, 0, 0.5);
        border: none;
        color: white;
        border-radius: 5px;
    }

    button{
        background-color: rgba(119, 119, 119, 0.637);
        color: white;
        border-radius: 5px;
        border: none;
    }

    ul{
        background-color: rgba(0, 0, 0, 0.5);
        justify-content: center;
        color: white;
        max-width: 50%;
        margin-left: 25%;
    }

    li{
        list-style: none;
    }
</style>
<body>
    <h1 class = "titulo">Deixe seu Comentário</h1>
    <form method="POST">
        <input class = "nome" type="text" name="name" placeholder="Seu nome" required>
        <br>
        <textarea class ="comentario" name="comment" placeholder="Seu comentário" required></textarea>
        <br>
        <button type="submit">Enviar</button>
    </form>
    
    <h2>Comentários</h2>
    <ul>
        {% for name, comment in comments %}
            <li><strong>{{ name }}</strong>: {{ comment }}</li>
        {% endfor %}
    </ul>
</body>
</html>
´´´
