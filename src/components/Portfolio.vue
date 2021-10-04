<template>
  <section class="portfolio">
    <nav class="filter-tecnologies">  
      <button v-for="i of tecnologies" :key="i.name">{{ i.name }}</button>
    </nav>

    <div class="projetos">

      <div class="container" v-for="(proj, ind) in projects" :key="ind">
        <div class="about">

          <h2 class="title"> {{ proj.title }}</h2>

          <span class="sub-title"> {{ proj.subtitle}} </span>

          <div class="tecnologies">
            <img v-for="i in proj.tecnologies" :key="i" height="30" :src="tecnologies[i].icon" alt="">
          </div>
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
        filters: [1],
          tecnologies: [
            /* 0 */{ name: 'Javascript', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg'},
            /* 1 */{ name: 'Typescript', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg'},

            /* 2 */{ name: 'ReactJS', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg'},
            /* 3 */{ name: 'VueJS', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vuejs/vuejs-original.svg'},

            /* 4 */{ name: 'Sass', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/sass/sass-original.svg'},
            /* 5 */{ name: 'Bootstrap', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bootstrap/bootstrap-plain.svg'},

            /* 6 */{ name: 'Webpack', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/webpack/webpack-original.svg'},
            /* 7 */{ name: 'NodeJS', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg'},

            /* 8 */{ name: 'NestJS', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nestjs/nestjs-plain.svg'},
            /* 9 */{ name: 'MongoDB', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mongodb/mongodb-original.svg'},

            /* 10 */{ name: 'MySQL', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg'},
            /* 11 */{ name: 'SQLite', icon: 'https://upload.wikimedia.org/wikipedia/commons/thumb/9/97/Sqlite-square-icon.svg/384px-Sqlite-square-icon.svg.png'},

            /* 12 */{ name: 'Front-end', icon: ''},
            /* 13 */{ name: 'Back-end', icon: ''}
          ],
          projects: [
            { title: 'Chat', tecnologies: [2,4,5,6,1,7,9, 12, 13], subtitle: '', image: ''},
            { title: 'Pokedex-react', tecnologies: [2,5, 12], subtitle: '', image: ''},
            { title: 'Pokedex-vue', tecnologies: [3,1,4, 12], subtitle: '', image: ''},
            { title: 'Clone Web site Dota 2', tecnologies: [3,4, 12], subtitle: '', image: ''},
            { title: 'SQLClient', tecnologies: [7,11, 12, 13], subtitle: '', image: ''},
            { title: 'Server-EstoqueRFID', tecnologies: [7,11, 13], subtitle: '', image: ''},
            { title: 'Calculadora React', tecnologies: [2, 12], subtitle: '', image: ''},
            { title: 'Snakegame', tecnologies: [0, 12], subtitle: '', image: ''},
            { title: 'Player Video Web', tecnologies: [0, 12], subtitle: '', image: ''},
          ]
      }
  },
  computed: {
    projects_filtered(){
      // NÃO IMPLEMENTADO
      if( !this.filters.length )
        return this.projects
      return 0
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
