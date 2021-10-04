<template>
  <Header />
  <Navbar @page="change_page" />
  
  <About     v-if="current_page==1" />
  <Portfolio v-if="current_page==2" />
  
</template>

<script>
import Header from './components/Header.vue'
import Navbar from './components/Navbar.vue'
import About from './components/About.vue'
import Portfolio from './components/Portfolio.vue'

export default {
  name: 'App',
  components: { Header, Navbar, Portfolio, About },
  data: function(){
    return {
      current_page: 1
    }
  },
  methods: {
    change_page(n){
      this.current_page = n
    }
  }
  
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Lato&display=swap');

:root {
    font-size: 60%;

    --color-background: #fdfcdc;

    --color-background-light: #fed9b7;

    --color-primary: #0081A7;

    --color-secundary: #00AFB9;

    --color-background-dark: #545454;
    --color-text: #181818;

    --color-warning: #f07167;
}

*{
    margin: 0px;
    padding: 0px;
    box-sizing: border-box;
    font-family: 'Lato', sans-serif;
}

html, body, #root {
    height: 100%;
    background-color: var(--color-background);
}
</style>
