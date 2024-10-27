<template>
    <header class="app-header">
      <nav class="navbar">
        <div class="navbar-left">
          <img src="@/assets/icons/icon2.png" alt="Logo" class="logo" />
          <ul class="nav-links">
            <li><a href="#comandos">Comandos</a></li>
            <li><a href="#about">Acerca de Nosotros</a></li>
            <li><a href="https://ml-securebot.vercel.app/">Panel de administrador</a></li>
          </ul>
        </div>
        <div class="navbar-right">
          <a href="https://wa.link/rdrmgl" class="chat-button">Chat</a>
          <span class="language-icon">🌐</span>
        </div>
      </nav>
    </header>
  </template>
  
  <script>
  export default {
    name: 'AppHeader',
  }
  </script>
  
  <style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Source+Sans+Pro:wght@400;600&display=swap');
  @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap');
  
  .app-header {
    position: fixed;
    top: 0;
    left: 35px;
    z-index: 1000;
    background-color: #333;
    padding: 10px 40px;
    border-radius: 20px;
    display: flex;
    justify-content: center;
    align-items: center;
    width: 91%;
    margin: 20px auto;
    box-shadow: 0px 4px 12px rgba(0, 0, 0, 0.1);
    font-family: 'Source Sans Pro', sans-serif;
  }
  
  .navbar {
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  .navbar-left {
    display: flex;
    align-items: center;
  }
  
  .logo {
    height: 40px;
    margin-right: 20px;
  }
  
  .nav-links {
    list-style: none;
    display: flex;
    gap: 20px;
  }
  
  .nav-links li {
    display: inline-block;
  }
  
  .nav-links a {
    text-decoration: none;
    color: #ffffff;
    font-size: 1rem;
    font-weight: 600;
  }
  
  .navbar-right {
    display: flex;
    align-items: center;
    gap: 20px;
  }

  .chat-button {
    background: linear-gradient(90deg, #f953c6, #2E16FA);
    color: white;
    font-size: 1rem;
    font-weight: 600;
    padding: 10px 20px;
    border: none;
    border-radius: 30px;
    cursor: pointer;
    font-family: 'Poppins', sans-serif;
    transition: transform 0.5s ease-in-out, opacity 0.5s ease-in-out;
    text-decoration: none;
  }

  .chat-button:hover {
    transform: translateY(-5px);
    opacity: 0.9;
    border:2px solid #f953c6; 
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
  .language-icon {
    font-size: 1.5rem;
    color: #ffffff;
  }
  </style>
  
