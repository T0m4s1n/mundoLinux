<template>
    <section class="homeview">
        <div class="layout-container">
            <div class="code-container">
                <pre>
                    <code id="codeBlock">
                        <div class="lineOfCode">
                            <em>Soy ML SecureBot</em>
                        </div>
                        <div class="lineOfCode">
                            <strong>Y estoy listo</strong>
                        </div>
                        <div class="lineOfCode">
                            <b>Para ayudarte!</b>
                        </div>
                    </code>
                </pre>
            </div>
        </div>
        <div class="background-bar"></div>
        <div class="layout-container">
            <div class="content-container">
                <h1>ML SecureBot</h1>
                <h2>Tu asistente de ciberseguridad</h2>
                <p>ML SecureBot está aquí para ayudarte a protegerte de amenazas en línea y correos maliciosos.</p>
                <p>Utiliza inteligencia artificial para detectar comportamientos sospechosos y ofrecerte soluciones rápidas y efectivas.</p>
                <button class="start-button">Comenzar a chatear</button>
                
                <div class="payment-methods">
                    <div class="method-card large">
                        <div class="icon"><img src="../assets/icons/email.png" alt="Icono verificar correos" /></div>
                        <h3>Verificar correos sospechosos</h3>
                        <p>¿Tienes dudas sobre un correo? Puedo ayudarte a identificar si es seguro o no.</p>
                    </div>
                    <div class="method-card small">
                        <div class="icon"><img src="../assets/icons/asesoria.png" alt="Icono asesoría" /></div>
                        <h3>Asesoría en seguridad</h3>
                        <p>Recibe recomendaciones sobre cómo mejorar la seguridad de tu cuenta.</p>
                    </div>
                    <div class="method-card small">
                        <div class="icon"><img src="../assets/icons/reporte.png" alt="Icono reportar actividades" /></div>
                        <h3>Reportar actividades inusuales</h3>
                        <p>Si has notado algo raro en tus cuentas, házmelo saber y te guiaré sobre qué hacer.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'HomeView',
    components: {}
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap');
@import url('https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;1,100;1,200;1,300;1,400;1,500;1,600;1,700&display=swap');

.homeview {
    font-family: 'Poppins', sans-serif;
    position: relative;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 20px;
    overflow: hidden;
    background: linear-gradient(to bottom, #000000 0%, #4F46A5 100%);
}

.background-bar {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100vh;
    background-color: transparent;
    z-index: 0;
}

.layout-container {
    position: relative;
    z-index: 1;
    display: flex;
    align-items: center;
    gap: 40px;
    width: 40%;
    max-width: 1200px;
}

.hero-image-container {
    flex: 1;
    display: flex;
    justify-content: center;
    align-items: center;
}

.hero-image {
    width: 300px;
    height: auto;
    animation: float 3s ease-in-out infinite;
}

@keyframes float {
    0%, 100% {
        transform: translateY(0);
    }
    50% {
        transform: translateY(-15px);
    }
}

.content-container {
    flex: 2;
    display: flex;
    flex-direction: column;
    gap: 20px;
    color: white;
}

.start-button {
    background: linear-gradient(90deg, #f953c6, #2E16FA);
    border: none;
    border-radius: 5px;
    padding: 10px 20px;
    color: white;
    font-size: 1.1rem;
    cursor: pointer;
    transition: background 0.3s, transform 0.5s ease-in-out, opacity 0.5s ease-in-out;
    font-family: 'Poppins', sans-serif;
}

.start-button:hover {
    transform: translateY(-5px);
    opacity: 0.9; 
}

.payment-methods {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: auto;
    gap: 20px;
    width: 100%;
}

.method-card {
    background: #1c1c1e;
    border-radius: 10px;
    padding: 20px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
    color: white;
}

.method-card.large {
    grid-column: span 2;
    grid-row: span 1;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
}

.method-card.small {
    grid-column: span 1;
}

.method-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
}

.method-card h3 {
    margin-top: 10px;
    font-size: 1.2rem;
}

.method-card p {
    margin-bottom: 0;
    font-size: 1rem;
}

.icon {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 10px;
    border-radius: 50%;
    width: 50px;
    height: 50px;
    background: white;
    
}

.icon img {
    width: 100%;
    height: auto;
}

pre {
  font-size: 1.5rem;
  line-height: 2rem;
  padding: 1.5rem;
  padding-left: 1.5rem;
  background-color: #151718;
  color: #e6cd69;
  border-radius: 8px;
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.5);
  white-space: pre-wrap;
}

code {
  font-family: "IBM Plex Mono", monospace;
  font-weight: 400;
}

b,
em,
strong {
  text-decoration: none;
  font-weight: 400;
  font-style: normal;
  color: #2E16FA;
}

em {
  color: #4F46A5;
}

strong {
  color: #fff;
}

.lineOfCode {
  padding: 0;
  margin: 0;
  width: 0;
  height: auto;
  overflow: hidden;
  white-space: nowrap;
  border-right: 2px solid #fff;
  animation: typingEffect 0.6s steps(16, end) forwards,
    caretAnim 0.8s steps(2, end) infinite;
}

.lineOfCode:nth-of-type(2) {
  animation-delay: 2s;
}

.lineOfCode:nth-of-type(3) {
  animation-delay: 4s;
}

@keyframes typingEffect {
  to {
    width: 16ch;
  }
}

@keyframes caretAnim {
  50% {
    border-color: transparent;
  }
}
</style>
