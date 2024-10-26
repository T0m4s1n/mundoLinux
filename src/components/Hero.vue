<template>
  <div class="Hero-Background">
      <img class="to-mask" src="../assets/Hero-Background.png" width="100%" height="100%"/>
  </div>
</template>

<style>
.Hero-Background{
  margin-left: 50px;
}

.Hero-Background .to-mask{
  mask-image: url('../assets/MundoLinuxLogo.png');
  mask-size: cover;
  mask-repeat: no-repeat;
  -webkit-mask-image: url('../assets/MundoLinuxLogo.png'); /* Compatibilidad con navegadores webkit */
  -webkit-mask-size: cover;
  -webkit-mask-repeat: no-repeat; 
}
</style>

<script>
export default{
  name: "HeroView"
}
</script>