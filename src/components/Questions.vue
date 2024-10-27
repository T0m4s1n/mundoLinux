<template>
  <div class="faq-section">
    <div class="faq-container">
      <div class="faq-header">
        <h1>Tienes preguntas? puedes consultarlas aqui</h1>
        <p>
          igualmente si sigues con dudas despues de leer este apartado puedes comunicarte con nosotros a traves de nuestro correo electronico o numero (+573007478871) y enfatiza la importancia de comunicarse con este centro para recibir ayuda especializada y directa en situaciones críticas que superen las capacidades del bot.
        </p>
      </div>
      <div class="faq-content">
        <div class="faq-item" v-for="(faq, index) in faqs" :key="index">
          <h2 @click="toggleFaq(index)">
            {{ faq.question }}
            <span v-if="faq.open">-</span>
            <span v-else>+</span>
          </h2>
          <transition name="slide">
            <p v-if="faq.open">{{ faq.answer }}</p>
          </transition>

          <hr />
        </div>
      </div>
    </div>
    <div class="contact-bar">
      <div class="contact-content">
        <div class="contact-text">
          <p>Contactanos</p>
          <p class="contact-subtext">Te mandaremos un mensaje una vez por cada semana. SIN SPAM.</p>
        </div>
        <div class="contact-form">
          <input type="email" placeholder="Ingresa tu email" />
          <button>Subscribete</button>
        </div>
      </div>
    </div>
  </div>
  <br>
  <br>
  <br>
  <br>
</template>

<script>
export default {
  name: 'QuestionsView',
  data() {
    return {
      faqs: [
        {
          question: "Como funciona el chatbot?",
          answer: "ML SecureBot está programado para responder preguntas sobre una amplia gama de temas relacionados con la seguridad digital, incluyendo pero no limitándose a: protección de datos, seguridad en redes, malware, phishing, contraseñas seguras y la privacidad en línea. Los usuarios pueden realizar consultas generales o específicas, y el bot proporciona respuestas claras, acompañadas de recomendaciones prácticas para fortalecer la seguridad de sus dispositivos y datos.",
          open: false
        },
        {
          question: "Tiene algun costo adicional?",
          answer: "No, el chatbot es completamente gratuito.",
          open: false
        },
        {
          question: "Donde puedo acceder al chat?",
          answer: "Puedes ingresar al chat a traves del codigo QR, o con cualquiera de los botones de chat",
          open: false
        },
        {
          question: "Que beneficios me ofrece el chatbot?",
          answer: "El chatbot te ofrece una serie de beneficios como: Vlidacion de URLS, Cuestionario de ciberseguridad interactivo, Asistencia en casos de emergencia, Consejos de seguridad, Explicacion de terminos de ciberseguridad, Alertas en tiempo real",
          open: false
        }
      ]
    };
  },
  methods: {
    toggleFaq(index) {
      this.faqs[index].open = !this.faqs[index].open;
    }
  }
};
</script>

<style scoped>
.faq-section {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-color: #1a1a1a;
  color: #fff;
  padding: 60px 0;
  background: linear-gradient(to bottom, #4F46A5 0%, #000000 100%);
}

.faq-container {
  width: 80%;
  max-width: 1200px;
  display: flex;
  justify-content: space-between;
}

.faq-header {
  width: 45%;
}

.faq-header h1 {
  font-size: 36px;
  margin-bottom: 20px;
}

.faq-header p {
  font-size: 16px;
  margin-bottom: 30px;
  color: rgba(255, 255, 255, 0.8);
}

.more-faqs {
  color: #ff6347;
  text-decoration: none;
  font-weight: bold;
}

.more-faqs span {
  font-size: 18px;
  margin-left: 5px;
}

.faq-content {
  width: 45%;
}

.faq-item {
  margin-bottom: 20px;
}

.faq-item h2 {
  font-size: 18px;
  cursor: pointer;
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: #fff;
}

.faq-item h2 span {
  font-size: 24px;
  color: white;
  
}

.faq-item p {
  font-size: 16px;
  margin-top: 10px;
  color: rgba(255, 255, 255, 0.8);
  transition: all 0.3s ease;
}

.faq-item hr {
  border: none;
  border-top: 1px solid rgba(255, 255, 255, 0.1);
  margin-top: 15px;
  transition: all 0.3s ease;
}

.slide-enter-active, .slide-leave-active {
  transition: all 0.3s ease;
}
.slide-enter, .slide-leave-to {
  transform: translateY(-20px);
  transition: all 0.3s ease;
  opacity: 0;
}
.contact-bar {
  width: 91%;
  left:35px;
  background-color: #222;
  padding: 20px 0;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 40px;
  box-shadow: 0px 4px 12px rgba(0, 0, 0, 0.1);
  border-radius: 20px;

}

.contact-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 80%;
  max-width: 1200px;
  flex-direction: row;
}

.contact-text p {
  font-size: 24px;
  color: #fff;
  margin-bottom: 5px;
}

.contact-subtext {
  font-size: 16px;
  color: rgba(255, 255, 255, 0.6);
  margin-bottom: 20px;
  font-family: 'Poppins', sans-serif; 
}

.contact-form {
  display: flex;
  align-items: center;
}

.contact-form input {
  padding: 12px;
  width: 300px;
  margin-right: 10px;
  border: 1px solid rgba(255, 255, 255, 0.3);
  background-color: #1c1c1c;
  color: #fff;
  border-radius: 5px;
  transition: background-color 0.3s ease, box-shadow 0.3s ease;
  font-family: 'Poppins', sans-serif;
}

.contact-form input:focus {
  background-color: #262626;
  outline: none;
  box-shadow: 0 0 5px rgba(255, 99, 71, 0.5);
}

.contact-form input::placeholder {
  color: rgba(255, 255, 255, 0.6);
}

.contact-form button {
  padding: 12px 20px;
  background: linear-gradient(90deg, #f953c6, #2E16FA);
  border: none;
  color: #fff;
  cursor: pointer;
  border-radius: 5px;
  transition: background-color 0.3s ease;
  font-family: 'Poppins', sans-serif;
  transition: transform 0.5s ease-in-out, opacity 0.5s ease-in-out;
}

.contact-form button:hover {
transform: translateY(-5px);
background-color: #3e3a91;
border: 2px solid #f953c6;
animation: glow 1.5s infinite alternate;
}

@keyframes glow {
  from {
    box-shadow: 0 0 5px #fff;
  }
  to {
    box-shadow: 0 0 20px #fff;
  }
}

</style>
