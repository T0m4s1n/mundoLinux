<template>
    <section class="about">
        <br>
        <h2>Testimonios</h2>
        <br>
        <div class="testimonials">
            <div class="testimonial">
                <img src="../assets/icons/persona1.png" alt="Sarah Khan">
                <h3>Teresa Galgo</h3>
                <p class="role">Usuario</p>
                <p class="feedback">"Casi fui hackeada por un correo raro, pero este chatBot me ayudo completamente y ahora soy una persona mas feliz."</p>
                <div class="rating">
                    <span>⭐</span><span>⭐</span><span>⭐</span><span>⭐</span><span class="empty-star">⭐</span>
                </div>
            </div>
            <div class="testimonial">
                <img src="../assets/icons/persona2.png" alt="Emily S.">
                <h3>Antonio Castro.</h3>
                <p class="role">Gerente de Antonio S.A.S</p>
                <p class="feedback">"Este chatbot me a resultado bastante util porque aprendi como cuidarme de los virus en linea y tener mucha mas consciencia sobre el interneh y su peligroh"</p>
                <div class="rating">
                    <span>⭐</span><span>⭐</span><span>⭐</span><span>⭐</span><span>⭐</span>
                </div>
            </div>
            <div class="testimonial">
                <img src="../assets/icons/persona3.png" alt="John D.">
                <h3>River Bonilla</h3>
                <p class="role">Usuario</p>
                <p class="feedback">"He probado múltiples formas de cuidarme en linea, pero Cuando descubri ML SecureBot, mi vida se volvio mas feliz, La interfaz es intuitiva, y la seguridad es excelente."</p>
                <div class="rating">
                    <span>⭐</span><span>⭐</span><span>⭐</span><span>⭐</span><span>⭐</span>
                </div>
            </div>
        </div>
        <br>
        <br>
        <br>
    </section>
</template>

<script>
export default {
    name: 'AboutPage'
}
</script>

<style scoped>
.about {
    font-family: 'Poppins', sans-serif;
    padding: 40px;
    color: white;
    min-height: 100vh;
    background: linear-gradient(to bottom, #4F46A5 0%, #000000 100%);
}

h1, h2 {
    margin-bottom: 10px;
}

p, ul {
    margin-bottom: 20px;
}

ul {
    list-style-type: disc;
    padding-left: 20px;
}

.testimonials {
    display: flex;
    justify-content: center;
    gap: 25px;
    margin-top: 30px;
    flex-wrap: wrap;
    padding: 0 20px;
}

.testimonial {
    background: linear-gradient(to bottom right, #2C2C2C, #1B1B1B);
    border-radius: 20px;
    padding: 30px;
    width: calc(33.333% - 30px);
    min-width: 260px;
    max-width: 320px;
    text-align: center;
    transition: transform 0.3s ease-in-out;
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.5);
    flex: 0 1 auto;
}

.testimonial:hover {
    transform: translateY(-10px);
}

.testimonial img {
    width: 80px;
    height: 80px;
    border-radius: 50%;
    object-fit: cover;
    margin-bottom: 15px;
    border: 3px solid rgba(255, 255, 255, 0.3);
}

.testimonial h3 {
    font-size: 18px;
    margin-bottom: 5px;
    color: white;
}

.testimonial .role {
    font-size: 14px;
    font-weight: 300;
    margin-bottom: 15px;
    color: #a1a1ff;
}

.testimonial .feedback {
    font-size: 15px;
    line-height: 1.6;
    margin-bottom: 15px;
    color: #e0e0e0;
}

.testimonial .rating {
    font-size: 18px;
    color: gold;
}

.empty-star {
    color: rgba(255, 255, 255, 0.4);
}

@media screen and (max-width: 1024px) {
    .about {
        padding: 30px 15px;
    }

    .testimonials {
        gap: 20px;
    }

    .testimonial {
        width: calc(50% - 20px);
    }
}

@media screen and (max-width: 768px) {
    .about {
        padding: 25px 15px;
    }

    .testimonials {
        flex-direction: column;
        align-items: center;
        gap: 25px;
    }

    .testimonial {
        width: 100%;
        max-width: 400px;
        margin: 0;
    }
}

@media screen and (max-width: 480px) {
    .about {
        padding: 20px 10px;
    }

    .testimonials {
        padding: 0 10px;
        gap: 20px;
    }

    .testimonial {
        padding: 20px 15px;
    }

    .testimonial img {
        width: 60px;
        height: 60px;
    }

    h2 {
        font-size: 24px;
        text-align: center;
    }

    .testimonial h3 {
        font-size: 16px;
    }

    .testimonial .role {
        font-size: 13px;
    }

    .testimonial .feedback {
        font-size: 13px;
        line-height: 1.5;
    }
}

@media screen and (max-width: 320px) {
    .testimonial {
        padding: 15px 10px;
    }

    .testimonial .feedback {
        font-size: 12px;
    }
}
</style>
