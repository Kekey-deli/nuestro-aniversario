# nuestro-aniversario
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nuestra Zona Secreta 🌌</title>
    <style>
        /* --- FONDO NEGRO Y TEXTO GENERAL --- */
        body {
            background-color: #000000;
            background-image: radial-gradient(#1a0033 15%, transparent 15%);
            background-size: 20px 20px;
            color: #b3d9ff; /* Texto azul claro muy legible */
            font-family: 'Courier New', Courier, monospace;
            margin: 0;
            padding: 20px;
        }

        /* --- MARQUESINA DE ARRIBA (MORADO Y AZUL) --- */
        .marquee-retro {
            background: linear-gradient(90deg, #4d0099, #0055ff, #9900cc);
            color: #ffffff;
            font-weight: bold;
            padding: 12px;
            font-size: 24px;
            text-shadow: 2px 2px #000000;
            border: 3px outset #0055ff;
            margin-bottom: 20px;
        }

        /* --- CONTENEDOR EN REJILLA --- */
        .grid-container {
            display: grid;
            grid-template-columns: 1fr;
            gap: 20px;
        }
        @media(min-width: 768px) {
            .grid-container { grid-template-columns: 1fr 2fr 1fr; }
        }

        /* --- CAJITAS CON BORDES AZULES Y ADORNOS MORADOS --- */
        .retro-box {
            background-color: #0b001a; /* Negro con un toque morado muy oscuro */
            border: 4px double #0088ff; /* Borde doble azul neón */
            padding: 15px;
            box-shadow: 6px 6px 0px #aa00ff; /* Sombra rígida morada */
        }

        /* Títulos de las cajas en Morado Brillante */
        .retro-box h2 {
            background-color: #7700ea; 
            color: #ffffff;
            margin-top: 0;
            padding: 6px;
            font-size: 18px;
            text-align: center;
            text-shadow: 1px 1px #000;
            border: 2px ridge #0088ff;
        }

        /* --- DETALLES DE TEXTO RESALTADO --- */
        .neon-purple { color: #df80ff; text-shadow: 0 0 5px #aa00ff; }
        .neon-blue { color: #3399ff; text-shadow: 0 0 5px #0055ff; }
        
        .contador {
            font-size: 22px;
            text-align: center;
            color: #00ffff; /* Cian neón para el reloj */
            font-weight: bold;
            text-shadow: 0 0 8px #0088ff;
        }
    </style>
</head>
<body>

    <marquee class="marquee-retro" scrollamount="7">✨ WELCOME TO OUR SPACE // 03.07.2026 // NUESTRO ANIVERSARIO ✨</marquee>

    <div class="grid-container">
        
        <div class="retro-box">
            <h2>[ DISTANCE ]</h2>
            <p><span class="neon-purple">Tú:</span> Allá 📍</p>
            <p><span class="neon-blue">Yo:</span> Aquí 📍</p>
            <hr style="border: 1px dashed #7700ea;">
            <center>
                <div style="border: 2px dashed #0088ff; padding: 10px; color: #7700ea;">
                    [ Aquí irá tu dibujo 1 ]
                </div>
            </center>
        </div>

        <div class="retro-box">
            <h2>[ COUNTDOWN ]</h2>
            <div id="reloj" class="contador">Calculando...</div>
            
            <hr style="border: 1px dashed #aa00ff; margin: 20px 0;">
            
            <h2>[ OUR LOG ]</h2>
            <p>Hola mi amor... Bienvenido a nuestro rincón en el internet. Diseñé este espacio con colores de la galaxia y la noche porque me recuerdan a lo infinito de nuestro cariño. ¡Feliz 3 de Julio! 📟🌌</p>
            
            <center>
                <div style="border: 2px dashed #aa00ff; padding: 20px; color: #0088ff; margin-top: 15px;">
                    [ Aquí irá tu animación principal ]
                </div>
            </center>
        </div>

        <div class="retro-box">
            <h2>[ MUSIC ]</h2>
            <p style="color: #00ffff; text-align: center;">🎵 Playlist Especial</p>
            <div style="background: #050010; padding: 20px; text-align: center; border: 2px inset #0088ff;">
                [ Aquí pondremos la música ]
            </div>
        </div>

    </div>

    <script>
        const fechaInicio = new Date(2026, 6, 3); 

        function actualizarContador() {
            const ahora = new Date();
            let diferencia = ahora - fechaInicio;
            let prefijo = "Llevamos: ";

            if (diferencia < 0) {
                diferencia = fechaInicio - ahora;
                prefijo = "Faltan: ";
            }

            const dias = Math.floor(diferencia / (1000 * 60 * 60 * 24));
            const horas = Math.floor((diferencia % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutos = Math.floor((diferencia % (1000 * 60 * 60)) / (1000 * 60));
            const segundos = Math.floor((diferencia % (1000 * 60)) / 1000);

            document.getElementById('reloj').innerHTML = 
                `${prefijo}<br>${dias}d ${horas}h ${minutos}m ${segundos}s`;
        }

        setInterval(actualizarContador, 1000);
        actualizarContador();
    </script>

</body>
</html>
