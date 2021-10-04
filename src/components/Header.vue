<template>
    <header>
        <h1>Olá, Eu sou alguma pessoa que </h1>

        <div class="icons">
            <a class="social-medias" > <img width="10" height="10" src="https://www.svgrepo.com/show/280479/email.svg"/> </a>
            <a class="social-medias" > <img src="https://www.svgrepo.com/show/22753/whatsapp-logo-variant.svg"/> </a>
            <a class="social-medias" target="_blanc" href="https://github.com/talis-fb"> <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg"/> </a>
            <a class="social-medias" target="_blanc" href="https://www.linkedin.com/in/talison-fabio-9097001b2/"> <img src="https://icons.getbootstrap.com/assets/icons/linkedin.svg"/> </a>
        </div>
    </header>
</template>

<script>
export default {
  name: 'Header',
  data: function(){
      return {
          
      }
  }
}
</script>

<style>
header {
    background-color: var(--color-background-dark);
    color: var(--color-background);
    height: 600px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}
.icons {
    display: flex;
}
.social-medias {
    background-color: var(--color-secundary);
    width: 50px;
    height: 50px;
    border-radius: 10px;
    display: flex;
    justify-content: center;
    align-items: center;
}
.social-medias img {
    width: 90%;
    height: 90%;
}

</style>
