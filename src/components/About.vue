<template>
    <section class="about">
        <div class="topic">
            <div class="image"></div>
            <!-- <img width="100" src="" alt=""> -->
            <span>O Firefox limpa seu histórico de pesquisa e navegação quando você sai do aplicativo ou fecha todas as abas e janelas de navegação privativa. Apesar disso não tornar você anônimo para sites e para seu provedor de serviços de internet, facilita manter o que você faz online privativo para outras pessoas que usam este computador.</span>
        </div>

        <div class="topic">
            <div class="image"></div>
            <!-- <img width="100" src="" alt=""> -->
            <span>O Firefox limpa seu histórico de pesquisa e navegação quando você sai do aplicativo ou fecha todas as abas e janelas de navegação privativa. Apesar disso não tornar você anônimo para sites e para seu provedor de serviços de internet, facilita manter o que você faz online privativo para outras pessoas que usam este computador.</span>
        </div>
    </section>
</template>

<script>
export default {
  name: 'About',
  data: function(){
      return {
          
      }
  }
}
</script>

<style>
.about {
    padding: 50px;
}
.topic .image {
    width: 500px;
    height: 100%;
    background: url('https://images.ctfassets.net/swt2dsco9mfe/5hvcpZM9EuL4dYa9cnPfW2/9a62a131d86b308bf7a114ebca4fbf64/c9yJAEn8GDeHWqD-hero-bg.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    border-radius: 20px;
}
.about .topic {
    display: flex;
    justify-content: space-around;
    align-items: center;
    height: 500px;
    margin-bottom: 50px;
}
.topic span {
    width: 45%;
    font-size: 28px;
}
</style>
