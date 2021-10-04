<template>
  <section class="portfolio">
    <nav class="filter-tecnologies">
      <button>Front-end</button>
      <button>Back-end</button>
      <button>Typescript</button>
      <button>ReactJS</button>
      <button>VueJS</button>
      <button>ExpressJS</button>
      <button>NestJS</button>
    </nav>

    <div class="projetos">

      <div class="container">
        <div class="about">
          <h2 class="title">Chat boladão</h2>
          <span class="sub-title">Chat mucho loko para conversar, completão</span>
          <div class="tecnologies">ReactJS, Typescript</div>
        </div>
      </div>
      <div class="container">
        <div class="about">
          <h2 class="title">Chat boladão</h2>
          <span class="sub-title">Chat mucho loko para conversar, completão</span>
          <div class="tecnologies">ReactJS, Typescript</div>
        </div>
      </div>
      <div class="container">
        <div class="about">
          <h2 class="title">Chat boladão</h2>
          <span class="sub-title">Chat mucho loko para conversar, completão</span>
          <div class="tecnologies">ReactJS, Typescript</div>
        </div>
      </div>

    </div>
  </section>

</template>

<script>
export default {
  name: 'Portfolio',
  data: function(){
      return {
          
      }
  }
}
</script>

<style>
.portfolio {
  min-height: 500px;
}
.filter-tecnologies {
  display: flex;
  justify-content: center;
  gap: 7px;
  margin-top: 17px;
  margin-bottom: 7px;
}
.filter-tecnologies button {
  background-color: var(--color-background-dark);
  color: #f2f2f2;
  border: none;
  outline: none;
  border-radius: 5px;
  padding: 10px;
  border-bottom: 2px solid grey;
}
.filter-tecnologies button[active] {
  background-color: grey;
}

.projetos {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 10px;
  padding: 10px;
}
.projetos .container {
  width: 400px;
  height: 300px;
  border-radius: 10px;
  position: relative;
  background: url('https://raw.githubusercontent.com/talis-fb/Chat/main/screenshot1.png');
  background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
}
.projetos .container .about {
  color: var(--color-background);
  text-align: center;
  position: absolute;
  font-size: 18px;
  width: 100%;
  height: 30%;
  bottom: 0;
  border-bottom-left-radius: 10px;
  border-bottom-right-radius: 10px;
  opacity: 0.95;
  background-color: var(--color-background-dark);
}
.sub-title {
  font-size: 15px;
}
</style>
