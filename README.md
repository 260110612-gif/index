<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>¿Quién soy? | Emma</title>

<style>

/* CONFIGURACIÓN GENERAL */

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    scroll-behavior: smooth;
}

:root {
    --verde: #174f46;
    --verde-claro: #287b68;
    --dorado: #c59b55;
    --crema: #f5f0e7;
    --blanco: #ffffff;
    --texto: #34443f;
}

body {
    font-family: 'Segoe UI', Arial, sans-serif;
    background:
        radial-gradient(circle at 10% 10%, #dce9df, transparent 35%),
        linear-gradient(135deg, #f5f0e7, #e4eee7);
    color: var(--texto);
    line-height: 1.8;
}

/* BARRA DE NAVEGACIÓN */

nav {
    position: sticky;
    top: 0;
    z-index: 100;
    background: rgba(23, 79, 70, 0.96);
    padding: 15px;
    text-align: center;
    box-shadow: 0 4px 15px rgba(0,0,0,0.15);
    backdrop-filter: blur(10px);
}

nav a {
    color: white;
    text-decoration: none;
    margin: 0 12px;
    font-size: 14px;
    font-weight: bold;
    transition: 0.3s;
}

nav a:hover {
    color: #e5bd78;
}

/* CONTENEDOR */

.container {
    max-width: 1050px;
    margin: 45px auto;
    padding: 0 20px;
}

/* SECCIONES */

section {
    background: rgba(255,255,255,0.93);
    border-radius: 25px;
    padding: 45px;
    margin-bottom: 40px;
    border: 1px solid #d9e4da;
    box-shadow: 0 12px 35px rgba(31, 73, 57, 0.09);
    animation: aparecer 0.9s ease;
    transition: transform 0.3s, box-shadow 0.3s;
}

section:hover {
    box-shadow: 0 16px 40px rgba(31, 73, 57, 0.15);
}

/* ANIMACIÓN */

@keyframes aparecer {
    from {
        opacity: 0;
        transform: translateY(25px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

/* TÍTULOS */

h1 {
    font-size: 55px;
    text-align: center;
    color: var(--verde);
    letter-spacing: 3px;
    margin-bottom: 12px;
}

h2 {
    color: var(--verde);
    font-size: 32px;
    margin-bottom: 25px;
    border-left: 5px solid var(--dorado);
    padding-left: 15px;
}

h3 {
    color: var(--verde-claro);
    font-size: 22px;
    margin-bottom: 10px;
}

.numero {
    color: var(--dorado);
    font-weight: 800;
}

.subtitulo {
    text-align: center;
    color: #687a70;
    font-size: 19px;
    margin-bottom: 25px;
}

/* PORTADA */

.portada {
    background:
        linear-gradient(135deg, rgba(23,79,70,0.97), rgba(40,123,104,0.93));
    color: white;
    padding: 75px 35px;
    border-radius: 30px;
    position: relative;
    overflow: hidden;
    text-align: center;
}

.portada::before {
    content: "✦";
    position: absolute;
    font-size: 180px;
    color: rgba(255,255,255,0.07);
    right: 25px;
    top: -45px;
}

.portada h1 {
    color: #ffffff;
    font-size: 58px;
    position: relative;
}

.portada .subtitulo {
    color: #e6eee9;
}

.especialidad {
    display: inline-block;
    border: 1px solid #d8b779;
    border-radius: 50px;
    padding: 13px 25px;
    color: #f3d69e;
    margin-top: 20px;
    font-weight: bold;
}

/* FOTOGRAFÍAS */

.foto {
    width: 100%;
    max-width: 520px;
    height: 340px;
    display: block;
    margin: 25px auto 35px;
    object-fit: cover;
    border-radius: 25px 80px 25px 80px;
    border: 5px solid white;
    outline: 2px solid #c59b55;
    box-shadow: 0 12px 25px rgba(0,0,0,0.15);
    transition: transform 0.4s, border-radius 0.4s;
}

.foto:hover {
    transform: scale(1.025);
    border-radius: 50px;
}

/* TEXTO */

p {
    font-size: 17px;
    margin-bottom: 18px;
    text-align: justify;
}

/* TARJETAS */

.tarjeta {
    background: linear-gradient(135deg, #edf4ed, #ffffff);
    border: 1px solid #d5e4d8;
    border-left: 5px solid var(--verde-claro);
    border-radius: 18px;
    padding: 25px;
    margin-top: 20px;
    transition: 0.3s;
}

.tarjeta:hover {
    transform: translateX(8px);
    box-shadow: 0 8px 20px rgba(23,79,70,0.12);
    border-left-color: var(--dorado);
}

.tarjeta p {
    margin-bottom: 0;
}

/* COLLAGE */

.collage {
    width: 100%;
    max-height: 440px;
    object-fit: cover;
    border-radius: 35px;
    margin-top: 30px;
    border: 5px solid white;
    box-shadow: 0 10px 25px rgba(0,0,0,0.13);
    transition: 0.4s;
}

.collage:hover {
    transform: scale(1.015);
}

/* LISTA */

ul {
    padding-left: 25px;
}

li {
    margin-bottom: 17px;
    font-size: 17px;
}

li strong {
    color: var(--verde-claro);
}

/* FRASE FINAL */

.frase {
    background: var(--verde);
    color: white;
    text-align: center;
    padding: 35px;
    border-radius: 25px;
    font-size: 20px;
    font-style: italic;
    border-bottom: 5px solid var(--dorado);
}

/* PIE DE PÁGINA */

footer {
    text-align: center;
    color: #536b5e;
    padding: 30px 10px;
    font-size: 15px;
}

/* CELULARES */

@media (max-width: 650px) {

    nav {
        padding: 12px 5px;
    }

    nav a {
        display: inline-block;
        margin: 5px;
        font-size: 12px;
    }

    .container {
        margin-top: 20px;
        padding: 0 12px;
    }

    section {
        padding: 25px 20px;
    }

    h1, .portada h1 {
        font-size: 37px;
    }

    h2 {
        font-size: 25px;
    }

    .portada {
        padding: 55px 20px;
    }

    .foto {
        height: 260px;
    }

    p, li {
        font-size: 16px;
    }
}

</style>
</head>

<body>

<!-- MENÚ -->

<nav>
    <a href="#inicio">Inicio</a>
    <a href="#conoceme">Conóceme</a>
    <a href="#origen">Origen</a>
    <a href="#estudios">Estudios</a>
    <a href="#pasatiempos">Pasatiempos</a>
    <a href="#favoritos">Favoritos</a>
</nav>

<div class="container">

<!-- PORTADA -->

<section class="portada" id="inicio">

    <h1>¿QUIÉN SOY?</h1>

    <div class="subtitulo">
        Emma · Mi historia, mis metas y lo que me inspira
    </div>

    <div class="especialidad">
        Ingeniería en Tecnologías de la Información y Comunicaciones
    </div>

</section>

<!-- 01 CONÓCEME -->

<section id="conoceme">

    <img src="WhatsApp Image 2026-11-09 at 1.03.11 PM (4).jpeg"
         alt="Fotografía de Emma"
         class="foto">

    <h2><span class="numero">01.</span> Conóceme</h2>

    <p>
        Soy Emma. Me considero una persona seria y sumamente
        responsable, que ha aprendido a enfrentar la vida con madurez.
        Desde pequeña he enfrentado complicaciones de salud y eso
        me enseñó a valorar cada día y a no rendirme fácilmente.
        Eso me hizo una persona eficaz.
    </p>

    <p>
        No le tengo miedo a lo nuevo que viene; al contrario,
        lo veo como una oportunidad para crecer y demostrar
        de qué estoy hecha. Aunque a veces no exprese mucho
        con palabras, valoro a cada una de las personas que
        me han apoyado y que nunca me han dejado sola.
    </p>

</section>

<!-- 02 ORIGEN -->

<section id="origen">

    <h2><span class="numero">02.</span> ¿De dónde vengo?</h2>

    <p>
        Mis raíces están en <strong>Colonia Huitexcalco</strong>,
        el lugar de donde vengo y que forma parte de mi historia.
    </p>

    <img src="WhatsApp Image 2026-11-09 at 1.03.11 PM (6).jpeg"
         alt="Colonia Huitexcalco"
         class="foto">

</section>

<!-- 03 ESTUDIOS -->

<section id="estudios">

    <h2><span class="numero">03.</span> ¿Por qué estudio TICs?</h2>

    <p>
        Llegar hasta esta universidad no fue nada fácil,
        pero mis ganas de superarme en el ámbito académico
        me impulsaron a seguir adelante. Mis metas son demostrar
        que, aunque haya tenido y tenga situaciones complicadas,
        sí se puede.
    </p>

    <p>
        También le debo esta oportunidad a mis papás, quienes,
        poco o mucho, siempre me han apoyado. Quiero seguir
        creciendo y adquiriendo conocimientos. Elegí TICs porque
        desde un principio me ha gustado la tecnología,
        los códigos y descubrir todo lo que puedo aprender
        sobre ellos.
    </p>

    <div class="tarjeta">
        <h3>💻 Tecnología</h3>
        <p>Explorar herramientas y nuevas posibilidades.</p>
    </div>

    <div class="tarjeta">
        <h3>⌨️ Programación</h3>
        <p>Aprender códigos y resolver problemas.</p>
    </div>

    <div class="tarjeta">
        <h3>🚀 Superación</h3>
        <p>Crecer, avanzar y demostrar que sí se puede.</p>
    </div>

</section>

<!-- 04 PASATIEMPOS -->

<section id="pasatiempos">

    <h2><span class="numero">04.</span> Mis pasatiempos</h2>

    <div class="tarjeta">
        <h3>🛍️ Trabajar</h3>
        <p>Ser responsable y salir adelante.</p>
    </div>

    <div class="tarjeta">
        <h3>📚 Estudiar</h3>
        <p>Prepararme para alcanzar mis metas.</p>
    </div>

    <div class="tarjeta">
        <h3>😴 Dormir</h3>
        <p>Descansar y recargar energía.</p>
    </div>

    <div class="tarjeta">
        <h3>❤️ Estar con mi pareja</h3>
        <p>Compartir momentos especiales.</p>
    </div>

    <div class="tarjeta">
        <h3>🧠 Aprender tecnología</h3>
        <p>Seguir descubriendo cosas nuevas.</p>
    </div>

    <img src="WhatsApp Image 2026-11-09 at 1.03.11 PM (5).jpeg"
         alt="Collage de mis pasatiempos"
         class="collage">

</section>

<!-- 05 CONTENIDO FAVORITO -->

<section id="favoritos">

    <h2>
        <span class="numero">05.</span>
        Top 5 de mi contenido favorito
    </h2>

    <ul>

        <li>
            <strong>Anime:</strong>
            Me gusta verlo para distraerme y conocer historias diferentes.
        </li>

        <li>
            <strong>Facebook:</strong>
            Para estar conectado y enterarme de lo que pasa.
        </li>

        <li>
            <strong>TikTok:</strong>
            Contenido rápido y entretenido.
        </li>

        <li>
            <strong>YouTube:</strong>
            Para aprender sobre tecnología, códigos y temas que me interesan.
        </li>

        <li>
            <strong>Instagram:</strong>
            Para ver contenido variado y estar al día.
        </li>

    </ul>

    <img src="WhatsApp Image 2026-11-09 at 1.03.11 PM (3).jpeg"
         alt="Mis redes sociales favoritas"
         class="collage">

</section>

<!-- FRASE FINAL -->

<div class="frase">

    "Mi pasado me fortalece, mi presente me prepara
    y mi futuro me espera."

</div>

<footer>
    Página personal de Emma | Ingeniería en TICs
    <br>
    © 2026 · Mi historia, mi esencia y mis sueños.
</footer>

</div>

</body>
</html>
