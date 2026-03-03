<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Carlos Fonseca: El Juego Definitivo</title>
    <style>
        :root { --rojo: #ce1126; --negro: #000000; --gris: #1a1a1a; --blanco: #ffffff; }
        body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; margin: 0; background: var(--negro); color: var(--blanco); text-align: center; }
        
        .pantalla { display: none; padding: 20px; min-height: 100vh; box-sizing: border-box; }
        .activa { display: block; animation: fadeIn 0.5s; }
        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
        
        .img-juego { width: 100%; max-width: 420px; border: 4px solid var(--rojo); border-radius: 12px; margin: 15px 0; box-shadow: 0 0 20px rgba(206, 17, 38, 0.4); }
        .card { background: var(--gris); padding: 25px; border-radius: 20px; border-top: 6px solid var(--rojo); max-width: 550px; margin: 15px auto; box-shadow: 0 10px 30px rgba(0,0,0,0.5); }
        
        .btn { background: var(--rojo); color: white; border: none; padding: 18px; margin: 10px auto; border-radius: 8px; cursor: pointer; font-weight: bold; width: 90%; max-width: 320px; display: block; text-transform: uppercase; font-size: 16px; transition: 0.3s; }
        .btn:hover { background: #900; transform: translateY(-2px); }
        .btn-volver { background: #333; margin-top: 25px; }

        .opcion-viva { background: #252525; padding: 15px; margin: 12px; border-radius: 10px; cursor: pointer; border: 1.5px solid var(--rojo); font-size: 1.1em; transition: 0.2s; }
        .opcion-viva:hover { background: var(--rojo); color: white; }

        #contenedor-puzzle { display: flex; flex-wrap: wrap; justify-content: center; gap: 12px; margin: 25px 0; }
        .pieza { background: var(--rojo); padding: 15px 20px; border-radius: 8px; cursor: pointer; font-weight: bold; box-shadow: 2px 2px 5px rgba(0,0,0,0.3); }
        #resultado-puzzle { border: 2px dashed var(--rojo); min-height: 60px; padding: 20px; margin: 20px 0; font-size: 1.3em; background: #0a0a0a; border-radius: 10px; color: #ffeb3b; }
    </style>
</head>
<body>

    <div id="menu" class="pantalla activa">
        <h1>COMANDANTE CARLOS FONSECA</h1>
        <img src="https://upload.wikimedia.org/wikipedia/commons/6/6f/Carlos_Fonseca_Amador.jpg" class="img-juego">
        <div class="card">
            <button class="btn" onclick="iniciarTrivia('facil')">🟢 TRIVIA: NIVEL FÁCIL</button>
            <button class="btn" onclick="iniciarTrivia('medio')">🟡 TRIVIA: NIVEL MEDIO</button>
            <button class="btn" onclick="iniciarTrivia('dificil')">🔴 TRIVIA: NIVEL DIFÍCIL</button>
            <button class="btn" onclick="navegar('senderos')">🏔️ SENDEROS DE ZINICA</button>
            <button class="btn" onclick="iniciarPuzzle()">🧩 ROMPECABEZAS</button>
        </div>
    </div>

    <div id="pantalla-trivia" class="pantalla">
        <h2 id="trivia-titulo" style="color:var(--rojo)">Nivel</h2>
        <div class="card">
            <p id="pregunta-texto" style="font-size: 1.3em; margin-bottom: 20px; font-weight: bold;"></p>
            <div id="opciones-contenedor"></div>
        </div>
        <button class="btn btn-volver" onclick="navegar('menu')">VOLVER AL MENÚ</button>
    </div>

    <div id="senderos" class="pantalla">
        <h2>SENDEROS DE LA HISTORIA</h2>
        <img src="https://viva-nicaragua.imgix.net/2020/11/comandante-carlos-fonseca-amador-revolucion.jpg" class="img-juego">
        <div class="card">
            <p id="historia-texto" style="font-size: 1.2em; line-height: 1.5;">Eres un joven colaborador en la montaña de Zinica. Carlos Fonseca te llama y te dice: "La educación es nuestra mejor arma". ¿Qué decides hacer?</p>
            <div id="historia-opciones">
                <button class="btn" onclick="historia(1)">Organizar a los campesinos para leer</button>
                <button class="btn" onclick="historia(2)">Vigilar las rutas contra la guardia</button>
            </div>
        </div>
        <button class="btn btn-volver" onclick="navegar('menu')">SALIR</button>
    </div>

    <div id="rompecabezas" class="pantalla">
        <h2>RECONSTRUYE LA FRASE</h2>
        <div class="card">
            <p>Toca las palabras en orden para completar el mandato de Carlos:</p>
            <div id="contenedor-puzzle"></div>
            <div id="resultado-puzzle"></div>
            <button class="btn" style="background: #2e7d32; display:none;" id="btn-verificar-p" onclick="verificarPuzzle()">VERIFICAR FRASE</button>
            <button class="btn" style="background: #444;" onclick="limpiarPuzzle()">BORRAR Y REINTENTAR</button>
        </div>
        <button class="btn btn-volver" onclick="navegar('menu')">MENÚ</button>
    </div>

    <script>
        // BASE DE DATOS DE PREGUNTAS
        const preguntas = {
            facil: [
                { p: "¿En qué país nació Carlos Fonseca?", o: ["Nicaragua", "Cuba", "Venezuela"], c: 0 },
                { p: "¿En qué ciudad nació?", o: ["Managua", "Matagalpa", "Estelí"], c: 1 },
                { p: "¿Cuáles son los colores de su bandera?", o: ["Azul y Blanco", "Rojo y Negro", "Rojo y Blanco"], c: 1 },
                { p: "¿Qué pedía que le enseñaran a los campesinos?", o: ["A bailar", "A leer", "A cocinar"], c: 1 },
                { p: "¿A qué organización fundó Carlos?", o: ["FSLN", "ONU", "UNESCO"], c: 0 }
            ],
            medio: [
                { p: "¿En qué año nació el Comandante?", o: ["1936", "1950", "1945"], c: 0 },
                { p: "¿Cómo se llamaba su madre?", o: ["Josefa", "Agustina Amador", "Blanca Arauz"], c: 1 },
                { p: "¿Qué profesión tenía Carlos?", o: ["Ingeniero", "Profesor e Intelectual", "Médico"], c: 1 },
                { p: "¿A qué país viajó y escribió un libro sobre ello?", o: ["España", "URSS (Moscú)", "México"], c: 1 },
                { p: "¿Qué prócer nicaragüense rescató en sus escritos?", o: ["Sandino", "Rubén Darío", "Andrés Castro"], c: 0 }
            ],
            dificil: [
                { p: "¿En qué lugar cayó en combate en 1976?", o: ["Zinica (Boca de Piedra)", "Pancasán", "Monimbó"], c: 0 },
                { p: "¿Cómo se llamaba su seudónimo en la lucha?", o: ["Agatón", "Danto", "Modesto"], c: 0 },
                { p: "¿En qué año fundó el FSLN?", o: ["1961", "1979", "1956"], c: 0 },
                { p: "¿En qué instituto estudió su secundaria?", o: ["Inst. Nacional de Matagalpa", "Ramírez Goyena", "La Salle"], c: 0 },
                { p: "¿En qué mes se celebra su aniversario?", o: ["Noviembre", "Julio", "Junio"], c: 0 }
            ]
        };

        let nivelActual = "";
        let pregActual = 0;

        function navegar(id) {
            document.querySelectorAll('.pantalla').forEach(p => p.classList.remove('activa'));
            document.getElementById(id).classList.add('activa');
            window.scrollTo(0,0);
        }

        // LÓGICA DE TRIVIA
        function iniciarTrivia(nivel) {
            nivelActual = nivel; pregActual = 0;
            navegar('pantalla-trivia'); mostrarPregunta();
        }

        function mostrarPregunta() {
            let datos = preguntas[nivelActual][pregActual];
            document.getElementById("trivia-titulo").innerText = "Nivel " + nivelActual.toUpperCase();
            document.getElementById("pregunta-texto").innerText = (pregActual + 1) + ". " + datos.p;
            let cont = document.getElementById("opciones-contenedor");
            cont.innerHTML = "";
            datos.o.forEach((opc, i) => {
                let div = document.createElement("div");
                div.className = "opcion-viva";
                div.innerText = opc;
                div.onclick = () => {
                    if(i === datos.c) {
                        pregActual++;
                        if(pregActual < 5) { alert("¡Respuesta Correcta!"); mostrarPregunta(); }
                        else { alert("¡FELICIDADES! Has completado el " + nivelActual.toUpperCase()); navegar('menu'); }
                    } else { 
                        alert("¡ERROR! Para ser un buen revolucionario hay que estudiar. Regresas al inicio del nivel."); 
                        pregActual = 0; mostrarPregunta(); 
                    }
                };
                cont.appendChild(div);
            });
        }

        // LÓGICA DE SENDEROS (HISTORIA)
        function historia(paso) {
            let txt = document.getElementById("historia-texto");
            let o = document.getElementById("historia-opciones");
            if(paso === 1) {
                txt.innerText = "¡Excelente! Has formado un círculo de estudio. Carlos te entrega una cartilla. Ahora, ¿dónde estableces la escuela?";
                o.innerHTML = `<button class="btn" onclick="historia(3)">Bajo el árbol de ceiba</button>
                               <button class="btn" onclick="historia(3)">En la cueva secreta</button>`;
            } else if(paso === 2) {
                txt.innerText = "Has detectado una patrulla enemiga. Debes alertar al campamento sin ser visto. ¿Qué usas?";
                o.innerHTML = `<button class="btn" onclick="historia(3)">Señales de aves</button>
                               <button class="btn" onclick="historia(3)">Un mensajero veloz</button>`;
            } else {
                alert("Has demostrado lealtad y valor en la montaña. ¡Misión cumplida!");
                navegar('menu');
            }
        }

        // LÓGICA DE PUZZLE (ROMPECABEZAS)
        const fraseOriginal = ["TAMBIÉN", "ENSÉÑENLES", "A", "LEER"];
        let fraseUsuario = [];

        function iniciarPuzzle() { navegar('rompecabezas'); limpiarPuzzle(); }

        function limpiarPuzzle() {
            fraseUsuario = [];
            document.getElementById("resultado-puzzle").innerText = "";
            document.getElementById("btn-verificar-p").style.display = "none";
            let cont = document.getElementById("contenedor-puzzle");
            cont.innerHTML = "";
            [...fraseOriginal].sort(() => Math.random() - 0.5).forEach(pal => {
                let span = document.createElement("span");
                span.className = "pieza";
                span.innerText = pal;
                span.onclick = () => {
                    fraseUsuario.push(pal);
                    document.getElementById("resultado-puzzle").innerText = fraseUsuario.join(" ");
                    span.style.visibility = "hidden";
                    if(fraseUsuario.length === 4) document.getElementById("btn-verificar-p").style.display = "block";
                };
                cont.appendChild(span);
            });
        }

        function verificarPuzzle() {
            if(fraseUsuario.join(" ") === fraseOriginal.join(" ")) {
                alert("¡EXCELENTE! Has completado la frase histórica.");
                navegar('menu');
            } else {
                alert("El orden no es correcto. Intenta de nuevo.");
                limpiarPuzzle();
            }
        }
    </script>
</body>
</html>
