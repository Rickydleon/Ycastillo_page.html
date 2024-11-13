<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Un Viaje de Momentos Especiales</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
            color: #333;
            margin: 0;
            padding: 0;
            text-align: center;
        }
        h1 {
            color: #333;
            margin-top: 20px;
            font-size: 28px;
        }
        h2 {
            color: #e60073;
            font-size: 36px;
            margin-top: 10px;
        }
        p {
            width: 80%;
            margin: 0 auto;
            font-size: 18px;
            line-height: 1.6;
        }
        .question {
            font-size: 24px;
            color: #4a4a4a;
            margin-top: 30px;
        }
        .instructions {
            font-size: 14px;
            color: #777;
            margin-top: 10px;
        }
        .buttons {
            margin-top: 20px;
        }
        .buttons button {
            background-color: #333;
            color: white;
            border: none;
            padding: 10px 20px;
            font-size: 18px;
            border-radius: 5px;
            cursor: pointer;
            margin: 10px;
        }
        .buttons button:hover {
            background-color: #555;
        }
    </style>
    <script>
        function showMemory1() {
            document.getElementById("initialText").style.display = "none";
            document.getElementById("memory1").style.display = "block";
        }

        function showQuestion1() {
            document.getElementById("memory1").style.display = "none";
            document.getElementById("question1").style.display = "block";
        }

        function showQuestion2() {
            document.getElementById("question1").style.display = "none";
            document.getElementById("question2").style.display = "block";
        }

        function showNervous() {
            document.getElementById("question2").style.display = "none";
            document.getElementById("nervous").style.display = "block";
        }

        function revealFinalQuestion() {
            document.getElementById("nervous").style.display = "none";
            document.getElementById("finalQuestion").style.display = "block";
        }

        function positiveResponse() {
            alert('¡Sabía que dirías que sí! 😊 Aquí comienza nuestro siguiente capítulo.');
        }

        function extraLoveResponse() {
            alert('¡Esa respuesta me encanta! 💖 Cada día estoy más feliz de tenerte en mi vida.');
        }

        function playfulResponse() {
            alert('Esa es una respuesta con truco… pero me gusta cómo suena 😉');
        }

        function excitedResponse() {
            alert('Sabía que sentías lo mismo. ¡Estoy muy emocionado! 😊');
        }
    </script>
</head>
<body>
    <h2>Yaviela, mi vida</h2>
    <h1>Quiero que me prestes atención...</h1>
    <p id="initialText">Toca el botón cuando estés lista para comenzar nuestro viaje.</p>
    
    <button onclick="showMemory1()" style="background-color: #4a90e2; color: white; padding: 10px 25px; border: none; font-size: 18px; border-radius: 5px; cursor: pointer; margin-top: 20px;">
        Comenzar el viaje
    </button>

    <div id="memory1" style="display: none;">
        <p class="question">🤭 No tuve tiempo...</p>
        <p>No tuve tiempo de estar a tu lado como quería, pero aún así me encantas. Cada día que pasa te siento más cerca, entonces lo he pensado y quiero hacerte una pregunta.</p>
        <button onclick="showQuestion1()">Siguiente</button>
        <p class="instructions">Toca "Siguiente" para continuar.</p>
    </div>

    <div id="question1" style="display: none;">
        <p class="question">¿Me quieres?</p>
        <div class="buttons">
            <button onclick="positiveResponse()">¡Muchísimo!</button>
            <button onclick="extraLoveResponse()">Con todo mi corazón</button>
            <button onclick="playfulResponse()">¿Eso se pregunta? Claro que sí!</button>
        </div>
        <p class="instructions">Selecciona una respuesta para continuar.</p>
    </div>

    <div id="question2" style="display: none;">
        <p class="question">¿Me extrañas?</p>
        <div class="buttons">
            <button onclick="excitedResponse()">¡Cada segundo!</button>
            <button onclick="extraLoveResponse()">Más de lo que imaginas</button>
            <button onclick="positiveResponse()">Demasiado, te extraño siempre</button>
        </div>
        <button onclick="showNervous()" style="margin-top: 20px;">Siguiente</button>
        <p class="instructions">Selecciona una respuesta y luego toca "Siguiente".</p>
    </div>

    <div id="nervous" style="display: none;">
        <p class="question">😳 Estoy nervioso...</p>
        <p>No suelo ponerme así, pero tú tienes algo especial que me hace sentir así. Ahora sí, tengo algo importante que preguntarte.</p>
        <button onclick="revealFinalQuestion()">Dímelo ya</button>
        <p class="instructions">Toca "Dímelo ya" para ver la pregunta final.</p>
    </div>

    <div id="finalQuestion" style="display: none;">
        <p class="question">¿Quieres ser mi novia?</p>
        <p>Responde con sinceridad y sin presiones… pero quiero saber si te gustaría dar este paso conmigo.</p>
        <div class="buttons">
            <button onclick="positiveResponse()">Sí, claro que sí</button>
            <button onclick="extraLoveResponse()">No estaba segura, pero ahora… ¡Sí!</button>
            <button onclick="playfulResponse()">¿Por qué no? ¡Me encantan los riesgos! 😜</button>
            <button onclick="positiveResponse()">Depende… ¿Vas a invitarme a cenar primero? 😆</button>
            <button onclick="positiveResponse()">Solo como amigos, pero con cariño</button>
        </div>
        <p class="instructions">Selecciona una respuesta para completar tu viaje.</p>
    </div>
</body>
</html>
