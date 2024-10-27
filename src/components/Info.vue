<template>
    <section class="container">
       <div class="hex-section">
           <div class="hex-grid">
               <div class="hex first-row">
                   <div class="hex-content">
                       <img src="../assets/icons/icon9.png" alt="Bitcoin">
                       <h3>Calidad</h3>
                       <p>El mayor proposito de ML SecureBot es asegurar la calidad de sus respuestas para los usuarios.</p>
                   </div>
               </div>
               <div class="hex first-row">
                   <div class="hex-content">
                       <img src="../assets/icons/icon8.png" alt="Bitcoin">
                       <h3>Accesibilidad</h3>
                       <p>Utiliza ML SecureBot a traves de Whatsapp en cualquier dispositivo./p>
                   </div>
               </div>
               <div class="hex second-row">
                   <div class="hex-content">
                       <img src="../assets//icons/comunicacion1.png" alt="Trade Securely">
                       <h3>Conversaciones Seguras</h3>
                       <p>Tus conversaciones con ML SecureBot son completamente seguras</p>
                   </div>
               </div>
               <div class="hex second-row">
                   <div class="hex-content">
                       <img src="../assets/icons/icon3.png" alt="Insightful feedback">
                       <h3>Reporte Inmediato</h3>
                       <p>Cuando el usuario chatea con ML SecureBot este respondera de inmediato con todo el reporte del incidente</p>
                   </div>
               </div>
               <div class="hex third-row">
                   <div class="hex-content">
                       <img src="../assets/icons/icon6.png" alt="Sellam Wallet for Free">
                       <h3>Concientizacion</h3>
                       <p>ML SecureBot busca que el usuario conozca mas los peligros y sepa protegerse en todo momento sobre sus vulnerabilidades.</p>
                   </div>
               </div>
               <div class="hex third-row">
                   <div class="hex-content">
                       <img src="../assets/icons/icon4.png" alt="Invite friends">
                       <h3>Analisis real</h3>
                       <p>El analisis de los casos que presente el usuario se realizan en tiempo real para dar la respuesta acertada lo mas rapido posible</p>
                   </div>
               </div>
           </div>
       </div>
       <div class="cta">
           <h2>ML SecureBoot esta listo para chatear contigo</h2>
           <p>Puedes comunicarte con ML SecureBot cuando quieras donde quieras, solo es necesario que abras un chat y empieces!</p>
               <img src="../assets/qr-code.png" alt="Start Chat" style="width: 250px; height: 250px; margin-right: 10px;">
       </div>
   </section>
   
</template>
<script>
export default {
 name: 'InfoView',
}
</script>
<style>
.container {
   display: flex;
   align-items: flex-start;
   justify-content: center;
   padding: 60px;
   background: linear-gradient(to bottom, #000000 0%, #4F46A5 100%);
}

.hex-section {
   display: flex;
   justify-content: flex-start;
   flex: 1;
   margin-right: 50px;
}

.hex-grid {
   display: grid;
   grid-template-columns: repeat(2, 1fr);
   gap: 20px;

}

.hex {
   width: 220px;
   height: 250px;
   background-color: #222;
   clip-path: polygon(50% 0%, 100% 25%, 100% 75%, 50% 100%, 0% 75%, 0% 25%);
   display: flex;
   align-items: center;
   justify-content: center;
   transition: transform 0.3s;
   box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
}

.hex-content {
   text-align: center;
   padding: 10px;
   color: #fff;
}

.hex-content img {
   width: 40px;
   height: 40px;
   margin-bottom: 10px;
}

.hex-content h3 {
   font-size: 16px;
   margin-bottom: 10px;
}

.hex-content p {
   font-size: 12px;
   color: #ccc;
}

.hex:hover {
   transform: scale(1.05);
}

.first-row {
   margin-left:50px;
}

.second-row {
   margin-right:50px;
}

.third-row {
   margin-left:50px;
}

.cta {
   text-align: left;
   max-width: 600px;
   margin-top: 5cm;
}

.cta h2 {
   font-size: 28px;
   margin-bottom: 10px;
   color: #fff;
}

.cta p {
   font-size: 16px;
   color: #ccc;
   margin-bottom: 20px;
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
