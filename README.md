<!DOCTYPE html>

<html lang="es">

<head>

    <meta charset="UTF-8">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>¿Quieres invitarme una salchipapa?</title>

    <style>

        body {

            text-align: center;

            background-color: pink;

            font-family: Arial, sans-serif;

            overflow: hidden; /* Evita las barras de desplazamiento en la página */

            height: 100vh;

            display: flex;

            flex-direction: column;

            justify-content: center;

            align-items: center;

            margin: 0;

        }



        h1 {

            font-size: 2em;

        }



        .contenedor {

            position: relative;

            width: 1000px; /* Ancho del área donde se moverá el botón */

            height: 1000px; /* Alto del área donde se moverá el botón */

            border: none;

            overflow: hidden; /* Oculta cualquier desbordamiento */

            margin-top: 20px;

        }



        .boton {

            padding: 10px 20px;

            font-size: 18px;

            cursor: pointer;

            border: none;

            border-radius: 5px;

            position: absolute;

        }



        .si {

            background-color: lightblue;

            margin-top: 20px;

            position: relative;

        }



        .no {

            background-color: brown;

            color: white;

            left: 50%; /* Posición inicial centrada */

            top: 50%;

            transform: translate(-50%, -50%);

        }

    </style>

</head>

<body>



    <h1>¿Quieres invitarme una salchipapa?</h1>

    <img src="./artworks-tHcvcBuCrJzDMlU4-CSh9zA-t500x500.jpg" alt="" width="150">



    <div class="contenedor">

        <button class="boton no" id="noBtn">No</button>

    </div>

    <button class="boton si" id="siBtn">Sin duda</button>



    <script>

        const noBtn = document.getElementById("noBtn");

        const siBtn = document.getElementById("siBtn");

        const contenedor = document.querySelector(".contenedor");



        noBtn.addEventListener("mouseover", () => {

            const contWidth = contenedor.clientWidth;

            const contHeight = contenedor.clientHeight;

            const btnWidth = noBtn.clientWidth;

            const btnHeight = noBtn.clientHeight;



            // Calcular posiciones seguras dentro del contenedor

            const maxX = contWidth - btnWidth;

            const maxY = contHeight - btnHeight;



            const x = Math.random() * maxX;

            const y = Math.random() * maxY;



            noBtn.style.left = `${x}px`;

            noBtn.style.top = `${y}px`;

        });



        siBtn.addEventListener("click", () => {

            document.body.innerHTML = "<h1>¡cuando vengas me invitas minion! </h1>";

        });

    </script>



</body>

</html>

