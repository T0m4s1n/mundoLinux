<template>
    <div class="footer">
      <div class="bubbles">
        <div
          v-for="i in 128"
          :key="i"
          class="bubble"
          :style="{
            '--size': `${2 + Math.random() * 4}rem`,
            '--distance': `${6 + Math.random() * 4}rem`,
            '--position': `${-5 + Math.random() * 110}%`,
            '--time': `${2 + Math.random() * 2}s`,
            '--delay': `${-1 * (2 + Math.random() * 2)}s`
          }"
        ></div>
      </div>
      <div class="content">
        <div class="box">
          <div class="box1">
            <b>Empresas</b>
            <a href="#">Acerca de nosotros</a>
            <a href="#">Contacto</a>
          </div>
        </div>
        <div class="social-box">
          <b>Siguenos en nuestras redes Sociales</b>
          <div class="social-icons">
            <a href=""><img src="../assets/icons/Facebook.png" alt="Facebook" /></a>
            <a href=""><img src="../assets/icons/Twitter.png" alt="X" /></a>
            <a href=""><img src="../assets/icons/Instagram.png" alt="Instagram" /></a>
            <a href=""><img src="../assets/icons/Linkedin.png" alt="LinkedIn" /></a>
          </div>
        </div>
        <div class="copyright">
          <p>2024 © Todos los derechos reservados</p>
        </div>
        <div class="autor">
          <a href=""><img src="../assets/icons/icon2.png" alt="ML SecureBot" class="ml-icon" /></a>
          <p>Es una iniciativa de MundoLinux</p>
        </div>
      </div>
    </div>
  
    <svg style="position:fixed; top:100vh">
      <defs>
        <filter id="blob">
          <feGaussianBlur in="SourceGraphic" stdDeviation="10" result="blur" />
          <feColorMatrix
            in="blur"
            mode="matrix"
            values="1 0 0 0 0  0 1 0 0 0  0 0 1 0 0  0 0 0 19 -9"
            result="blob"
          />
        </filter>
      </defs>
    </svg>
  </template>
  
  <script>
  export default {
    name: "FooterPage"
  };
  </script>
  
  <style scoped>
  .footer {
    z-index: 1;
    --footer-background: #333;
    display: grid;
    position: relative;
    grid-area: footer;
    min-height: 12rem;
  }
  
  .bubbles {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 1rem;
    background: var(--footer-background);
    filter: url("#blob");
  }
  
  .bubble {
    position: absolute;
    left: var(--position, 50%);
    background: var(--footer-background);
    border-radius: 100%;
    animation: bubble-size var(--time, 4s) ease-in infinite var(--delay, 0s),
      bubble-move var(--time, 4s) ease-in infinite var(--delay, 0s);
    transform: translate(-50%, 100%);
  }
  
  .content {
    z-index: 2;
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-gap: 2rem;
    padding: 2rem;
    background: var(--footer-background);
    border-radius: 5px;
  }
  
  .box {
    padding: 1rem;
    border-radius: 5px;
    display: flex;
    gap: 2rem;
    background-color: #333;
    align-items: center;
    justify-content: center;
  }
  
  .box1 {
    display: flex;
    flex-direction: column;
    gap: 1rem;
    align-items: center;
  }
  
  .social-box {
    padding: 1rem;
    border-radius: 5px;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 1rem;
    background-color: #333;
  }
  
  .social-icons {
    display: flex;
    gap: 2rem;
  }
  
  .social-icons a img {
    width: 24px;
    height: 24px;
  }
  
  .social-icons a:hover {
    opacity: 0.8;
  }
  
  .copyright {
    grid-column: span 2;
    text-align: center;
  }
  
.autor {
    grid-column: span 2;
    text-align: center;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 0.5rem;
}
  
  .ml-icon {
    width: 160px;
    height: 100px;
  }
  
  p {
    margin: 0;
    font-size: 0.75rem;
    color: #f5f7fa;
  }
  
  a {
    text-decoration: none;
    color: #f5f7fa;
  }
  
  b {
    color: white;
  }
  
  @keyframes bubble-size {
    0%, 75% {
      width: var(--size, 4rem);
      height: var(--size, 4rem);
    }
    100% {
      width: 0rem;
      height: 0rem;
    }
  }
  
  @keyframes bubble-move {
    0% {
      bottom: -4rem;
    }
    100% {
      bottom: var(--distance, 10rem);
    }
  }
  </style>
  