<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>¿Qué emoción estás sintiendo en este momento?</title> 
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #0c2461; /* Azul oscuro */
            color: #fff; /* Texto blanco */
            margin: 0;
            padding: 0;
        }

        header {
            background-color: #1e3799; /* Azul */
            color: #fff; /* Texto blanco */
            padding: 20px 0;
            text-align: center;
        }

        header h1 {
            font-size: 36px;
        }

        .container {
            width: 80%;
            margin: 0 auto;
            padding: 20px 0;
        }

        .emotions {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
        }

        /* Colores para cada emoción */
        .emotion-button.Felicidad { background-color: #FFD700; } /* Amarillo */
        .emotion-button.Tristeza { background-color: #1E90FF; } /* Azul cielo */
        .emotion-button.Enojo { background-color: #FF6347; } /* Rojo */
        .emotion-button.Miedo { background-color: #8A2BE2; } /* Violeta */
        .emotion-button.Ansiedad { background-color: #FFA07A; } /* Salmón */
        .emotion-button.Esperanza { background-color: #32CD32; } /* Verde lima */
        .emotion-button.Amor { background-color: #FF69B4; } /* Rosa */
        .emotion-button.Confusión { background-color: #1E90FF; } /* Azul cielo */
        .emotion-button.Frustración { background-color: #FF4500; } /* Naranja rojizo */
        .emotion-button.Soledad { background-color: #9400D3; } /* Violeta oscuro */
        .emotion-button.Agradecimiento { background-color: #FFA500; } /* Naranja */
        .emotion-button.Inspiración { background-color: #00CED1; } /* Azul verdoso */
        .emotion-button.Paz { background-color: #90EE90; } /* Verde pálido */
        .emotion-button.Culpa { background-color: #FF1493; } /* Rosa fuerte */
        .emotion-button.Orgullo { background-color: #8B4513; } /* Marrón */
        .emotion-button.Desesperación { background-color: #708090; } /* Gris pizarra */
        .emotion-button.Alegría { background-color: #FFD700; } /* Amarillo */
        .emotion-button.Estrés { background-color: #FF4500; } /* Naranja rojizo */
        .emotion-button.Resiliencia { background-color: #32CD32; } /* Verde lima */
        .emotion-button.Optimismo { background-color: #FF69B4; } /* Rosa */
        .emotion-button.Duda { background-color: #708090; } /* Gris pizarra */
        .emotion-button.Inseguridad { background-color: #9400D3; } /* Violeta oscuro */
        .emotion-button.Empatía { background-color: #FFA500; } /* Naranja */
        .emotion-button.Compasión { background-color: #00CED1; } /* Azul verdoso */

        .emotion-button {
            color: #fff; /* Texto blanco */
            border: none;
            padding: 15px 20px;
            font-size: 18px;
            border-radius: 10px;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        .emotion-button:hover {
            opacity: 0.8;
        }

        #message-container {
            margin-top: 30px;
            text-align: center;
        }

        #message {
            font-size: 20px;
        }

        footer {
            background-color: #1e3799; /* Azul */
            color: #fff; /* Texto negro: ; */
            text-align: center;
            padding: 20px 0;
            position: absolute;
            bottom: 0;
            width: 100%;
        }
    </style>
</head>
<body>
    <header>
        <h1>¿Qué emoción estás sintiendo en este momento?</h1>
    </header>
    <div class="container">
        <div class="emotions">
            <button class="emotion-button Felicidad" onclick="showMessage('Felicidad')">Felicidad</button>
            <button class="emotion-button Tristeza" onclick="showMessage('Tristeza')">Tristeza</button>
            <button class="emotion-button Enojo" onclick="showMessage('Enojo')">Enojo</button>
            <button class="emotion-button Miedo" onclick="showMessage('Miedo')">Miedo</button>
            <button class="emotion-button Ansiedad" onclick="showMessage('Ansiedad')">Ansiedad</button>
            <button class="emotion-button Esperanza" onclick="showMessage('Esperanza')">Esperanza</button>
            <button class="emotion-button Amor" onclick="showMessage('Amor')">Amor</button>
            <button class="emotion-button Confusión" onclick="showMessage('Confusión')">Confusión</button>
            <button class="emotion-button Frustración" onclick="showMessage('Frustración')">Frustración</button>
            <button class="emotion-button Soledad" onclick="showMessage('Soledad')">Soledad</button>
            <button class="emotion-button Agradecimiento" onclick="showMessage('Agradecimiento')">Agradecimiento</button>
            <button class="emotion-button Inspiración" onclick="showMessage('Inspiración')">Inspiración</button>
            <button class="emotion-button Paz" onclick="showMessage('Paz')">Paz</button>
            <button class="emotion-button Culpa" onclick="showMessage('Culpa')">Culpa</button>
            <button class="emotion-button Orgullo" onclick="showMessage('Orgullo')">Orgullo</button>
            <button class="emotion-button Desesperación" onclick="showMessage('Desesperación')">Desesperación</button>
            <button class="emotion-button Estrés" onclick="showMessage('Estrés')">Estrés</button>
            <button class="emotion-button Resiliencia" onclick="showMessage('Resiliencia')">Resiliencia</button>
            <button class="emotion-button Optimismo" onclick="showMessage('Optimismo')">Optimismo</button>
            <button class="emotion-button Duda" onclick="showMessage('Duda')">Duda</button>
            <button class="emotion-button Inseguridad" onclick="showMessage('Inseguridad')">Inseguridad</button>
            <button class="emotion-button Empatía" onclick="showMessage('Empatía')">Empatía</button>
            <button class="emotion-button Compasión" onclick="showMessage('Compasión')">Compasión</button>
        </div>
        <div id="message-container">
            <p id="message"></p>
        </div>
    </div>
    <footer>
    </footer>

    <script>
        function showMessage(emotion) {
            var messages = {
                'Felicidad': "Hiii ¡Es tan maravilloso verte radiante de felicidad! Tu sonrisa es como un rayo de sol que ilumina cada rincón de mi corazón. Saber que estás disfrutando de la vida y encontrando alegría en cada momento me llena de una inmensa felicidad también. Recuerda que la vida está llena de momentos brillantes como este, y estoy aquí para celebrar cada uno de ellos contigo. Tu felicidad es contagiosa y me inspira a ser una mejor persona cada día. Que esta felicidad que estás experimentando se convierta en un río interminable de alegría y que cada día esté lleno de momentos tan hermosos como este. Te quiero mucho.",
                'Tristeza': "Oiii Staylor, nos volvemos a encontrar, de verdad que quiero que sepas que la tristeza es una emoción natural que todos experimentamos en algún momento de nuestras vidas, y aunque pueda parecer abrumadora en este momento, recuerda que esta oscuridad eventualmente dará paso a la luz. Permíteme estar a tu lado mientras navegas por estos sentimientos, recordándote que no estás sola en este camino. Tu fuerza y resiliencia son inspiradoras, y confío en que encontrarás la luz al final de este túnel. Juntos, superaremos este desafío y saldremos más fuertes del otro lado. No dudes en comunicarte conmigo siempre que lo necesites, ya sea para hablar, llorar o simplemente para compartir el silencio. Estoy aquí para ti, hoy y siempre.",
                'Enojo': "Entiendo que estés sintiendo enojo en este momento, y quiero que sepas que estoy aquí para ti, sin importar cuán grande sea la tormenta que estés enfrentando. Tu enojo es válido y comprensible, y estoy aquí para ofrecerte mi apoyo incondicional mientras navegas por estas emociones intensas. El enojo puede ser una fuerza poderosa y abrumadora, pero recuerda que tú tienes el control sobre cómo lo manejas. Permíteme ser tu ancla en medio de esta tormenta, ofreciéndote mi presencia tranquila y mi escucha compasiva mientras te ayudamos a encontrar maneras saludables de canalizar este enojo. Juntos, podemos trabajar para comprender las raíces de tu enojo y buscar soluciones constructivas para abordar cualquier situación que lo esté provocando. Confío en tu capacidad para superar este desafío y encontrar la paz en medio de la tormenta. No dudes en comunicarte conmigo en cualquier momento. Estoy aquí para apoyarte, ya sea para hablar sobre lo que te está molestando o simplemente para estar contigo en silencio.",
                'Miedo': "Me acabo de enterar que estás pasando por un momento de miedo, y quiero que sepas que estoy aquí para ti. Mientras enfrentas tus temores, quiero recordarte cuánto confío en ti, no sólo para superar este desafío, sino para emerger de él más fuerte y más sabio de lo que nunca creíste posible. El miedo puede parecer una sombra oscura que amenaza con envolvernos, pero tú, eres una luz brillante capaz de iluminar incluso los rincones más oscuros de la mente y el corazón. Confío en tu fuerza interior y tu valentía, en tu capacidad para enfrentar tus miedos de frente y transformarlos en oportunidades de crecimiento y aprendizaje. Recuerda que el miedo es sólo una parte de tu historia, no el final de ella. Cada desafío que enfrentas te brinda la oportunidad de descubrir más sobre ti mismo, de crecer en comprensión y compasión, y de abrazar tu verdadero potencial con valentía y determinación. En estos momentos de miedo, quiero que sepas que no estás solo. Estoy aquí a tu lado, con los brazos abiertos y el corazón lleno de amor y apoyo incondicional. Juntos, enfrentaremos tus temores, desafiaremos las limitaciones autoimpuestas y daremos paso a un futuro lleno de posibilidades infinitas. No temas pedir ayuda cuando la necesites, ni permitas que el miedo te paralice. Eres más fuerte de lo que imaginas, y estoy aquí para recordártelo en cada paso del camino.",
                'Ansiedad': "La ansiedad puede ser abrumadora, pero recuerda que cada paso que das es un logro. Estoy aquí para apoyarte en este camino y brindarte tranquilidad.",
                'Esperanza': "La esperanza es una luz brillante en tiempos oscuros. Mantén la fe y recuerda que siempre hay una salida. Estoy aquí para caminar contigo hacia un futuro mejor.",
                'Amor': "Hoy quiero recordarte cuánto significas para mí y cuánto amor tengo por ti en mi corazón. Cada momento que pasamos juntos es un tesoro para mí, lleno de risas, conversaciones profundas y recuerdos que atesoraré para siempre. Tu presencia en mi vida es un regalo que nunca dejaré de agradecer. Tu bondad, tu generosidad y tu capacidad para ver lo mejor en los demás son cualidades que admiro profundamente en ti. Eres un ser humano excepcional, y me siento increíblemente afortunada de tenerte. se le quiere. Que este mensaje sirva como un recordatorio de que siempre estaré aquí para ti, en los buenos y malos momentos, con los brazos abiertos y el corazón lleno de amor. Eres amado más de lo que puedas imaginar.",
                'Confusión': "La vida puede ser confusa a veces, pero juntos podemos encontrar claridad. Estoy aquí para ayudarte a entender y navegar por cualquier situación.",
                'Frustración': "La frustración es parte de la vida, pero también es una oportunidad para crecer             y superar desafíos. Estoy aquí para apoyarte y ayudarte a convertir la frustración en éxito.",
                'Soledad': "Hello, siento mucho escuchar que estás atravesando un momento de soledad. Quiero que sepas que, aunque pueda parecer que estás solo en este momento, estoy aquí para ti. La soledad puede ser una compañera difícil de enfrentar, pero recuerda que nunca estás completamente solo. Estoy aquí, a tu lado, con los brazos abiertos y el corazón lleno de comprensión. Puedes contar conmigo para ofrecerte consuelo, apoyo y compañía en cada paso del camino. Aunque la vida pueda parecer sombría en este momento, quiero recordarte que la soledad es solo una estación en tu viaje, no tu destino final. Juntos, encontraremos formas de iluminar incluso los días más oscuros con risas, conversaciones significativas y momentos compartidos. Permíteme ser tu amiga en este momento de soledad, recordándote que eres amado y valorado más de lo que puedas imaginar. Tu presencia en mi vida es un regalo que aprecio profundamente, y estoy agradecida por cada momento que compartimos juntos. No dudes en comunicarte conmigo siempre que lo necesites, ya sea para hablar sobre lo que te está molestando o simplemente para saber que no estás solo. Estoy aquí para ti, hoy y siempre.",
                'Agradecimiento': "El agradecimiento es una poderosa expresión de amor y reconocimiento. Estoy agradecida por tu amistad y siempre valoraré nuestra conexión.",
                'Inspiración': "Tu capacidad para inspirar a los demás es asombrosa. Sigue siendo una fuente de luz y motivación para aquellos que te rodean.",
                'Paz': "La paz interior es un regalo invaluable. Que encuentres serenidad y armonía en tu corazón en medio de cualquier situación.",
                'Culpa': "La culpa puede ser una carga pesada, pero recuerda que todos cometemos errores. Permíteme ofrecerte comprensión y perdón.",
                'Orgullo': "Hoy quiero tomarme un momento para expresarte cuánto orgullo siento por ti. Eres una persona verdaderamente excepcional, llena de talento, determinación y una capacidad innata para inspirar a los demás. Cada vez que te veo enfrentar un desafío con valentía y determinación, mi corazón se hincha de orgullo. Tu dedicación y esfuerzo son ejemplos inspiradores para todos los que te rodean, y estoy increíblemente agradecida de tener la oportunidad de ser testigo de tu crecimiento y éxito. Tu capacidad para superar obstáculos, perseguir tus sueños y convertir tus metas en realidad es verdaderamente inspiradora. No sólo has logrado tanto en tu vida, sino que lo has hecho con gracia, humildad y un corazón lleno de bondad y compasión. En cada logro que alcanzas, en cada meta que conquistas, mi admiración por ti solo crece más y más. Eres una luz brillante en este mundo, recuerda que siempre estaré aquí para apoyarte, celebrar tus éxitos y animarte en tus desafíos. Eres una persona extraordinaria, y no puedo esperar para ver todo lo que el futuro tiene reservado para ti.",
                'Desesperación': "La desesperación puede nublar nuestra visión, pero recuerda que siempre hay esperanza. Juntos encontraremos una solución.",
                'Estrés': "El estrés puede abrumarnos, pero recuerda que tienes la fuerza y la resiliencia para superarlo. Estoy aquí para ofrecerte apoyo y alivio.",
                'Resiliencia': "Tu resiliencia y fortaleza son admirables. Sigues adelante a pesar de los desafíos y eso es verdaderamente inspirador.",
                'Optimismo': "El optimismo es la clave para abrir nuevas puertas y crear nuevas posibilidades. Mantén la esperanza viva y sigue persiguiendo tus sueños.",
                'Duda': "La duda puede ser una compañera incómoda, pero recuerda que tus dudas no definen quién eres. Estoy aquí para ayudarte a encontrar claridad y confianza.",
                'Inseguridad': "La inseguridad puede pesar sobre ti, pero recuerda que eres único/a y valioso/a en tu propio camino. Estoy aquí para recordarte tu valía y ayudarte a encontrar la confianza en ti mismo/a.",
                'Empatía': "Tu empatía y comprensión son cualidades admirables. Sigues siendo una luz de compasión en un mundo a menudo desafiante.",
                'Compasión': "La compasión es una fuerza poderosa que puede cambiar el mundo. Sigue mostrando amor y cuidado a aquellos que te rodean."
            };

            var messageContainer = document.getElementById('message');
            messageContainer.innerHTML = messages[emotion];
        }
    </script>
</body>
</html>
